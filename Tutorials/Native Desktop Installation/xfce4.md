# Termux Desktop Installation Guide - XFCE4
To install a native XFCE4 desktop on your Termux, follow these steps:

## Package Installation
1. Update the Termux packages
```
pkg update && pkg upgrade
```
3. Install the XFCE4 desktop with additional applications
```
pkg install xfce4 xfce4-goodies xfce4-terminal
```
   * The installation may take a bit long, since there are many packages to install.
   * Make sure you have enabled the X11 repository. If you didn't, read [this](https://github.com/GlitchBlake/Termux-Tutorials/blob/main/Tutorials/Getting%20Started/termux_basics.md).

## Display Setup

### X11
1. Before proceeding everything below, install [Termux:X11 application](https://github.com/termux/termux-x11)
2. Install the essential packages
```
pkg install pulseaudio termux-x11-nightly
```
3. Start the PulseAudio server
```
pulseaudio --start --load="module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" --exit-idle-time=-1
```
4. Set the required environment variables
```
export PULSE_SERVER=127.0.0.1
export DISPLAY=:0
export XDG_RUNTIME_DIR=$TMPDIR
```
5. Start the X11 server along with the XFCE4 desktop
```
termux-x11 -xstartup xfce4-session
```
Now check Termux:X11 application to see your desktop!

### VNC
1. Install a VNC application to your phone before proceeding.
2. Install the essential packages
```
pkg install tigervnc dbus
```
3. Set up the VNC password
```
vncpasswd
```
4. Create/edit the VNC startup script
```
nano ~/.vnc/xstartup
```
5. Paste the following in it:
```
dbus-launch --exit-with-session xfce4-session
```
6. Start the VNC server
```
vncserver
```
Finally, check your VNC viewer application and enjoy your desktop!
