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
- Glue sticks for paper
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

I have found that every time I print something, I should properly prepare my bed to ensure a good start to each print. Properly prepare is done in two steps. Any time I omit one of these steps I quickly regret it as my first layer does not go well and I must start over.

1. **Prepare the Bed**
There are many opinions on what the proper bed preparation is for printing. I am having success with using a glue stick on the bed. A separate article, describing alternatives, is being prepared. For now, this describes what has worked for me.
__Clean the bed and apply fresh glue__
Every time I prepare the bed, I use a water bottle to wet the surface of the bed.
__Be careful to not spray any electronics or wiring.__
I then wipe off all the previous glue. I have two cloths. One I always use for the initial wipe off and it quickly accumulates lots of glue, but I do not care. After I wipe off most of the glue, I wet the glass again and wipe the bed clean and dry with the second, less dirty, cloth. Rinse and dry these cloths regularly. Then I apply fresh glue. I use an Elmer's Purple dissolvable paper glue stick to apply a complete layer of glue to the glass. I cover the entire surface running the stick up and down and then repeat with the stick running across. I clean and glue the bed when it is still cool and before heating.

2. **Bed levelling**
I always, always, bed level each time. Any time I get rushed and omit this step, I regret it. The Owners Manual, in section 6 (2), describes the bed levelling procedure. I quickly found I could not get good, repeatable, results using paper as a thickness guide, so I now use a mechanics feeler gauge. These are readily available in auto supply stores, hardware stores and online. The gauges are made of steel so are easy to handle and provide repeatable results. I use a gauge with 0.05mm thickness. This is thin but adjusting so the extruder just drags as the gauge is moved under it gives me good results.

3. **Clogged nozzle**
Sooner or later, when least expected, you will get a clogged nozzle. The first signs are either a bad first layer with little or no filament or no filament coming out of the nozzle during a print. Keep spare nozzles on hand, they are cheap but important. Preheat the end (nozzle) to allow removing the nozzle. The old nozzle must be removed when it is hot, so preheat the end. The nozzle is removed with a 7mm nut driver or 7mm wrench. The nut driver is easier to use when installing the new nozzle. The end of the heater assembly must be held in place while loosening and tightening the nozzle. This requires a 17mm wrench.
4. **First layer**
If your first layer does not go down without any 'oops' filament, or any filament sticking to itself, or filament lifting from the bed then you have a good chance of a good print. If not, stop and recheck your preparation and levelling. _Nothing can correct a bad first layer_.

# Conclusion

This is a summary of the hard lessons I learned. I have not discussed which slicer to use or print setting as I have had success with both Cura and Prusa Slicer. If you follow these setup guidelines, you will have a stable setup to use for experimenting until you can print the way you want to print. Do not give up, it took my over a month to get my routines in place to have repeatable, successful results.
