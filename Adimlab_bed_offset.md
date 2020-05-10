__Adimlab Gantry Pro - Fixing bed Offset__

There are problems caused by the home (0X, 0Y) position on this printer being offset from the front left corner of the bed. If objects are arranged on the slicer's bed they are not printed at exactly the same location on the printer's bed. The extruder is offset to the left by 3mm (3X) and forward by 12.5mm (12.5Y).

A second problem is that the extruder sometimes crashes into the left front bed glass clip during startup on its way to the first coordinate. This is caused by the direct route it takes from 0,0 to the start point.

This has been tested with Marlin 1.1.9 Rev 1.5.1A

This will:
- Allow the Cura and PrusaSlicer slicers to accurately layout object(s) on the bed even though the bed corner is not at 0X and 0Y.
- During startup, position the extruder out of the way of the left front bed glass clip so they doesn't collide.

I thank Mark Rehorst and his comprehensive article https://drmrehorst.blogspot.com/2017/08/setting-up-3d-printers-origin.html that clearly describes the problem. His solution is for another printer and I have modified it to suit the Gantry Pro. I added the extruder / clip guard.

The solutions are to use gcode to:
- Position the extruder at front left corner of bed and reset the printer coordinates to recognize this as 0,0,0
- Reposition the extruder down the bed so that when it travels to the first cordinate in the model it travels up the bed, ather than from 0,0 directly to the point, and possibly coliding with the clip.

For both Cura 4.6.x and PrusaSlicer 2.2.x, modify the printer settings and replace the startup gcode with the following:  
<pre>
; intialize
G21 ; set units to millimeter - (probably not needed)
G90 ; use absolute coordinates
G28 ; Home
; reset coordinates
G0 Z5 ; raise nozzle 5mm
G0 X3 Y12.5 Z5 ; go to left-front corner of bed
G92 X0 Y0 Z5 ; set printer's coordinates to (0,0,5)
G92 E0 ; set extruder to 0
; move the nozzle down the bed so it won't hit the clip
G0 X-3 Y100 ; get away from clips
; ready to go
</pre>

Be sure the bed size is set to 315,315. The printer's documentation says the build size is 310, 310 but the bed is larger. Once this gcode has been enabled, any layout in the slicer will exactly match the final position of the model on the printer bed.

The offset values of 3X and 12.5Y are based on  observation of my printer. If you think they need revision or fine tuning, just change them in your gcode.

If you have questions, comments or problems please open an issue on the github repository. https://github.com/CharlesGodwin/3DPrinting