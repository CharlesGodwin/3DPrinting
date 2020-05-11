# __Adimlab Gantry Pro - Missing the Clip at Startup__

The extruder sometimes crashes into the left front bed glass clip during startup on its way to the first coordinate. This is caused by the direct route it takes from 0,0 to the start point which may be on the other side of the clip.

The solution is to reposition the extruder down the bed so that when it travels to the first cordinate in the model it travels up the bed, rather than from 0,0.


The following has been tested with a Gantry Pro using Marlin 1.1.9 Rev 1.5.1A firmware and using Cura 4.6.1 and PrusaSlicer 2.2.0. The gcode may work with other slicers, but has not been tested.

In the slicer's printer definition modify the printer start print settings and insert the following gcode command in Start G-code. It should be placed after any exisiting positioning code, such as G28.

`G0 X-3 Y100 ; get away from clips but allow extruder to drip off the bed`

This command will position the nozzle left of the bed and about a third of the way towards the back.

If you have questions, comments, enhancements or problems please open an issue on the [github repository](https://github.com/CharlesGodwin/3DPrinting).
