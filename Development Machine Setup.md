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
- GitHub fine-grained personal access token with `Public repositories (read-only)` access.
    - Follow this section of the documentation (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token)
    - If you are a team member of OpenTourBuilder with write access, Your token must be setup this way instead:
        - `All repositories` access
        - Repository permissions with `Contents` set to `Read and write`
        - Resource owner is `opentourbuilder`

## MacBook Setup

Before you do anything else, login on the Mac through System Settings. This section assumes that you have an accessible administrator user account on the MacBook and is currently running MacOS 13 Ventura at the time of writing.

### Software Installation

- Install Homebrew
    - Follow this documentation (https://brew.sh/)

- Install Ruby
    - Follow this documentation (https://www.ruby-lang.org/en/documentation/installation/#homebrew)

- Install CocoaPods
    - Follow this documentation (https://guides.cocoapods.org/using/getting-started.html)

- Install Xcode
    - Follow this article (https://matteomanferdini.com/install-xcode/#xcode-app-store)

- Install Flutter SDK
    - Follow this documentation (https://docs.flutter.dev/get-started/install/macos)

- Install Visual Studio Code
    - Follow this documentation (https://code.visualstudio.com/docs/setup/mac)

- Install Android Studio
    - Follow this documentation (https://developer.android.com/studio/install#mac)

### Setup Git Repository

Open the terminal at a desired location and run these commands, line-by-line:

```
git init
git remote add origin https://<YOUR_FINEGRAINED_TOKEN_HERE>@github.com/<ORGANIZATION_OR_USERNAME>/<REPOSITORY>.git
git fetch
```

The repository is ready to use. Repeat this entire process for any additional repository that you want to clone. Note that you must read `README.md` for the repository for any additional setups.

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

