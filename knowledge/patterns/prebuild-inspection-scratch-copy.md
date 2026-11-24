# Pattern: Inspect `expo prebuild` output without touching committed native folders

**When to use:** a module asks a learner to run `npx expo prebuild` only to *read* the generated
`ios/` and `android/` folders, while the program's ground rule is that those folders stay committed
and hand-managed (bare workflow). Running prebuild in the real repo risks overwriting them.

**Pattern:** generate in a throwaway copy, not in the project.

```bash
mkdir -p /tmp/<module>-prebuild
rsync -a --exclude node_modules --exclude ios --exclude android --exclude .git \
  ./ /tmp/<module>-prebuild/
ln -s "$(pwd)/node_modules" /tmp/<module>-prebuild/node_modules
cd /tmp/<module>-prebuild
npx expo prebuild --no-install
```

**Why each part matters:**

- Excluding `ios`/`android` makes Expo generate fresh folders rather than prompting to overwrite.
- Excluding `.git` keeps the scratch copy out of the learner's commit history.
- Symlinking `node_modules` makes `npx` use the project's pinned Expo version instead of downloading
  an unpinned one — essential when the cohort freezes exact versions.
- `--no-install` skips CocoaPods/Gradle work because the goal is only to read files.
- After the skim, verify the real repo is unchanged with `git status --short`.

**Decision rule:** use this pattern by default. Run prebuild in place only when the module
intentionally asks the learner to regenerate and commit native folders; state that condition
explicitly rather than leaving it implied.

**Source:** discovered while validating `modules/m03-ios-android-project-internals/guide.md`, whose
brief asks for a read-only skim of generated native folders while README ground rules keep those
folders committed.
