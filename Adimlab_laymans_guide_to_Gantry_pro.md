#
# A Layman&#39;s Guide to the Adimlabs Gantry Pro

# Introduction

I acquired an Adimlabs Gantry Pro 3D printer early in 2020. This document is a review of the lessons I have learned about setup and use of the machine. These are my opinions, and this is not meant to be a &quot;you must do it this way&quot; kind of document. Experienced users may disagree or have preferred alternatives. I welcome corrections where I have provided wrong, misleading, harmful, or incomplete information as well as suggestions for improvement..

# Accessories

I found these items especially useful for setup and regular use of the printer. Usage will be described later

- Small water spray bottle
- 2 micro-fibre cloths
- Small multi-Good #2 Philipstip screwdriver
- 7 mm socket or wrenchnut driver
- 10mm wrench
- 17mm wrench
- Many Gglue sticks for paper
- 30mm / 12&quot; metal ruler / straight edge
- Metric metal feeler gauges
- Scissors
- Small sharp knife or box cutter
- SLots of spare nozzles
- Tupperware food container or equivalent box for all the accessories

# Initial Setup

## All rollers and Eccentric Nuts

DYou should double check all roller assemblies on the printer before you use it. They can be too loose or too tight. There are five sets of rollers on the printer. These are assemblies with 3 or 4 rubber wheels straddling one of the black aluminum rails. There are two sets under the bed (table) supporting it, the bed, one on each vertical rail supporting the moving cross bar and one on the crossbar supporting the extruder unit. All the wheels should be &#39;snug&#39;. This, which means they should not be able to spin freely in place nor can they be so tight the assembly will not move when expected. Refer to the Assembly Manual and User Guide for guidance. The provided tool for tightening these nuts is small and hard to work with., I recommend you use a regular 10mm wrench (see my list of accessories). Search for &quot;eccentric nut&quot; while reading the supplied PDF files.

Here is what I did to get them all adjusted.

- With the power on, raise the crossbar up about 100+ mm using the control panel Prepare-\&gt; Move axis -\&gt; Z-axis -\&gt; 10mm -\&gt; rotate knob to +100. This will give you room to access all the adjustment bolts for the extruder and vertical assemblies.
- Switch off the printer. Now you can move the bed and extruder around easily.
- To adjust to correct amount, first loosen the nuts so the rubber wheels are running free. T, then, slowly, tighten the nut until each wheel can no longer turn. Do not tighten more than that or it will be too tight.
- Turn printer on its side to access the bearings under the bed,
- Straighten printer and adjust the three remaining assemblies.

## Drive Belt Tension

Refer to the Users Manual for location of the two drive belts. Each has a tensioner. Try to get these tight but not so tight as to stretch them.

## X-Axis Adjustment

The Owners manual, in Section 6(1), describes X-axis guide height adjustment. Follow the instructions to get this adjusted. But, after its adjusted, run the test a second time. This time you do not need to readjust the height, but you should check if the height of the X-Axis bar is the same at each end. You can use the ruler (accessory) to measure the height of the bar. If they are not the same height, then recheck the tension on the eccentric nuts for the bar. If they are not correctly tensioned, the bar will not position properly, and you will never be happy with your prints.

## Bed Flat

This is not bed levelling but a check if the bed is, in fact, flat, with no dips or bumps. As described earlier, raise the x-axis up 100mm to give you access to the bed. Using the foot long, or longer, steel ruler, place the edge of the ruler on the bed, stretching from to diagonal corners. The ruler&#39;s edge should lie flat on the glass with not light underneath and the ruler should not rock. Repeat the test for the other diagonal corners. If the bed is not completely flat, you should try to rectify the problem. In my case, I removed the clips holding the glass down and rotated the glass 90 degrees. This, somehow, reduced the dip I had in the centre of my glass. I think the clamps may have helped. I still had a slight dip in the centre, so I placed 3 small pieces of aluminum foil under the glass at the center of the bed. This helped raise the glass slightly in the middle. If you have convex shaped glass, I am not sure what solution you have. If you bed is not flat, you will never get perfect manual bed levelling. &quot;Close&quot; will work if you know where the imperfection is and avoid it if possible when printing.

Automatic &#39;bed levelling&#39; is the ideal solution as the a computer then adjust for all imperfections in flat.

# Routine Use

I have found that every time I print something, I should properly prepare my bed to ensure a good start to each print. Properly prepare is done in two steps. Any time I omit one of these steps I quickly regret it as my first layer does not go well and I must start over.

1. **Clean the bed and add fresh glue**
 There are many opinions on what the proper bed preparation is to use for printing. I am having success with using a glue stick on the bed. Every time I prepare the bed, I use a water bottle to wet the surface of the bed. I then wipe off all the previous glue. I have two cloths. One I always use for the initial wipe off and it quickly accumulates lots of glue, but I do not care. After I wipe off most of the glue, I wet the glass again and wipe the bed clean and dry with the second, less dirty, cloth. Wash Rinse and dry these cloths regularly. Then I add fresh glue. I use Elmer&#39;s or Amazon&#39;s paper glue stick to apply a complete layer of glue to the glass. I cover the entire surface running the stick up and down and then repeat with the stick running across. I clean and glue the bed when it is still cool and before heating.
2. **Bed levelling**
 I always, always, bed level each time. Anytime I get rushed and omit this step, I regret it. The Owners Manual, in section 6(2) describes the bed levelling procedure. I quickly found I could not get good, repeatable, results using paper, so I now use a mechanics feeler gauges. These are readily available in auto supply store and online. The gauges are made of steel so are easy to handle and provide repeatable results. I use a gauge with 0.05mm thickness. This is thin but adjusting so the extruder just drags as the gauge is moved under it gives me good results.
3. **Clogged nozzle**
Sooner or later, when least expected, you will get a clogged nozzle. The first signs are either a bad first layer with little or no filament or no filament coming out of the nozzle during a print. Keep spare nozzles on hand, they are cheap but important. Preheat the end (nozzle) to allow removing the nozzle. The old nozzle must be removed with a the end hot end, so preheat the end. The nozzle is removed with a 7mm wrench, although a 7mm socket is easier when installing the new nozzle. The end of the heater assembly must be held in place while loosening the nozzle. This requires a 17mm wrench.
4. **First layer**
If your first layer does not go down without any &#39;oops&#39; filament, or any filament sticking to itself, or filament lifting from the bed then you have a good chance of a good print. If not, stop and recheck your preparation and levelling. Nothing can correct a bad first layer.

# Enhancements

I have installed one significant enhancement and plan two others.

## OctoPrint

This is a computer-based web server for managing your printer. [Full information is here.](https://octoprint.org/) It allows management of most printer function using a browser interface from anywhere in your network. Many users implement the server on a Raspberry Pi and the organization markets all-in-one turnkey Pi systems for those who chose not to build their own system. I have installed a Pi based unit and it has significantly improved my access to the printer. The only time I use the printer&#39;s LCD screen and controls is when I am levelling the bed. I use OctoPrint interface with my slicer to directly download the gcode to the server. I can control start and stop and check job status using my browser. It also supports a camera interface so you can watch your printer from afar. I have no recommendation on which camera to use or how to mount it.

## Automatic Bed Levelling

Automatic bed leveling eliminates problems with adjusting for warped beds. The software examines multiple points on the bed and calculates the correct distance, in software, to set the height of the nozzle. This takes bed levelling out of your hands, so bed preparation gets much simpler/

At the time of writing this there was no packaged automatic bed leveller available although [Ray Shain](https://everybody3dprints.com/) is developing one and it is expected soon. I look forward to its availability as I will install bed leveling as soon as its available.

## Cabinet or Enclosure

May use a cabinet to enclose the entire printer to allow for a warm chamber for printing and noise reduction. I have found many designs but not that match my budget. The Gantry Pro is a big printer, so some quick solutions will not work.

# Conclusion

This is a summary of the hard lessons I learned. I have not discussed which slicer to use or print setting as I have had success with both Cura and Prusa Slicer. If you follow these setup guidelines, you will have a stable setup to use for experimenting until you can print the way you want to print. Do not give up, it took my over a month to get my routines in place to have repeatable, successful results.

May 7, 2020 Charles Godwin Page 3