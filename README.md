## Windows Developer Machine Setup For Mobile App Development

### Introduction
This document assumes you already have familiarity in using Windows, CLI, IDEs, Git(Hub), and other development tools.

### Install `chocolatey`
1. Follow the instruction here: https://chocolatey.org/install#individual
2. After following the installation instruction for Chololatey, close and reopen PowerShell as Administrator.

### Install applications
1. Run the following command in PowerShell: `choco install androidstudio vscode flutter dart-sdk -y`\
This will take some time depending on your internet connection.

### Initial setup in Android Studio
1. Launch Android Studio.
2. Follow through the initial setup process, let it choose the default option if you aren't unsure of what to do.
3. Install Flutter, Dart, and Kotlin plugins if they are not already installed.\
You should see `Welcome to Android Studio` screen at this point.

### Setting up GitHub integration
1. Go here https://github.com/settings/tokens \
Login GitHub and it will take you to the tokens setting.
2. Create a new token with the following scopes: `repo`, `workflow`, `read:org`, `gist`
3. Copy the newly generated token on your way out.

### Clone the project to Android Studio
1. Back to Android Studio, press `Get from VCS` > Switch to `GitHub` tab > Press `Use token...` > Paste the generated token > Press `Log in`.
You should be back to the `Get from Version Control` screen on the `GitHub` tab with lists of all repo you have access to.
2. Search for `evresi/app` and select it, then set your desired project directory, then press `Clone` \
Android Studio should be fetching the project from remote and setting it up locally.

### Setting up the newly created project
1. Navigate to file `lib/main.dart`, run `flutter pub get` as the IDE suggested on the popup.
2. At top right > Press `Device Manager` > Press `Create device` > Select `Pixel 3` > Download system image `S` > Finish \
Done!
