# Introduction

This website holds the documentation for TourForge, an open source set of software that makes it easy to create custom tour guide apps. TourForge has two main components: the TourForge tour builder (often just referred to as TourForge) and the software library TourForge Guide.

The TourForge tour builder, located at <https://tourforge.github.io/builder/>, is a web application that provides a simple interface to build the tour data files that are used by TourForge Guide. A work-in-progress tutorial on how to use TourForge is available in our guide on [using the tour builder](using-tour-builder.md).

TourForge Guide is a Flutter library providing a baseline with the majority of features needed by a tour guide application. Although almost all of the work has already been done for you, building your app with the TourForge Guide library still requires some software engineering knowledge (or a lot of patience). You will need to [set up your development environment](development-environment.md) and follow the guide on [building an app](building-app.md).

# TourForge Baseline

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/tourforge/baseline/android.yml?branch=main&label=Android%20build&style=for-the-badge)](https://github.com/tourforge/baseline/actions/workflows/android.yml)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/tourforge/baseline/ios.yml?branch=main&label=iOS%20build&style=for-the-badge)](https://github.com/tourforge/baseline/actions/workflows/ios.yml)

TourForge Baseline is a rebrandable GPS-guided tour app for Android and iOS, built using Flutter. This repository holds the generic, unbranded code, packaged as a Flutter library. Create your own tour guide app by forking this repository and editing the starter code in the `app/` subdirectory.

You can also put your application code in a separate repository, which is the approach taken by TourForge's flagship [Florence Navigator](https://github.com/tourforge/florence-navigator) application. Technically, putting your application code into a separate repository loses the flexibility of being able to edit the internal code of TourForge Baseline, unless you also fork this repository and point to your copy in the `pubspec.yaml` file.

More info is available on our [documentation site](https://tourforge.github.io/).

## First-Time Development Setup

In order for the satellite imagery feature to work, you need to create a file under `app/assets/` called `tomtom.txt` and paste a TomTom API key into this file.

### Android-Specific Setup

Open a terminal in the project directory and run `flutter pub get`.

## Running the App on Physical Device

### iOS

With Xcode open, follow this documentation (https://developer.apple.com/documentation/xcode/running-your-app-in-simulator-or-on-a-device#Connect-real-devices-to-your-Mac).

### Android

- Connect the Android device to the development machine with an appropriate USB cable.
  - If this is the first time, tap `Allow` when you see the `Allow USB debugging?` box.
- Open the Android Studio terminal and run `flutter run`.

  ### iOS

Make sure to back to the first-time setup for iOS section (https://github.com/tourforge/guide?tab=readme-ov-file#ios-specific-setup) and consult on step 4 to copy `ios-arm64_x86_64-simulator` instead.
With Xcode open, follow this documentation (https://developer.apple.com/documentation/xcode/running-your-app-in-simulator-or-on-a-device#Configure-the-list-of-simulated-devices).

### Android

- Initialize your desired system image and device here (https://developer.android.com/studio/run/managing-avds).
  - If this is the first time, tap `Allow` when you see the `Allow USB debugging?` box.
- Open the Android Studio terminal and run `flutter run`.
- You may need to get the device ID, obtainable via command `flutter emulators`.
## Building Release Distributables

### iOS Archive Instructions

To build an app archive and upload to Apple, follow these sections at (https://developer.apple.com/documentation/xcode/distributing-your-app-for-beta-testing-and-releases#Create-an-archive-of-your-app):
- `Create an archive of your app`
    - If you are creating an archive for the first time, follow the temporary solution in the thread (https://github.com/CocoaPods/CocoaPods/issues/11808) to successfully archive the app, then restart Xcode. 
- `Select a method for distribution`
    - Select `TestFlight & App Store`; this will also upload the archive directly to Apple.

### Android Build Signed Bundle Instructions

When creating a signed release bundle for the first time, you must follow this documentation (https://docs.flutter.dev/deployment/android#create-an-upload-keystore). Take note on a couple of things:
1. You may need to install the JDK for the generating keystore command to work.
2. It is going to ask a couple of identifying questions, but it doesn't matter how you answer them.
3. Remember to save the password and the location for the keystore.
4. Insert the password and keystore location in the `key.properties` file and move the file into the `android/` directory.
5. You can now create a signed bundle by running the following command: `flutter build appbundle`.
6. The signed bundle can be found in `build/app/outputs/bundle/release/app.aab`.

You only need to do this once. After that, any time that you need to build new bundle, simply re-run the command `flutter build appbundle`. You may now upload this signed bundle to the Google Play Console.
