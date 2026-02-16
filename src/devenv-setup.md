# Development Environment Setup (aarch64-darwin)
This guide outlines the core steps to initialize a development environment on Apple Silicon.

## Required

* **VS Code:** Install via direct download. Instruction found online.
* **Homebrew:** Install via the official shell script. Instruction found online.
* **Nix Package Manager:** Install the Nix package manager. Instruction found online.
* **Xcode IDE:** Installation options available either directly within Apple App Store. Alternatively, try the `xcodes` tool, which should be available for use in devenv setup. This may be necessary if you are on older Intel Mac who cannot get the latest Xcode.
* **Xcode Command Line Tools:** Run in the terminal
```bash
xcode-select --install
```

### Nix Configuration
Edit with sudo `/etc/nix/nix.conf` to enable experimental features and trust your local user. To find your current macOS username, run:
```bash
whoami
```

Add these lines to the configuration file (replacing `$MAC_USERNAME` with your actual username):
```text
experimental-features = nix-command flakes
trusted-users = root $MAC_USERNAME
```

### Add Packages
Install the primary CLI toolset via `nix profile`:
```bash
nix profile install nixpkgs#git nixpkgs#direnv nixpkgs#devenv nixpkgs#tree
```

## Project Workflow
To initialize a project environment (devenv supported environment only):

**Clone** the desired repository.
**Enter environment:** Do the following while you are in the project root directory.
* Run `devenv shell` manually, or
* Run `direnv allow` to automatically load the `.envrc` configuration upon entering the directory.

## Optional Enhancements

### Nix Package Registry Customization
If you need to use **unfree packages** (i.e. proprietary software), run this command once to update your registry:
```bash
nix registry add nixpkgs github:numtide/nixpkgs-unfree/nixos-unstable
```

### Applications & Shell

**iTerm2:** Install as a terminal emulator replacement. Generally nicer than MacOS system terminal. Instruction found online.
**Zsh Plugins:** Enhance your zsh shell with `zsh-autosuggestions`, `zsh-completions`, and `zsh-syntax-highlighting`. Installable via homebrew.
