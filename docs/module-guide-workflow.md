# Module Guide Workflow

How to run the E→P→A→V commands against a folder inside `modules/`.

## What this is

`/evaluate`, `/plan`, `/apply`, and `/validate` accept a module folder as their target. When the
target resolves to a folder directly under `modules/`, the command switches to **module-guide mode**:
it reads that module's curriculum files and produces a guide for completing the module.

Module-guide mode **does not** implement the module's React Native code, install packages, run builds,
or edit the curriculum inputs. The only file it writes is:

```
modules/<folder>/guide.md
```

The existing `brief.md`, `tasks.md`, `write-up-template.md`, and any `module_<NN>.md` are treated as
read-only source material.

## Quick start

Use a module ID:

```text
/evaluate m01
/plan m01
/apply m01
/validate m01
```

Or use the full folder name:

```text
/evaluate m01-toolchain-hybrid-project-setup
/plan m01-toolchain-hybrid-project-setup
/apply m01-toolchain-hybrid-project-setup
/validate m01-toolchain-hybrid-project-setup
```

Or run the whole cycle in one command:

```text
/epav m01
```

`/epav` still stops at the approval gate before APPLY.

## Folder resolution

Every command resolves its first argument the same way:

1. An existing path to a directory directly under `modules/` — e.g.
   `modules/m05-dev-workflow-professional-structure`.
2. `modules/<target>` — e.g. `m05-dev-workflow-professional-structure`.
3. A module ID matching the `mNN-` prefix, case-insensitive — e.g. `m05` or `M05`.
4. A unique, case-insensitive substring of a folder name — e.g. `firebase` resolves to
   `m06-firebase-bare-project`.

If no folder matches, or more than one folder matches, the command lists the candidates and stops.
It never guesses. Use the full folder name when a partial name is ambiguous.

A target that does not resolve to a module folder keeps the command's original task-mode behavior.
For example, `/evaluate "fix the login timeout"` still evaluates a normal development task.

## The cycle at a glance

| Command              | Reads                                                                                     | Writes                       | Stops with                        |
| -------------------- | ----------------------------------------------------------------------------------------- | ---------------------------- | --------------------------------- |
| `/evaluate <folder>` | Module brief, tasks, write-up template, README, relevant docs, knowledge graph if present | Nothing                      | `EVALUATE SUMMARY — MODULE GUIDE` |
| `/plan <folder>`     | Everything from EVALUATE, plus the module's source-to-guide mapping                       | Nothing                      | `GUIDE PLAN`                      |
| `/apply <folder>`    | The approved plan and the module sources                                                  | `modules/<folder>/guide.md`  | `APPLY COMPLETE`                  |
| `/validate <folder>` | The guide and every module source it claims to cover                                      | Fixes inside `guide.md` only | `VALIDATE COMPLETE`               |

Each command is a separate invocation. Run them in order, one folder at a time.

## What each command does

### `/evaluate <folder>`

Orients before anything is planned or written.

1. Queries the active knowledge graph when one exists (`graphify-out/graph.json` or
   `.codegraph/codegraph.db`). If neither exists, it continues and notes the gap.
2. Reads in full:
   - `modules/<folder>/brief.md` — required; stop if missing.
   - `modules/<folder>/tasks.md` — if present.
   - `modules/<folder>/write-up-template.md` — if present.
   - `modules/<folder>/module_<NN>.md` — if present, as prior teaching material.
   - `README.md` and the relevant `docs/` material.
   - The briefs of modules named under **Builds on**.
3. Extracts the module's objective, deliverable, scope, stack constraints, dependencies, lab,
   definition of done, logistics, open items, and write-up sections.
4. Outputs an EVALUATE SUMMARY and stops. It does not write the guide and does not plan.

### `/plan <folder>`

Turns the evaluation into a guide blueprint.

1. Requires `/evaluate <folder>` to have run for the same module. If it has not, stop and ask.
2. Runs the blast-radius/impact check against the active knowledge graph where available.
3. Maps each source section to a guide section, so nothing in the brief is silently dropped.
4. Outputs a GUIDE PLAN containing:
   - the target guide path,
   - the guide outline,
   - a coverage table (source → guide section),
   - assumptions and items that must stay flagged as open,
   - the exact list of files to touch — which is always `guide.md` alone.
5. Stops and waits for approval.

### `/apply <folder>`

Writes the guide. Nothing else.

1. Requires an approved GUIDE PLAN for the same module.
2. Writes `modules/<folder>/guide.md` using the approved outline and only facts found in the module
   sources.
3. If `guide.md` already exists:
   - a file written by this workflow starts with
     `<!-- generated-by: /apply module-guide-mode -->` and can be replaced;
   - a file without that marker, or with manual edits, is not overwritten without confirmation.
4. Does not edit `brief.md`, `tasks.md`, `write-up-template.md`, or `module_<NN>.md`. Does not create
   app code, install packages, or run builds.
5. Outputs APPLY COMPLETE.

### `/validate <folder>`

Checks the guide against the module it describes.

1. Requires `/apply <folder>` to be complete and `guide.md` to exist.
2. Checks coverage:
   - every definition-of-done item appears in the guide's verification section;
   - every `tasks.md` checklist item is represented;
   - every `write-up-template.md` section is mapped;
   - objective, deliverable, scope, constraints, prerequisites, and evidence capture are present;
   - logistics and open items remain visibly flagged.
3. Checks honesty:
   - no invented versions, commands, package names, or acceptance criteria;
   - every version-specific claim is sourced from the brief or marked for cohort-freeze
     confirmation;
   - no curriculum input was modified;
   - no app code was written in this repository.
4. Classifies issues as `[BLOCKER]`, `[FIX NOW]`, or `[BACKLOG]`.
5. Fixes BLOCKERs and FIX NOWs inside `guide.md` only.
6. Outputs VALIDATE COMPLETE with a coverage count.

## Generated guide structure

`modules/<folder>/guide.md` follows this outline. `/plan` may refine the section names, but it must
keep the coverage:

```markdown
<!-- generated-by: /apply module-guide-mode -->

# M0X — <Title> Guide

> Generated by /apply from this module's brief, tasks, and write-up template.
> This is a how-to guide, not the module's official write-up or module\_<NN>.md.
> Verify version-specific commands against the cohort's pinned baseline before relying on them.

## 1. At a glance

## 2. Prerequisites and what this builds on

## 3. What you are building (scope and deliverable)

## 4. Stack constraints

## 5. Environment setup and checks

## 6. Step-by-step build

## 7. Verification and definition of done

## 8. Evidence to capture for the write-up

## 9. Write-up map

## 10. Pitfalls, logistics, and open items

## 11. References
```

The guide is a teaching aid. It is **not** the official `write-up-template.md` fill-in and it does
**not** replace the `module_<NN>.md` teaching material that the module's own tasks call for after the
build passes VALIDATE.

## Guardrails

- Work on one module at a time.
- Treat module files as read-only. The only writable output is `guide.md`.
- Prefer the module's own wording. When the brief does not settle something, say so with
  `[confirm with trainer]` or `[verify at cohort freeze]` rather than inventing a version, command,
  or acceptance criterion.
- The trainee's React Native project lives outside this repository. The guide should say where the
  work happens, but the commands do not create or modify that project.
- If the module's brief is missing, stop. Do not build a guide from `tasks.md` alone.
- If `guide.md` has manual edits, ask before replacing them.

## Worked example: M01

```text
/evaluate m01
```

Produces an EVALUATE SUMMARY for `modules/m01-toolchain-hybrid-project-setup`: objective, the
`PersonalProfileApp` deliverable, toolchain constraints, the three planted faults, the definition of
done, and the open logistics items the trainer must confirm.

```text
/plan m01
```

Produces a GUIDE PLAN mapping M01's Setup, Build, Verify, and Write-up task groups into the guide
outline. It names `modules/m01-toolchain-hybrid-project-setup/guide.md` as the only file to write.

```text
/apply m01
```

Writes `modules/m01-toolchain-hybrid-project-setup/guide.md`. It does not create the React Native
project, install tools, or fill in `write-up-template.md`.

```text
/validate m01
```

Checks that every M01 definition-of-done item and every `tasks.md` item is represented, that the
three planted faults and the README evidence are captured, and that no unsourced version numbers
were invented. Fixes only `guide.md`, then reports `VALIDATE COMPLETE`.

## Troubleshooting

**"No module folder matched"** — run `ls modules` and use the full folder name. Module IDs are
`m01` through `m11`.

**"More than one module matched"** — the partial name is ambiguous. Use the full folder name.

**The guide already exists** — `/apply` will replace a generated guide. If you edited it manually,
it will ask before overwriting. `/validate` always limits its fixes to `guide.md`.

**The commands started doing development work on a module** — the target did not resolve to a module
folder. Re-run with the exact folder name or module ID; the command should print the resolved
`MODULE_DIR` in its summary.

**The module has no `tasks.md`** — `/evaluate` notes it and continues from `brief.md` and
`write-up-template.md`. The guide will be thinner, and `/validate` will flag the missing checklist
as a gap rather than inventing tasks.

## Related files

- `.opencode/commands/evaluate.md`
- `.opencode/commands/plan.md`
- `.opencode/commands/apply.md`
- `.opencode/commands/validate.md`
- `.opencode/commands/epav.md`
- `README.md` — module index and ground rules
