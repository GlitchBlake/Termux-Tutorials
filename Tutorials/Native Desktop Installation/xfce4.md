# Termux Desktop Installation Guide - XFCE4
To install a native XFCE4 desktop on your Termux, follow these steps:

## Package Installation
1. Update the Termux packages: `pkg update && pkg upgrade`
2. Install the XFCE4 desktop with additional applications: `pkg install xfce4 xfce4-goodies xfce4-terminal`
   * The installation may take a bit long, since there are many packages to install.
   * Make sure you have enabled the X11 repository. If you didn't, read [this](https://github.com/GlitchBlake/Termux-Tutorials/blob/main/Tutorials/Getting%20Started/termux_basics.md).

## Display Setup

### X11
1. Before proceeding everything below, install [Termux:X11 application](https://github.com/termux/termux-x11)
2. Install the essential packages: `pkg install pulseaudio termux-x11-nightly dbus`
