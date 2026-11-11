# M01 Write-Up — Toolchain and Hybrid Project Setup

Project Repository: https://github.com/gubaldo/PersonalProfileApp.git

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

— Metro is the JavaScript bundler for React Native. It runs as a local development server that packages your code and assets, instantly streaming them to your phone or simulator whenever changes occur.

- ios/ and android/ folder contain the native project required to wrap and execute the JavaScript code.

## What tripped me up

No version mismatches were encountered during the execution.

## Checkpoint evidence

Go to evidence/m01 to see the screenshots and md files.

## What I'd do differently

Nothing major to change. The module's step-by-step instructions provided a clear, reliable roadmap from setup to verification.
