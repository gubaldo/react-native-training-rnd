geremyubaldo@AOCSGOMDY663 PersonalProfileApp % export ANDROID_HOME=/nonexistent/android-sdk
echo "$ANDROID_HOME"
npx expo run:android
/nonexistent/android-sdk
Failed to resolve the Android SDK path. ANDROID_HOME is set to a non-existing path: /nonexistent/android-sdk
Failed to resolve the Android SDK path. ANDROID_HOME is set to a non-existing path: /nonexistent/android-sdk
Failed to resolve the Android SDK path. ANDROID_HOME is set to a non-existing path: /nonexistent/android-sdk

eremyubaldo@AOCSGOMDY663 PersonalProfileApp % echo 'export ANDROID_HOME="$HOME/Library/Android/sdk"' >> ~/.zshrc
echo 'export PATH="$PATH:$ANDROID_HOME/emulator:$ANDROID_HOME/platform-tools"' >> ~/.zshrc
source ~/.zshrc
echo "$ANDROID_HOME"
adb --version
cd ~/Projects/PersonalProfileApp
npx expo run:android
/Users/geremyubaldo/Library/Android/sdk
Android Debug Bridge version 1.0.41
Version 36.0.0-13206524
Installed as /Users/geremyubaldo/Library/Android/sdk/platform-tools/adb
Running on Darwin 27.2.0 (arm64)
cd: no such file or directory: /Users/geremyubaldo/Projects/PersonalProfileApp
› Building app...
Configuration on demand is an incubating feature.

> Configure project :app
> WARNING: The option setting 'android.builtInKotlin=false' is deprecated.
> The current default is 'true'.
> It will be removed in version 10.0 of the Android Gradle plugin.
> WARNING: The option setting 'android.newDsl=false' is deprecated.
> The current default is 'true'.
> It will be removed in version 10.0 of the Android Gradle plugin.
> ℹ️ Applying gradle plugin 'expo-max-sdk-override-plugin'
> [expo-max-sdk-override-plugin] This plugin will find all permissions declared with `android:maxSdkVersion`. If there exists a declaration with the `android:maxSdkVersion` annotation and another one without, the plugin will remove the annotation from the final merged manifest. In order to see a log with the changes run a clean build of the app.
> WARNING: API 'applicationVariants' is obsolete and has been replaced with 'AndroidComponentsExtension'.
> It will be removed in version 10.0 of the Android Gradle plugin.
> The legacy variant API is disabled by default in AGP 9.0, but can be re-enabled by adding

    android.newDsl=false

to this project's gradle.properties file.
For more information, see http://developer.android.com/build/r/new-dsl.

To determine what is calling applicationVariants, use -Pandroid.debug.obsoleteApi=true on the command line to display more information.
WARNING: API 'testVariants' is obsolete and has been replaced with 'AndroidComponentsExtension'.
It will be removed in version 10.0 of the Android Gradle plugin.
The legacy variant API is disabled by default in AGP 9.0, but can be re-enabled by adding
android.newDsl=false
to this project's gradle.properties file.
For more information, see http://developer.android.com/build/r/new-dsl.

To determine what is calling testVariants, use -Pandroid.debug.obsoleteApi=true on the command line to display more information.
WARNING: API 'unitTestVariants' is obsolete and has been replaced with 'AndroidComponentsExtension'.
It will be removed in version 10.0 of the Android Gradle plugin.
The legacy variant API is disabled by default in AGP 9.0, but can be re-enabled by adding
android.newDsl=false
to this project's gradle.properties file.
For more information, see http://developer.android.com/build/r/new-dsl.

To determine what is calling unitTestVariants, use -Pandroid.debug.obsoleteApi=true on the command line to display more information.

> Configure project :
> [ExpoRootProject] The Kotlin Gradle plugin used by this build is 2.2.10, but the version catalog declares 2.2.0. Using the plugin version.
> [ExpoRootProject] Using the following versions:

- buildTools: 37.0.0
- minSdk: 24
- compileSdk: 37
- targetSdk: 36
- ndk: 27.1.12297006
- kotlin: 2.2.10
- ksp: 2.2.10-2.0.2

> Configure project :expo
> WARNING: API 'libraryVariants' is obsolete and has been replaced with 'AndroidComponentsExtension'.
> It will be removed in version 10.0 of the Android Gradle plugin.
> The legacy variant API is disabled by default in AGP 9.0, but can be re-enabled by adding

    android.newDsl=false

to this project's gradle.properties file.
For more information, see http://developer.android.com/build/r/new-dsl.

To determine what is calling libraryVariants, use -Pandroid.debug.obsoleteApi=true on the command line to display more information.

Using expo modules

- expo-dom-webview (58.0.2)
- expo-log-box (58.0.15)
- expo-constants (58.0.15)
- expo-modules-core (58.0.30)
- [📦] expo-asset (58.0.20)
- [📦] expo-file-system (58.0.13)
- [📦] expo-font (58.0.11)
- [📦] expo-keep-awake (58.0.3)
- [📦] expo-status-bar (58.0.4)

[Incubating] Problems report is available at: file:///Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/android/build/reports/problems/problems-report.html

Deprecated Gradle features were used in this build, making it incompatible with Gradle 10.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

For more on this, please refer to https://docs.gradle.org/9.4.1/userguide/command_line_interface.html#sec:command_line_warnings in the Gradle documentation.

BUILD SUCCESSFUL in 2s
