# NETem - Network Link Emulator for GNS3

NETem emulates a network link, typically a WAN link.
It supports bandwidth limitation, delay, jitter and packet loss.
All this functionality is already build in the linux kernel,
NETem is just a menu system to make the configuration user-friendly.

For more informations see <http://www.bernhard-ehlers.de/projects/netem/index.html>.


## Building the image

The image is downloadable from the releases area.

If you want to build it yourself, you need a linux system and install
packer (https://www.packer.io) and qemu.

Then build the image with
```
packer build NETem.json
```

## PCEngines device fork
This fork modifies the project to support PCEngines ALIX and APU boards.  This repo is a fork of Bernhard Ehlers work (https://git.bernhard-ehlers.de/ehlers/NETem) modified to boot & run on a physical system rather than a GNS3 VM.

Currently, there is an issue booting from internal SD Card on PCEngines APU boards & these must boot from a USB flashdrive.  ALIX boards boot OK from internal CompactFlash.

The image is hard-coded to use 115200 baud on ttyS0.  Low baud rates (e.g. 9600) make the menu system very slow to draw and make it painful to use.
