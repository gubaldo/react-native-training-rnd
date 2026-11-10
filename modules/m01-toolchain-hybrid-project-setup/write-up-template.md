# M01 Write-Up — Toolchain and Hybrid Project Setup

> Fill this in as you go. Write it so a trainee starting this stage next cohort could follow your
> path on their own.

## What I built

`PersonalProfileApp`'s skeleton using expo workflow configuration that includes build setups for iOS and Android with README as a guide to clone the project.

## Why it's built this way (key decisions)

- I chose npx create-expo-app with the bare-minimum template so I start on a clean project and avoid refactoring the existing code.
- First is the node version wherein i forced to use Node 20. It showed and error that version 20 is outdated and unsupported, and we should updated to >=22.13.0. After installing version 24, i verify the version using node -v command and also npx expo-doctor for verification.

## How to build it (teach it to the next trainee)

Install the pre-requisite:

- Node.js
- Watchman
- Android Studio and Xcode

Clone and run npm install.

Run "npx expo doctor" to verify if pass before proceeding

Execute cd ios && pod install to setup iOS while for android, setup is already automatic.

## Concepts worth explaining

Pick 1-2 ideas — for example what Metro, Hermes and the native shell each do, or why the bare
workflow commits `ios/` and `android/` even though EAS Build still does the actual building for you
— Metro is the JavaScript bundler for React Native. It acts as a local development server that serves your bundled JavaScript code for your phone or simulator to fetch and execute.

## What tripped me up

No version mismatches were encountered during the execution.

## Checkpoint evidence

Show the fresh clone running on both platforms from the README alone, the clean `expo-doctor`
output, and the three fixed faults.

## What I'd do differently

If you started this module over, what would you do differently?
