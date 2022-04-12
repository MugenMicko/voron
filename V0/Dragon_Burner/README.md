# Dragon Burner

This is my take on the Voron V0.1 toolhead. I wanted to improve the cooling of the Dragon HF hotend and provide improved part cooling when printing filament that needs it (e.g. PLA).

It is based on the [MiniAfterSherpa](https://github.com/KurioHonoo/Mini-AfterSherpa), but I've designed it anew from the ground up.

Goals:

- Dragon HF hotend support
- Single 3010 24v hotend cooling fan
- Twin 4010 24v blower part cooling fans
- Support for the [SlideSwipe magnetic probe](https://github.com/chestwood96/SlideSwipe)
- ADXL345 mount point

These have all been implemented in this public release.

Additional Goals:

- Learn Fusion 360 so I can publish decent source CAD files (I've a way to go on this one, this work was done on TinkerCad)
- Add support for other hotends
- Add support for other Klicky variants

Printing: Use the Voron defaults and print in ABS or better. The part is orientated correctly in the STL.

BOM:

In addition to the [MiniAfterSherpa](https://github.com/KurioHonoo/Mini-AfterSherpa) and the [SlideSwipe magnetic probe](https://github.com/chestwood96/SlideSwipe):

- 2x additional heat inserts for the ADXL345 mount
- 2x M3x12mm BHCS
- 2x M2x10mm self tapping screws
- 2x 4010 blower fans (24v recommended)
- 1x 3010 hotend fan (24v recommended)

Building:

- If you are using one of the Klicky variants, add the wires and magnets to the toolhead
- There is a hole on the left face to put the left 4010 blower fan cable through, do this first
- Insert the 3010 hotend fan and route both fan cables through the provided channel and secure the 3010 fan
- Take care when screwing the hotend fan as it's secured into plastic and too much force will strip the created threads and/or deform the fan
- Be careful not to leave the cables loose or over the hotend mount
- Insert the 4010 fans into each side and slide backwards into the restraints
- Secure each fan using a M2x10mm self tapping screw at the bottom front hole
- Carefully mount the hotend into place making sure not to pinch any fan cables
- Run the hotend and fan cables along the 10mm side of the 4010 fans on each side and zip tie at the top
- Offer the hotend up to the toolhead mount and secure being careful not to trap any of the cables
- Check the X and Y movement still triggers the end-stops
- Check you have modified all the fan connections on the MCU if you have switched to higher voltage fans
