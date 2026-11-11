geremyubaldo@AOCSGOMDY663 PersonalProfileApp % rm -rf ios/Pods ios/Podfile.lock
npx expo run:ios --no-install
› Planning build

❌ Unable to open base configuration reference file '/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/Pods/Target Support Files/Pods-PersonalProfileApp/Pods-PersonalProfileApp.debug.xcconfig'. (in target 'PersonalProfileApp' from project 'PersonalProfileApp')

› 1 error(s), and 0 warning(s)

CommandError: Failed to build iOS project. "xcodebuild" exited with error code 65.
Build logs written to /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/.expo/xcodebuild.log
geremyubaldo@AOCSGOMDY663 PersonalProfileApp % cd ios
geremyubaldo@AOCSGOMDY663 ios % pod install
cd ..
npx expo run:ios
Using Expo modules
[Expo] Enabling modular headers for pod ExpoModulesCore
[Expo] Enabling modular headers for pod React-Core
[Expo] Enabling modular headers for pod ExpoModulesJSI
[Expo] Enabling modular headers for pod React-RCTAppDelegate
[Expo] Enabling modular headers for pod React-RCTFabric
[Expo] Enabling modular headers for pod ReactAppDependencyProvider
[Expo] Enabling modular headers for pod ReactCodegen
[Expo] Enabling modular headers for pod RCTRequired
[Expo] Enabling modular headers for pod RCTTypeSafety
[Expo] Enabling modular headers for pod React-bridging
[Expo] Enabling modular headers for pod ReactCommon
[Expo] Enabling modular headers for pod React-NativeModulesApple
[Expo] Enabling modular headers for pod Yoga
[Expo] Enabling modular headers for pod React-Fabric
[Expo] Enabling modular headers for pod React-graphics
[Expo] Enabling modular headers for pod React-utils
[Expo] Enabling modular headers for pod React-featureflags
[Expo] Enabling modular headers for pod React-debug
[Expo] Enabling modular headers for pod React-ImageManager
[Expo] Enabling modular headers for pod React-rendererdebug
[Expo] Enabling modular headers for pod React-jsi
[Expo] Enabling modular headers for pod React-renderercss
[Expo] Enabling modular headers for pod React-cxxstableapi
[Expo] Enabling modular headers for pod hermes-engine
[Expo] Enabling modular headers for pod glog
[Expo] Enabling modular headers for pod boost
[Expo] Enabling modular headers for pod DoubleConversion
[Expo] Enabling modular headers for pod fast_float
[Expo] Enabling modular headers for pod fmt
[Expo] Enabling modular headers for pod RCT-Folly
[Expo] Enabling modular headers for pod SocketRocket
[Expo] Enabling modular headers for pod React-jsinspector
Found 1 module for target `PersonalProfileApp`
link_native_modules! {ios_packages: [{configurations: [], name: "expo", root: "/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/node_modules/expo", path: "../node_modules/expo", podspec_path: "/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/node_modules/expo/Expo.podspec", script_phases: []}], ios_project_root_path: "/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios", react_native_path: "../node_modules/react-native"}
Framework build type is static library
[ReactNativeDependencies] Setting up ReactNativeDependencies...
[ReactNativeDependencies] Building from source: false
[ReactNativeDependencies] Using tarball from URL: https://repo.reactnative.dev/maven2/com/facebook/react/react-native-artifacts/0.88.1/react-native-artifacts-0.88.1-reactnative-dependencies-debug.tar.gz
[ReactNativeDependencies] Verifying checksum for cached reactnative-dependencies-0.88.1-debug.tar.gz...
[Cache] SHA1 verified for reactnative-dependencies-0.88.1-debug.tar.gz
[ReactNativeDependencies] Cache hit: copying reactnative-dependencies-0.88.1-debug.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
[ReactNativeDependencies] Verifying checksum for cached reactnative-dependencies-0.88.1-release.tar.gz...
[Cache] SHA1 verified for reactnative-dependencies-0.88.1-release.tar.gz
[ReactNativeDependencies] Cache hit: copying reactnative-dependencies-0.88.1-release.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
[ReactNativeDependencies] Source: {http: "https://repo.reactnative.dev/maven2/com/facebook/react/react-native-artifacts/0.88.1/react-native-artifacts-0.88.1-reactnative-dependencies-debug.tar.gz"}
[ReactNativeCore] Setting up ReactNativeCore...
[ReactNativeCore] Building from source: false
Configuring the target with the New Architecture
[ReactNativeCore] Using React Native Core and React Native Dependencies prebuilt versions.
[Codegen] Analyzing /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/package.json
[Codegen] Searching for codegen-enabled libraries in the app.
[Codegen] The "codegenConfig" field is not defined in package.json. Assuming there is nothing to generate at the app level.
[Codegen] Searching for codegen-enabled libraries in react-native.config.js
[Codegen] No codegen-enabled libraries found.
[Codegen] Generating RCTThirdPartyComponentsProvider.h
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactCodegen/RCTThirdPartyComponentsProvider.h
[Codegen] Generating RCTThirdPartyComponentsProvider.mm
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactCodegen/RCTThirdPartyComponentsProvider.mm
[Codegen] Generating RCTModulesProvider.h
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactCodegen/RCTModuleProviders.h
[Codegen] Generating RCTModuleProviders.mm
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactCodegen/RCTModuleProviders.mm
[Codegen] Generating RCTAppDependencyProvider
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactAppDependencyProvider/RCTAppDependencyProvider.h
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactAppDependencyProvider/RCTAppDependencyProvider.mm
[Codegen] Generated podspec: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactAppDependencyProvider/ReactAppDependencyProvider.podspec
[Codegen] Generated podspec: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/ReactCodegen/ReactCodegen.podspec
[Codegen] Generating Package.swift
[Codegen] Generated artifact: /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/build/generated/ios/Package.swift
[Codegen] Done.
Analyzing dependencies
Fetching podspec for `ExpoFileSystem` from `../node_modules/expo/node_modules/expo-file-system/ios/ExpoFileSystem.podspec`
Fetching podspec for `ExpoFont` from `../node_modules/expo/node_modules/expo-font/ios/ExpoFont.podspec`
Fetching podspec for `ExpoModulesCore` from `../node_modules/expo-modules-core/ExpoModulesCore.podspec`
Fetching podspec for `ExpoModulesWorklets` from `../node_modules/expo-modules-core/ExpoModulesWorklets.podspec`
Fetching podspec for `React-Core-prebuilt` from `../node_modules/react-native/React-Core-prebuilt.podspec`
[ReactNativeCore] Verifying checksum for cached reactnative-core-0.88.1-debug.tar.gz...
[Cache] SHA1 verified for reactnative-core-0.88.1-debug.tar.gz
[ReactNativeCore] Cache hit: copying reactnative-core-0.88.1-debug.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
[ReactNativeCore] Verifying checksum for cached reactnative-core-0.88.1-release.tar.gz...
[Cache] SHA1 verified for reactnative-core-0.88.1-release.tar.gz
[ReactNativeCore] Cache hit: copying reactnative-core-0.88.1-release.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
[ReactNativeCore] Resolved stable ReactNativeCore-prebuilt version:
[ReactNativeCore] ../../ios/Pods/ReactNativeCore-artifacts/reactnative-core-0.88.1-debug.tar.gz
[ReactNativeCore] ../../ios/Pods/ReactNativeCore-artifacts/reactnative-core-0.88.1-release.tar.gz
Fetching podspec for `ReactNativeDependencies` from `../node_modules/react-native/third-party-podspecs/ReactNativeDependencies.podspec`
[ReactNativeDependencies] Using tarball from URL: https://repo.reactnative.dev/maven2/com/facebook/react/react-native-artifacts/0.88.1/react-native-artifacts-0.88.1-reactnative-dependencies-debug.tar.gz
[ReactNativeDependencies] Tarball reactnative-dependencies-0.88.1-debug.tar.gz already exists in Pods. Skipping download.
[ReactNativeDependencies] Tarball reactnative-dependencies-0.88.1-release.tar.gz already exists in Pods. Skipping download.
Fetching podspec for `hermes-engine` from `../node_modules/react-native/sdks/hermes-engine/hermes-engine.podspec`
[Hermes] Using release tarball from URL: https://repo.reactnative.dev/maven2/com/facebook/hermes/hermes-ios/260318099.0.5/hermes-ios-260318099.0.5-hermes-ios-debug.tar.gz
[Hermes] Verifying checksum for cached hermes-ios-260318099.0.5-debug.tar.gz...
[Hermes] SHA1 verified for hermes-ios-260318099.0.5-debug.tar.gz
[Hermes] Cache hit: copying hermes-ios-260318099.0.5-debug.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
[Hermes] Verifying checksum for cached hermes-ios-260318099.0.5-release.tar.gz...
[Hermes] SHA1 verified for hermes-ios-260318099.0.5-release.tar.gz
[Hermes] Cache hit: copying hermes-ios-260318099.0.5-release.tar.gz from shared cache (/Users/geremyubaldo/Library/Caches/ReactNative)
Downloading dependencies
Installing DoubleConversion (1.1.6)
Installing EXConstants (58.0.15)
Installing Expo (58.0.23)
Installing ExpoAsset (58.0.20)
Installing ExpoDomWebView (58.0.2)
Installing ExpoFileSystem (58.0.13)
Installing ExpoFont (58.0.11)
Installing ExpoKeepAwake (58.0.3)
Installing ExpoLogBox (58.0.15)
Installing ExpoModulesCore (58.0.30)
Installing ExpoModulesJSI (58.0.22)
Installing ExpoModulesWorklets (58.0.30)
Installing ExpoStatusBar (58.0.4)
Installing FBLazyVector (0.88.1)
Installing RCT-Folly (2024.11.18.00)
Installing RCTDeprecation (0.88.1)
Installing RCTRequired (0.88.1)
Installing RCTSwiftUI (0.88.1)
Installing RCTSwiftUIWrapper (0.88.1)
Installing RCTTypeSafety (0.88.1)
Installing React (0.88.1)
Installing React-Core (0.88.1)
Installing React-Core-prebuilt (0.88.1)
Installing React-CoreModules (0.88.1)
Installing React-Fabric (0.88.1)
Installing React-FabricComponents (0.88.1)
Installing React-FabricImage (0.88.1)
Installing React-ImageManager (0.88.1)
Installing React-Mapbuffer (0.88.1)
Installing React-NativeModulesApple (0.88.1)
Installing React-RCTActionSheet (0.88.1)
Installing React-RCTAnimatedModuleProvider (0.88.1)
Installing React-RCTAnimation (0.88.1)
Installing React-RCTAppDelegate (0.88.1)
Installing React-RCTBlob (0.88.1)
Installing React-RCTFBReactNativeSpec (0.88.1)
Installing React-RCTFabric (0.88.1)
Installing React-RCTImage (0.88.1)
Installing React-RCTLinking (0.88.1)
Installing React-RCTNetwork (0.88.1)
Installing React-RCTRuntime (0.88.1)
Installing React-RCTSettings (0.88.1)
Installing React-RCTText (0.88.1)
Installing React-RCTVibration (0.88.1)
Installing React-RuntimeApple (0.88.1)
Installing React-RuntimeCore (0.88.1)
Installing React-RuntimeHermes (0.88.1)
Installing React-bridging (0.88.1)
Installing React-callinvoker (0.88.1)
Installing React-cxxreact (0.88.1)
Installing React-cxxstableapi (0.88.1)
Installing React-debug (0.88.1)
Installing React-defaultsnativemodule (0.88.1)
Installing React-domnativemodule (0.88.1)
Installing React-featureflags (0.88.1)
Installing React-featureflagsnativemodule (0.88.1)
Installing React-graphics (0.88.1)
Installing React-hermes (0.88.1)
Installing React-idlecallbacksnativemodule (0.88.1)
Installing React-intersectionobservernativemodule (0.88.1)
Installing React-jserrorhandler (0.88.1)
Installing React-jsi (0.88.1)
Installing React-jsiexecutor (0.88.1)
Installing React-jsinspector (0.88.1)
Installing React-jsinspectorcdp (0.88.1)
Installing React-jsinspectornetwork (0.88.1)
Installing React-jsinspectortracing (0.88.1)
Installing React-jsitooling (0.88.1)
Installing React-jsitracing (0.88.1)
Installing React-logger (0.88.1)
Installing React-microtasksnativemodule (0.88.1)
Installing React-mutationobservernativemodule (0.88.1)
Installing React-networking (0.88.1)
Installing React-oscompat (0.88.1)
Installing React-perflogger (0.88.1)
Installing React-performancecdpmetrics (0.88.1)
Installing React-performancetimeline (0.88.1)
Installing React-rendererconsistency (0.88.1)
Installing React-renderercss (0.88.1)
Installing React-rendererdebug (0.88.1)
Installing React-resizeobservernativemodule (0.88.1)
Installing React-runtimeexecutor (0.88.1)
Installing React-runtimescheduler (0.88.1)
Installing React-timing (0.88.1)
Installing React-utils (0.88.1)
Installing React-viewtransitionnativemodule (0.88.1)
Installing React-webperformancenativemodule (0.88.1)
Installing ReactAppDependencyProvider (0.88.1)
Installing ReactCodegen (0.88.1)
Installing ReactCommon (0.88.1)
Installing ReactNativeDependencies (0.88.1)
Installing SocketRocket (0.7.1)
Installing Yoga (0.0.0)
Installing boost (1.84.0)
Installing fast_float (8.0.0)
Installing fmt (12.1.0)
Installing glog (0.3.5)
Installing hermes-engine (260318099.0.5)
[Expo] Ensuring required slices in ExpoModulesJSI.xcframework
Generating Pods project
Setting USE_HERMES build settings
Setting REACT_NATIVE_PATH build settings
Setting SWIFT_ACTIVE_COMPILATION_CONDITIONS build settings
[Ccache]: Removing Ccache from CC, LD, CXX & LDPLUSPLUS build settings
Setting GCC_OPTIMIZATION_LEVEL to 2 for React Native pods in Release, and for Yoga, glog in all configurations
[ReactNativeCore] Configuring xcconfig for prebuilt React Native Core...
[ReactNativeCore] Prebuilt xcconfig configuration complete
[ReactNativeDependencies] Configuring xcconfig for prebuilt React Native Dependencies...
[ReactNativeDependencies] Prebuilt deps xcconfig configuration complete
[SPM] Cleaning old SPM dependencies from Pods project
[SPM] Adding SPM dependencies to Pods project
[Privacy Manifest Aggregation] Appending aggregated reasons to existing PrivacyInfo.xcprivacy file.
[Privacy Manifest Aggregation] Reading .xcprivacy files to aggregate all used Required Reason APIs.
Setting CLANG_CXX_LANGUAGE_STANDARD to c++20 on /Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/PersonalProfileApp.xcodeproj

==================== DEPRECATION NOTICE =====================
Calling `pod install` directly is deprecated in React Native
because we are moving away from Cocoapods toward alternative
solutions to build the project.

- If you are using Expo, please run:
  `npx expo run:ios`
- If you are using the Community CLI, please run:
  `yarn ios`
  =============================================================

Pod install took 25 [s] to run
Integrating client project
warning: The @ExpoModule class 'CoreModule' (/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/node_modules/expo-modules-core/ios/Core/Modules/CoreModule.swift) is internal, so the generated modules provider cannot reference it. Declare it public to link it automatically, or use a lower access level such as private to opt it out of linking.
Pod installation complete! There are 99 dependencies from the Podfile and 98 total pods installed.
[Expo-precompiled] Precompiled modules:
[Expo-precompiled] 📦 ExpoFileSystem (58.0.13)
[Expo-precompiled] 📦 ExpoFont (58.0.11)
[Expo-precompiled] 📦 ExpoModulesCore (58.0.30)
[Expo-precompiled] 📦 ExpoModulesWorklets (58.0.30)
[Expo] Disabling SWIFT_EMIT_MODULE_INTERFACE for pod targets (prebuilt React compatibility)
[Expo] Ensured modular React header flags on 0 xcconfig(s)
[Expo-precompiled] Looking for ExpoModulesCore.xcframework at:
/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/ios/Pods/ExpoModulesCore/ExpoModulesCore.xcframework
[Expo-precompiled] Adding ExpoModulesJSI header search paths to all targets
[Expo] Adding '[Expo] Remove duplicate codegen output' build phase to ReactCodegen

[!] ExpoFileSystem has added 2 script phases. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] ExpoFont has added 2 script phases. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] ExpoModulesCore has added 2 script phases. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] ExpoModulesWorklets has added 2 script phases. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] React-Core-prebuilt has added 1 script phase. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] ReactNativeDependencies has added 1 script phase. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.

[!] hermes-engine has added 1 script phase. Please inspect before executing a build. See `https://guides.cocoapods.org/syntax/podspec.html#script_phases` for more information.
› Planning build
› Executing react-native Pods/ReactNativeDependencies » [CP-User] [RNDeps] Replace React Native Dependencies for the right configuration, if needed
› Executing react-native Pods/ReactNativeDependencies » [CP] Copy XCFrameworks
› Preparing expo-constants Pods/EXConstants-EXConstants » ResourceBundle-EXConstants-EXConstants-Info.plist
› Executing react-native Pods/React-Core-prebuilt » [CP-User] [RNCore] Replace React Native Core for the right configuration, if needed
› Preparing Pods/EXConstants-ExpoConstants_privacy » ResourceBundle-ExpoConstants_privacy-EXConstants-Info.plist
› Executing react-native Pods/React-Core-prebuilt » [CP] Copy XCFrameworks
› Executing react-native Pods/hermes-engine » [CP-User] [Hermes] Replace Hermes for the right configuration, if needed
› Executing react-native Pods/hermes-engine » [CP] Copy XCFrameworks
› Preparing Pods/React-timing-React-timing_privacy » ResourceBundle-React-timing_privacy-React-timing-Info.plist
› Preparing Pods/React-cxxreact-React-cxxreact_privacy » ResourceBundle-React-cxxreact_privacy-React-cxxreact-Info.plist
› Executing expo-modules-jsi Pods/ExpoModulesJSI » [CP-User] Build ExpoModulesJSI xcframework
› Executing expo-modules-jsi Pods/ExpoModulesJSI » [CP] Copy XCFrameworks
› Executing react-native Pods/React-RCTFBReactNativeSpec » [CP-User] [RN]Check FBReactNativeSpec
› Executing personalprofileapp Pods/ReactCodegen » [Expo] Remove duplicate codegen output
› Compiling personalprofileapp Pods/ReactCodegen » RCTUnstableModulesRequiringMainQueueSetupProvider.mm
› Compiling personalprofileapp Pods/ReactCodegen » RCTThirdPartyComponentsProvider.mm
› Compiling personalprofileapp Pods/ReactCodegen » RCTModuleProviders.mm
› Compiling personalprofileapp Pods/ReactCodegen » RCTModulesConformingToProtocolsProvider.mm
› Compiling personalprofileapp Pods/ReactCodegen » ReactCodegen-dummy.m
› Packaging personalprofileapp Pods/ReactCodegen » libReactCodegen.a
› Executing expo-modules-core Pods/ExpoModulesCore » [CP-User] [Expo] Switch ExpoModulesCore XCFramework for build configuration
› Executing expo-modules-core Pods/ExpoModulesCore » [CP] Copy XCFrameworks
› Executing expo-constants Pods/EXConstants » [CP-User] Generate app.config for prebuilt Constants.manifest
› Compiling expo-constants Pods/EXConstants » EXConstants-dummy.m
› Compiling expo Pods/EXConstants » EXConstantsInstallationIdProvider.m
› Compiling expo Pods/EXConstants » EXConstantsService.m
› Packaging expo-constants Pods/EXConstants » libEXConstants.a
› Executing expo-constants Pods/EXConstants » Copy generated compatibility header
› Compiling personalprofileapp Pods/ReactAppDependencyProvider » RCTAppDependencyProvider.mm
› Compiling personalprofileapp Pods/ReactAppDependencyProvider » ReactAppDependencyProvider-dummy.m
› Packaging personalprofileapp Pods/ReactAppDependencyProvider » libReactAppDependencyProvider.a
› Compiling expo Pods/Expo » EXBundleConfiguration.mm
› Compiling expo Pods/Expo » ExpoReactNativeFactory.mm
› Compiling expo Pods/Expo » EXReactRootViewFactory.mm
› Compiling expo Pods/Expo » Expo-dummy.m
› Compiling expo Pods/Expo » EXLegacyAppDelegateWrapper.m
› Compiling expo Pods/Expo » EXAppDefinesLoader.m
› Compiling expo Pods/Expo » EXAppDelegatesLoader.m
› Packaging expo Pods/Expo » libExpo.a
› Executing expo Pods/Expo » Copy generated compatibility header
› Compiling expo-asset Pods/ExpoAsset » ExpoAsset-dummy.m
› Packaging expo-asset Pods/ExpoAsset » libExpoAsset.a
› Executing expo-asset Pods/ExpoAsset » Copy generated compatibility header
› Compiling @expo/dom-webview Pods/ExpoDomWebView » ExpoDomWebView-dummy.m
› Packaging @expo/dom-webview Pods/ExpoDomWebView » libExpoDomWebView.a
› Executing @expo/dom-webview Pods/ExpoDomWebView » Copy generated compatibility header
› Preparing Pods/ExpoFileSystem-ExpoFileSystem_privacy » ResourceBundle-ExpoFileSystem_privacy-ExpoFileSystem-Info.plist
› Executing expo-file-system Pods/ExpoFileSystem » [CP-User] [Expo] Switch ExpoFileSystem XCFramework for build configuration
› Executing expo-file-system Pods/ExpoFileSystem » [CP] Copy XCFrameworks
› Executing expo-font Pods/ExpoFont » [CP-User] [Expo] Switch ExpoFont XCFramework for build configuration
› Executing expo-font Pods/ExpoFont » [CP] Copy XCFrameworks
› Compiling expo-keep-awake Pods/ExpoKeepAwake » ExpoKeepAwake-dummy.m
› Packaging expo-keep-awake Pods/ExpoKeepAwake » libExpoKeepAwake.a
› Executing expo-keep-awake Pods/ExpoKeepAwake » Copy generated compatibility header
› Compiling expo Pods/ExpoLogBox » ExpoRedBoxSwap.mm
› Compiling @expo/log-box Pods/ExpoLogBox » ExpoLogBox-dummy.m
› Packaging @expo/log-box Pods/ExpoLogBox » libExpoLogBox.a
› Executing @expo/log-box Pods/ExpoLogBox » Copy generated compatibility header
› Executing expo-modules-core Pods/ExpoModulesWorklets » [CP-User] [Expo] Switch ExpoModulesWorklets XCFramework for build configuration
› Executing expo-modules-core Pods/ExpoModulesWorklets » [CP] Copy XCFrameworks
› Compiling expo-status-bar Pods/ExpoStatusBar » ExpoStatusBar-dummy.m
› Packaging expo-status-bar Pods/ExpoStatusBar » libExpoStatusBar.a
› Executing expo-status-bar Pods/ExpoStatusBar » Copy generated compatibility header
› Compiling Pods/Pods-PersonalProfileApp » Pods-PersonalProfileApp-dummy.m
› Packaging Pods/Pods-PersonalProfileApp » libPods-PersonalProfileApp.a
› Executing PersonalProfileApp » [CP] Check Pods Manifest.lock
› Executing PersonalProfileApp » [Expo] Configure project
The @ExpoModule class 'CoreModule' (/Users/geremyubaldo/Desktop/react-native-project/Project/PersonalProfileApp/node_modules/expo-modules-core/ios/Core/Modules/CoreModule.swift) is internal, so the generated modules provider cannot reference it. Declare it public to link it automatically, or use a lower access level such as private to opt it out of linking.
› Copying ./PrivacyInfo.xcprivacy ➜ ios/PersonalProfileApp/PrivacyInfo.xcprivacy
› Compiling PersonalProfileApp » PersonalProfileApp_vers.c
› Linking PersonalProfileApp » PersonalProfileApp.debug.dylib
› Linking PersonalProfileApp » PersonalProfileApp
› Executing PersonalProfileApp » Bundle React Native code and images
› Executing PersonalProfileApp » [CP] Copy Pods Resources
› Executing PersonalProfileApp » [CP] Embed Pods Frameworks
› Preparing PersonalProfileApp » Info.plist
› Generating debug PersonalProfileApp » PersonalProfileApp.app.dSYM
› Generating debug PersonalProfileApp » PersonalProfileApp.app.dSYM
› Signing PersonalProfileApp » PersonalProfileApp.debug.dylib
› Signing PersonalProfileApp » \_\_preview.dylib
› Signing PersonalProfileApp » PersonalProfileApp.app
› Build Succeeded
