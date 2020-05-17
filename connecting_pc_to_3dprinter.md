# Connecting a PC to a 3D Printer

## Introduction
This has been written about the ADIMLab Gantry Pro but could be applicable to most printers using Marlin firmware.

The printer comes with an SD card slot and the process to print a model is:
- create a gcode file using slicer software,
- copy it to an SD card,
- eject the SD card from the computer,
- insert it into the printer,
- select the file using the printer's LCD screen and
- then select print. 
  
This can get tedious very quickly.

It is also impossible to pass any configuration settings to the printer except by using the LCD panel. This can be slow at best and, in many cases, impossible to do.

This article refers to a 'PC' but this means any personal computer, laptop or even a [Raspberry Pi](https://www.raspberrypi.org/). Operating system can be Windows, Mac OS or various versions of Linux.

If all you want to do is have straight forward printing directly from your PC, then [slicer programs](beginners_guide_to_slicers.md) can be connected directly to the printer.

If you want to use advanced features to send and receive information using g-codes you will need a program that can act as terminal to communicate with the printer. The two discussed are:

### [PronterFace](https://www.pronterface.com/)
This program is bundled as an install time option as part of PrusaSlicer. It can also be downloaded from its site. It allows you to replicate most of the functionality of the printers LCD panel but also supplies a terminal interface to directly send G codes to the printer.

### [OctoPrint/OctoPi](https://octoprint.org/)
This is highly recommended. This software runs, connected to the printer, as a web based interface. You connect a computer to the printer, install OctoPrint, and can access the printer interface from anywhere in your home network using any browser. I have, like many users of thi class of 3D printer, have installed this software using a small, cheap, Raspberry Pi computer. If you don't want to set up a system yourself, the OctoPrint site offers vendors who will sell you a turnkey Raspberry Pi plug-n-play system. This was my first enhancement.
  
## The Connection

The connector on the printer is a [USB 2.0 Type-B connector](https://en.wikipedia.org/wiki/USB_hardware#Connectors). The printer is shipped with a Type-A / Type-B cable that will work for most PCs and a Raspberry Pi. both software packages perform automatic port detection and selection.
