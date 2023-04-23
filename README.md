# realvnc-server-aarch64-manjaro
RealVNC Server for Raspberry Pi4 64bit Manjaro AARCH64

This AUR package will install RealVNC Server aarch64 package on any Manjaro ArchLinux based ARM64 installation on a Raspberry Pi4.

Has been tested on all flavours of Manajaro ARM64 flavours using a 8gb Raspberry Pi 4b.  Has also been tried on XFCE, MATE & KDE Plasma desktop flavours.

BEFORE YOU INSTALL THIS PACKAGE:

***For verions 7+, I highly recommend you install this manually via cloning the GIT repo [instructions below] - only use the binary package if you DON"T have RealVNC installed!***

***Warning - Version 7 does NOT accept Version 6 Offline 25 number enterprise keys!***

***I highly recommend you perform a full system update before installing this on Manjaro so that it has the latest kernel installed (5.15+ and latest list of updated packages installed also.***   
```
$ sudo pacman -Syu
```
Make sure you have the package base-devel installed fully.  For example, a default install of Manjaro Arch ARM64 only has some components of   base-devel   installed by default on a fresh installation so please perform the following command to ensure all prerequists for building the package are met:    
```
$ sudo pacman -S base-devel
```
Installation:

You can use the precompiled package in my Releases page to download & install:
```
$ wget https://github.com/azalinux/realvnc-server-aarch64-manjaro/releases/download/v7.1.0/realvnc-vnc-server-7.1.0-1-aarch64.pkg.tar.zst
$ sudo pacman -U realvnc-vnc-server-7.1.0-1-aarch64.pkg.tar.zst
```
OR git clone this package to compile manually:
```
$ git clone https://github.com/azalinux/realvnc-server-aarch64-manjaro.git
$ makepkg -si
```
FYI:  This should be pre-activated as the source is pre-activated for use with Raspberry Pi's however if it doesn't show a valid license after installation, you will need a valid realvnc key;  to activate run:   
```
$ sudo /usr/bin/vnclicense -add
```
Don't forget to enable the systemd service:   
```
$ sudo systemctl enable vncserver-x11-serviced
$ sudo systemctl start vncserver-x11-serviced
```
And thats it!  A working 64bit RealVNC server running on Manjaro ArchLinux ARM64!

**Please note - This free Raspberry Pi edition of RealVnc Server will let clients connect via TCP direct mode rather than UDP direct mode. You need an Enterprise License to connect via UDP!**
