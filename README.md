ANT-FS Client
=============

This program extracts all activity FIT files from a device and writes them
to a folder (see file locations below). The first time it runs it attempts
to sync with the watch. This produces an authfile which is written to the
same folder. On startup this program will try to read that file to avoid
having to re-sync.

Requirements
------------

- [openant >= 0.2](https://github.com/Tigge/openant)

Usage
-----

    Usage: antfs-cli.py [options]

    Options:
      -h, --help  show this help message and exit
      --upload    enable uploading
      --debug     enable debug


File locations
--------------

### Simple answer (probably correct for most people)

Your files are placed in ~/.config/antfs-cli/

### Long answer

FIT files and authfiles are stored in an the location specified by the XDG
Base Directory specification. It uses the $XDG_CONFIG_HOME with
$HOME/.config as backup. In this directory a antfs-cli folder is created
in which a folder for each device is created. Both the .FIT files and
authfile are stored in this device-specific folder.

Supported devices
-----------------

Any device supported by [openant](https://github.com/Tigge/openant) should work.

### ANT USB Sticks

 - [ANTUSB2 Stick](http://www.thisisant.com/developer/components/antusb2/)
 (0fcf:1008: Dynastream Innovations, Inc.)
 - [ANTUSB-m Stick](http://www.thisisant.com/developer/components/antusb-m/)
 (0fcf:1009: Dynastream Innovations, Inc.)

### ANT-FS Devices

Any compliant ANT-FS device should in theory work, but those specific devices have been reported as working:

 - Garmin Forerunner 60
 - Garmin Forerunner 405CX
 - Garmin Forerunner 310XT
 - Garmin Forerunner 610
 - Garmin Forerunner 910XT
 - Garmin FR70
 - Garmin Swim

Please let me know if you have any success with devices that are not listed here.