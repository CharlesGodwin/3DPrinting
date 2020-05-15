# Guide to 3D Slicers for ADIMLab Gantry Pro

This references the ADIMLab Gantry Pro and files included on an SD card shipped with the printer. However the information may be useful to others too.

## What's a Slicer?
3D printing is the act (art?) of turning a 3 dimensional drawing into a 3D solid object. Most hobby 3D printers use FDM (Fused Deposition Modelling). Simply put it constructs objects by 'printing' one layer of melted plastic filament at a time, building the object. Slicer software is the translation process from a 3D drawing to the data needed to print the object. Input to the program is a 3D drawing file and output is gcode. Gcode is a protocol developed for Computer Numerical Control (CNC) machines. It has been adapted to control 3D printers.These commands, most starting with G, tell the printer, in very simple terms, what to do. Do a web search for 'gcode' to find innumerable articles on the inner workings of gcode. ;)

First you must pick something to print. The SD Card shipped with the Gantry Pro has a directory named `12.Test model`. It contains files with an extension of  `.stl`. These are drawings you can use with slicer programs. [Here is definition of .stl files](https://en.wikipedia.org/wiki/STL_(file_format))

If you need more choices, try [Thingiverse](https://www.thingiverse.com/). There are other repositories of drawings.

## Choices
There are many slicer programs available. These are two popular GUI based products. Both are free and available for Windows, Mac OS and many Linux desktops. These two slicers provide what is needed to print 3D models. 

1. __Cura__
Known formally as Ultimaker-Cura, this is published by [Ultimaker](https://ultimaker.com/software/ultimaker-cura), the makers of the Ultimaker brand of 3D printers. 
2. __PrusaSlicer__
This is published by [Prusa3D](https://www.prusa3d.com/prusaslicer/), the makers of the Prusa brand of 3D printers.

Like most software, the choice of slicer program is very subjective and everyone has their favourite.

This is the process:
- Start your favourite slicer program
- Select or setup the type of printer
- Select the type of filament you are using
- Load a drawing (.stl file)
- Position it on the bed if needed
- Set print preferences
- Slice the object
- Transfer the gcode to the printer
- Start printing
- Wait....wait... ;)

The steps preceding 'Transfer the gcode to the printer'  are always the same. But the slicers can be set up to treat 'transfer' different ways.
- SD card
  - transfer gcode to card
  - eject
  - carry to printer
  - insert in printer
  - select file 
  - start printing
- Connect PC to Printer
  - Print via USB (Only available in Cura)
  - PrusaSlicer has an interface with PronterFace but its use is beyond the scope of this document.
- Connect PC to OctoPrint
  - Print via OctoPrint

The transfer to SD card is, technically, the simplest solution nd reduces investment in more technology. Connecting the printer to a PC is possible, but not recommended for printer use as the PC must stay on for the duration of the print. Any interruption would terminate the print prematurely. The simplest solution is to forward gcode to OctoPrint server for processing. This frees you PC for other activities or shut down.

[Refer to this document for details about OctoPrint](connecting_pc_to_3dprinter.md).

