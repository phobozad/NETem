# NETem - Network Link Emulator for GNS3

NETem emulates a network link, typically a WAN link.
It supports bandwidth limitation, delay, jitter and packet loss.
All this functionality is already build in the linux kernel,
NETem is just a menu system to make the configuration user-friendly.

For more informations see <http://www.bernhard-ehlers.de/projects/netem/index.html>.


## Building the image

The image is downloadable from the GitHub releases area.

If you want to build it yourself, you need a linux system and install
packer (https://www.packer.io) and qemu.

Then build the image with
```
rm -rf output-qemu
packer build NETem.json
```

