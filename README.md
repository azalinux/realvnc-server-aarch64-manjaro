# realvnc-server-aarch64
Real VNC Server for Raspberry Pi4 64bit AARCH64

This AUR package will install Realvnc Server aarch64 package on any ArchLinux based ARM64 installation on a Raspberry Pi4.

Has been tested on all flavours of Manajaro ARM64 flavours using a 8gb Raspberry Pi 4b.  Has also been tried on XFCE, MATE & KDE Plasma desktop flavours.  This should work on any vanilla ArchLiux ARM64 install too!

BEFORE YOU INSTALL THIS PACKAGE:

Make sure you have the package base-devel installed fully.  For example, a default install of Manjaro Arch ARM64 only has some components of   base-devel   installed by default on a fresh installation so please perform the following command to ensure all prerequists for building the package are met:    pacman -S base-devel

Installation:

Either search for this package using an Arch AUR package manager like Pamac or Yay or git clone this package to compile manually:

git clone https://github.com/azalinux/realvnc-server-aarch64.git

makepkg

FYI:  You will need a vaild realvnc key - to activate run:   sudo /usr/bin/vnclicense -add

Don't forget to enable the systemd service:   sudo systemctl enable vncserver-x11-serviced.service

And thats it!  A working 64bit Real VNC server running on ArchLinux ARM64!


