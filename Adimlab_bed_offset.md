# __Adimlab Gantry Pro - Fixing bed Offset__

There can be confusion caused by the home (0X, 0Y, 0Z) position on this printer being offset from the front left corner of the bed. This causes objects  arranged on the slicer's bed to not be printed at the same location on the printer's bed. The extruder is offset to the left by approximately 5mm (5X) and forward by approximately 15mm (15Y). 

The following has been tested with a Gantry Pro using Marlin 1.1.9 Rev 1.5.1A firmware and using Cura 4.6.1 and PrusaSlicer 2.2.0. The gcode may work with other slicers, but has not been tested.

I thank Mark Rehorst and his [comprehensive article](https://drmrehorst.blogspot.com/2017/08/setting-up-3d-printers-origin.html) that describes the problem. His solution is for another brand of printer and I have modified it to suit the Gantry Pro.

## __Determining the offset__

** The offset values of X5.00 and Y15.00 for bed location 0,0 are based on observation of my printer. This set of values varies per machine setup, based on calibration of stop switches. These values are probably 'good enough', as one or two millimetres is not significant, you *can* check your machine for the values to use:
- Using the LCD panel, manually position the three axis to the left corner of the bed.
- First set the Z axis to 2, so the nozzle is close to the bed but not touching.
- Then move the Y and Z axis until you think the nozzle is positioned at the front left corner of the bed. Start with a value of Y15.00 and X5.00. You don't need to be precise, just as close as you want. No one will notice one or two millimetres.
- Record the X and Y coordinates as you move the extruder.

The first set of [instructions](#using-embedded-gcode) describe how to reset the bed corner location using gcode inserted into each print by your slicer. There is also an [alternative solution](#modifying-the-firmware) that modifies the printer's firmware instead. Use one solution or the other, DO NOT use both.

Please review the [notes](#notes) at the end.

## __Using embedded gcode__

The following change will allow a slicer to accurately layout object(s) on the bed, even though the bed corner is not at 0X and 0Y, by positioning the extruder at front left corner of bed and reset the printer coordinates to recognize this as 0,0

In the slicer's printer definition modify the printer settings and replace the Start G-code with the following:  
<pre>
; initialize
G90 ; use absolute coordinates
G28 ; Home
; reset coordinates
G0 Z5.00 ; raise nozzle 5mm
; ** USE YOUR OWN VALUES **
G0 X5.00 Y15.00 Z5.00 ; go to left-front corner of bed 
G92 X0 Y0 Z5 ; set printer's coordinates to (0,0,5)
G92 E0 ; set extruder to 0
</pre>
Please review the [notes](#notes) at the end.

## __Modifying the firmware__
Scott Thomas, in the [ADIMLab Facebook group](https://www.facebook.com/groups/1235236596606278/), identified a way to make the change permanent in printer's firmware. Once complete, the settings are permanent in firmware and do not depend on slicer settings. 
However, in order to do this, you must have software that can send gcode directly to the printer via its serial USB port.  [Read this document for information on relevant software](connecting_pc_to_3dprinter.md):


Perform these gcode steps:

- Get the current settings by sending M503  
`M503`
- This will return a list of the current firmware settings. Look for the text `Home offset:`, the next line should be `M206 X0.00 Y0.00 Z0.00`
- Send a M206 command using the X and Y numbers calculated [here](#determining-the-offset)  
`M206 X-5.00 Y-15.00 Z0.00`
- Resend `M503` to confirm the new `Home offset:` value
- Save it to memory by sending  
`M500`
- Turn off the printer __AND__ disconnect the USB to prevent it powering the motherboard. 
- Turn on the printer and reconnect the USB.
- Resend `M503` to confirm the new `Home offset:` value.

__The LCD panel will display `X -5 Y -15 Z 0` when you home the printer.__

## __NOTES:__
- Leave the bed size at 315, 315. The printer's documentation says the build size is 310, 310 but the bed is larger. Once this gcode has been enabled, any layout in the slicer will closely match the position of the model on the printer bed.
- The furthest the extruder can go on the bed, in the Y axis, is restricted by the physical limits of the bed belt and pulley system. On my machine the best I can do is 320 mm from the home position, which is about 5 mm short of the rear edge of the bed. Since the home position is set at -15, the maximum Y axis ON THE BED for a build is 305.00 (320 - 15). This is a little short of the declared 310 but will probably never interfere with a print. Your performance may vary.
- The problem with the extruder sometimes crashing into the left front bed glass clip during startup, on its way to the first coordinate is discussed [here](Adimlab_miss_the_clip.md). 

If you have questions, comments, enhancements or problems please open an issue on the [github repository](https://github.com/CharlesGodwin/3DPrinting).
