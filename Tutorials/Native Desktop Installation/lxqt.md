# Termux Desktop Installation Guide - LXQt
To install a native LXQt desktop on your Termux, follow these steps:

## Package Installation
1. Update the Termux packages
```
pkg update && pkg upgrade
```
3. Install the LXQt desktop
```
pkg install lxqt
```
   * The installation may take a bit long, since there are many packages to install.
   * Make sure you have enabled the X11 repository. If you didn't, read [this](https://github.com/GlitchBlake/Termux-Tutorials/blob/main/Tutorials/Getting%20Started/termux_basics.md).

## Display Setup

### X11
1. Before proceeding everything below, install [Termux:X11 application](https://github.com/termux/termux-x11)
