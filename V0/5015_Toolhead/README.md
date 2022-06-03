# 5015 Toolhead
This is a Voron V0.1 toolhead that uses the guts of a 5015 fan for part cooling. It currently only works with the LGX Lite extruder, but the TBG-Lite extruder will be added.

It uses the standard Voron V0.1 X carriage, is based on the [Mini-AfterSherpa](https://github.com/KurioHonoo/Mini-AfterSherpa), but I've designed it from the ground up using TinkerCad :man_facepalming:

This toolhead should not lose any X, Y or Z travel, though the standard cowl might hit on max Y due to the slant of the panels.

![5015_Toolhead](images/5015_toolhead.jpg)

Please Note: This is a Work In Progress and things will likely change as issues are fixed and enhancements are made.


## Printing:

- Use the Voron defaults and print in ABS or better
- The parts are orientated correctly in the STLs
- The cowl will have different variants for choice of probe, or no probe
- Choose the mount for the specific hotend to be used

## BOM:

- 5x M3x20mm SHCS/BHCS (2 for the hotend mount, 3 for the X carriage mount)
- 1x 5015 part cooling fan that you are happy to cut to pieces
- 1x 3010 hotend fan (24v recommended)

The cowl variants will support a no probe setup, [SlideSwipe magnetic probe](https://github.com/chestwood96/SlideSwipe) and [(Un)Klicky Probe](https://github.com/jlas1/Klicky-Probe)

## Fans:

I am using these fans:

- 24v Blower 5015: [Gdstime](https://www.aliexpress.com/item/32865977791.html)
- 24v Axial 3010: [Gdstime](https://www.aliexpress.com/item/1005002857100082.html)

## Heatsink Thermistor:

Each cowl includes a hole at the top to insert a thermistor. With this in place, klipper can track the temperature of the heatsink to watch for heat creep from the heatbreak. You can have klipper abort and shutdown before your whole toolhead melts! You only need a simple klipper entry for the appropriate pin on your MCU, e.g.:

```
[temperature_sensor Heatsink]
sensor_type: Generic 3950
sensor_pin: expander:PA5
max_temp: 85
```

Klipper will shutdown if the top of the heatsink hits 85C. You can use thermal paste to help keep a bulb thermistor in contact with the heatsink and layed the wires through the provided groove, then fitted the extruder on top to hold it in place.

## CAD:

Will be published once released from WIP.

## Assembly:

[currently incomplete]

You need to remove most of the outer shell of the 5010 fan. Before doing so, please connect the fan to your MCU/toolhead board and ensure that it responds to pmw from klipper.

You need to spli the 5010 fan casing in half by poking the tabs on the fan. Once done, take the half with the fan attached and carefully trim off the casing up to the fins. If more breaks off it shouldn't be a problem. What you want to be left with is a ~35mm circle of casing that matches the diameter of the actual fan. Be very careful not to cut the fan wires, or to manipulate the wires too much as they can easily break from their solder patches:
![fancut](images/fancut.jpg)

Using VHB tape, cut to fit the back of the fan. You might want to remove any stickers on the back of the fan casing to ensure a good bond:
![fantape](images/fantape.jpg)

Affix the fan to the fan cap by threading the wires through the hole and centre the fan into the middle of the fan cap. It does not need to be 100% central if you don't mind the off-centre aesthetic.
![fancap](images/fancap.jpg)

![fanfit](images/fanfit.jpg)
![hotendmount](images/hotendmount.jpg)
![extrudermount](images/extrudermount.jpg)
![testassembly](images/testassembly.jpg)
![xmount](images/xmount.jpg)


## Changelog:

- 2022-06-03 WIP release
