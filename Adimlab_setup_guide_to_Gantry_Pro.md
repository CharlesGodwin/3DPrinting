#
# How to Ensure All Axes are Properly Level on a ADIMlab Gantry Pro

# Introduction

I acquired an ADIMLab Gantry Pro 3D printer early in 2020. This document is a review of the lessons I have learned about setup and use of the machine. These are my opinions, and this is not meant to be a "you must do it this way" kind of document. Experienced users may disagree or have preferred alternatives. I welcome corrections where I have provided wrong, misleading, harmful, or incomplete information as well as suggestions for improvement..

# Accessories

I found these items especially useful for setup and regular use of the printer. Usage will be described later

- Small water spray bottle
- 2 micro-fibre cloths
- Good #2 Philips screwdriver
- 7 mm nut driver or wrench
- 10 mm wrench
- 17 mm wrench
- 30 mm / 12" metal ruler / straight edge
- Metric metal feeler gauges
- Scissors
- Small sharp knife or box cutter
- Spare nozzles
- Tupperware food container or equivalent box for all the accessories

# Initial Setup

## All rollers and Eccentric Nuts

You should double check all roller assemblies on the printer before you use it. They can be too loose or too tight. There are five sets of rollers on the printer. These are assemblies with 3 or 4 rubber wheels straddling one of the black aluminum rails. There are two sets under the bed (table) supporting it, the bed, one on each vertical rail supporting the moving cross bar and one on the crossbar supporting the extruder unit. All the wheels should be 'snug'. This means they should not be able to spin freely in place nor can they be so tight the assembly will not move when expected. Refer to the Assembly Manual and User Guide for guidance. The provided tool for tightening these nuts is small and hard to work with., I recommend you use a regular 10mm wrench (see my list of accessories). Search for "eccentric nut" while reading the supplied PDF files.

Here is what I did to get them all adjusted.

- With the power on, raise the crossbar up about 100+ mm using the control panel Prepare-> Move axis -> Z-axis -> 10mm -> rotate knob to +100. This will give you room to access all the adjustment bolts for the extruder and vertical assemblies.
- Switch off the printer. Now you can move the bed and extruder around easily.
- To adjust to correct amount, first loosen the nuts so the rubber wheels are running free. T, then, slowly, tighten the nut until each wheel can no longer turn. Do not tighten more than that or it will be too tight.
- Turn printer on its side to access the bearings under the bed,
- Straighten printer and adjust the three remaining assemblies.

## Drive Belt Tension

Refer to the Users Manual for location of the two drive belts. Each has a tensioner. Try to get these tight but not so tight as to stretch them.

## X-Axis Adjustment

The Owners manual, in Section 6 (1), describes X-axis guide height adjustment. Follow the instructions to get this adjusted. But, after its adjusted, run the test a second time. This time you do not need to readjust the height, but you should check if the height of the X-Axis bar is the same at each end. You can use the ruler (accessory) to measure the height of the bar. If they are not the same height, then recheck the tension on the eccentric nuts for the bar. If they are not correctly tensioned, the bar will not position properly, and you will never be happy with your prints.

## Bed Flat

This is not bed levelling but a check if the bed is, in fact, flat, with no dips or bumps. Experienced users tell me that there is no such thing as a completely flat bed in this type of machine, so we have to find out what we have and compensate. 

As described earlier, raise the x-axis up 100mm to give you access to the bed. Using the foot long, or longer, steel ruler, place the edge of the ruler on the bed, stretching between diagonal corners. The ruler's edge should lie flat on the glass with no light underneath and the ruler should not rock. Repeat the test for the other diagonal corners. If the bed is not completely flat, try to rectify the problem. In my case, I removed the clips holding the glass down and rotated the glass 90 degrees. This, somehow, reduced the dip I had in the centre of my glass. I think the clamps positions may have helped. I still had a slight dip in the centre, so I placed some small sheets of aluminum foil under the glass at the center of the bed. This helped raise the glass slightly in the middle. If you have convex shaped glass, I am not sure what solution you have. If your bed is not flat, you will never get perfect manual bed levelling. "Close" will work if you know where the imperfection is and avoid it, if possible, when printing.

Automatic 'bed levelling' is the better solution as the a computer then adjust for all imperfections in 'flat'.

# Routine Use

[Refer to the separate document](getting_a_good_first_layer.md) for help with print set up.
# Conclusion

This is a summary of the hard lessons I learned. I have not discussed which slicer to use or print setting as I have had success with both Cura and Prusa Slicer. If you follow these setup guidelines, you will have a stable setup to use for experimenting until you can print the way you want to print. Do not give up, it took my over a month to get my routines in place to have repeatable, successful results.
