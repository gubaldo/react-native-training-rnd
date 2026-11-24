# M02 Write-Up — Community Modules and Native Linking

> Fill this in as you go. Write it so a trainee starting this stage next cohort could follow your
> path on their own.

## What I built

AsyncStorage, vector icons and safe-area-context linked into the profile app, plus the lock-in
audit.

## Why it's built this way (key decisions)

- AsyncStorage is the key-value storage system for React Native
- Vector icons is UI icons library
- Safe-area context is essential for handling status bar, dynamic island and home indicator
- Autolinking connects standard native code automatically, but for some, you still have to step in manually for extra setup like font files and special setup for Android or iOS configs.

## How to build it (teach it to the next trainee)

Check the documentation of the dependencies or libraries.

When installing:

iOS: Run pod install in ios/, check \*.xcworkspace / Xcode build settings if needed, and do a clean native build.

Android: Sync Gradle, check MainApplication / AndroidManifest.xml if manual wiring is needed, and run a fresh native build.

Test both platforms to make sure everything works properly.

## Concepts worth explaining

Autolinking automatically finds installed native packages and connects them to the iOS and Android projects when you build your app, so you don't have to edit native project files manually.

## What tripped me up

None

## Checkpoint evidence

Go to evidence/m02 to see the screenshots, txt and md files.

## What I'd do differently

Nothing major to change. The module's step-by-step instructions provided a clear, reliable roadmap from setup to verification.
