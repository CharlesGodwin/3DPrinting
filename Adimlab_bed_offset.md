__Adimlab Gantry Pro - Fixing bed Offset__

There are problems caused by the home (0X, 0Y) position on this printer being offset from the front left corner of the bed. If objects are arranged on the slicer's bed they are not printed at the same location on the printer's bed. The extruder is offset to the left by approximately 3mm (3X) and forward by approximately 12.5mm (12.5Y). The offset values of 3X and 12.5Y for bed location 0,0 are based on observation of my printer. This value may vary per machine setup, based on calibration of stop switches. I recommend you check your machine by manually positioning the X axis and Y axis until nozzle is poitioned at the exact corner of the bed. Use the numbers displayed on the LCD Panel. 

A second problem is that the extruder sometimes crashes into the left front bed glass clip during startup on its way to the first coordinate. This is caused by the direct route it takes from 0,0 to the start point.

This has been tested with a Gantry Pro using Marlin 1.1.9 Rev 1.5.1A firmware and using Cura 4.6.1 and PrusaSlicer 2.2.0. The gcode may work with other slicers, but has not been tested.

This will:
- Allow the slicer to accurately layout object(s) on the bed even though the bed corner is not at 0X and 0Y.
- During startup, position the extruder out of the way of the left front bed glass clip so they doesn't collide.

I thank Mark Rehorst and his comprehensive article https://drmrehorst.blogspot.com/2017/08/setting-up-3d-printers-origin.html that clearly describes the problem. His solution is for another printer and I have modified it to suit the Gantry Pro. I added the extruder / clip guard.

The solutions are to use gcode to:
- Position the extruder at front left corner of bed and reset the printer coordinates to recognize this as 0,0,0
- Reposition the extruder down the bed so that when it travels to the first cordinate in the model it travels up the bed, rather than from 0,0 directly to the point, and possibly coliding with the clip.

For both Cura 4.6.x and PrusaSlicer 2.2.x, modify the printer settings and replace the startup gcode with the following:  
<pre>
; intialize
G90 ; use absolute coordinates
G28 ; Home
; reset coordinates
G0 Z5 ; raise nozzle 5mm
G0 X3 Y12.5 Z5 ; go to left-front corner of bed ** check these values **
G92 X0 Y0 Z5 ; set printer's coordinates to (0,0,5)
G92 E0 ; set extruder to 0
; move the nozzle down the bed so it won't hit the clip - this is optional
G0 X-3 Y100 ; get away from clips and allow extruder to drip off the bed
; ready to go
</pre>

Be sure the bed size is set to 315,315. The printer's documentation says the build size is 310, 310 but the bed is larger. Once this gcode has been enabled, any layout in the slicer will match the final position of the model on the printer bed.

__NOTES:__ 
- The default Adimlab firmware does not enable INCH_MODE_SUPPORT so G21 to set metric is not neccesary.
- Y_MAX_POS, the furthest the extruder can go on the bed in Y axis, is set to 320. Since the home position is -12.5, the maximum Y axis  ON THE BED for a build is 307.5 (320 - 12.5). This is a little short of the declared 310 but will probably never interfere with a print.

If you have questions, comments, ehnancements or problems please open an issue on the github repository. https://github.com/CharlesGodwin/3DPrinting
