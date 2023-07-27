# Development Machine Setup

## Prerequisite

It is highly recommended to have the following devices to develop and deploy your own OpenTourBuilder instances on both iOS and Android:
- MacBook
- iPhone
- Android

You need the following registered accounts:
- Apple ID
    - You should only use exactly one account for both the MacBook and iPhone setup
- Google Account
- GitHub

Additionally, completing and having these following items handy will speed up the setup process:
- GitHub fine-grained personal access token with `All repositories` access and repository permission `Contents` to `Read and write`
    - Follow this section of the documentation (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token)
    - If you are a team member of OpenTourBuilder with write access, make sure the resource owner is OpenTourBuilder

## MacBook Setup

Before you do anything else, login on the Mac through System Settings. This section assumes that you have an accessible administrator user account on the MacBook and is currently running MacOS 13 Ventura at the time of writing.

### Software Installation

- Install Xcode
    - Follow this article (https://matteomanferdini.com/install-xcode/#xcode-app-store)

- Install Visual Studio Code
    - Follow this documentation (https://code.visualstudio.com/docs/setup/mac)

- Install Android Studio
    - Follow this documentation (https://developer.android.com/studio/install#mac)

- Install Flutter SDK
    - Follow this documentation (https://docs.flutter.dev/get-started/install/macos)

### Setup Git Repository

Open the terminal at a desired location and run these commands:
- `git init`
- `git remote add origin https://<YOUR_FINEGRAINED_TOKEN_HERE>@github.com/<ORGANIZATION_OR_USERNAME>/<REPOSITORY>.git`
- `git fetch`
- `git checkout main`

The repository is ready to use, this will also grant write access if it exists on your account. Repeat this entire process for any additional repository that you want to clone.

## iPhone Setup

Complete the following steps:
- Login using a preferred Apple ID
- Enable developer mode
    - Follow this documentation (https://developer.apple.com/documentation/xcode/enabling-developer-mode-on-a-device)

## Android Setup

Complete the following steps:
- Login using a preferred Google account
- Enable developer options and then enable USB debugging
    - Follow the top portion of this documentation (https://developer.android.com/studio/debug/dev-options)

