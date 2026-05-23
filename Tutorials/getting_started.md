# Getting Started with Termux

## Update Packages
It is recommended to update the packages to keep Termux up-to-date. To update the packages you can run this simple command:

* `pkg update && pkg upgrade`

This will keep the packages up to date and install updates to the existing/installed packages.

## Storage Access

Termux may need access to your internal storage to do actions properly, or browse files through the app. You can run the `termux-setup-storage` command to do that.

## Enabling Package Repositories

There's many things to install in Termux, while some of them are in different repositories. By default, the main package repository is enabled. However, you can enable the other package repositories:

* `pkg install x11-repo`: This will enable the repository of X11 (X Window System) packages, where you can install desktop environments, or desktop applications.

* `pkg install root-repo`: Enable this repository only if your device is rooted. It contains the packages/applications that require root permissions.

* `pkg install tur-repo`: This package repository is unofficial, but it contains various packages/applications that are not in Termux's official packages list. ([Learn more](https://github.com/termux-user-repository/tur))

[[Go back to the navigation]](https://github.com/GlitchBlake/Termux-Tutorials/blob/main/README.md)
