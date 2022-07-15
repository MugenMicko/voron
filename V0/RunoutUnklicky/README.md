# Runout UnKlicky Sensor

The Runout UnKlicky Sensor is a filament runout sensor that can be used to pause a print if printing filament breaks, runs out or otherwise is no longer present in the sensor.

The design uses magnets as the switch, making it easy to cheap source BOM components.

![design](images/design.png)


## Printing:

- Use the Voron defaults and print in ABS or better
- The parts are orientated correctly in the STLs


## BOM:

- 5x M3x8mm SHCS/BHCS (2x for the wired screws, 2x for the top/base, 1x for 2020 extrusion mount)
- 2x 6x3mm neodymium magnets (for the switch)
- 1x M2x10mm (optional for 1515 extrusion mount)
- 1x M3 Hammer T-Nut (for 2020 extrusion mount)
- 2x fork connectors (optional - for attaching wires)


## Assembly:

![parts](images/parts.jpg)
![pin](images/pin.jpg)
![magnets](images/magnets.jpg)
![assembly](images/assembly.jpg)
![cable](images/cable.jpg)
![nofilament](images/nofilament.jpg)
![filament](images/filament.jpg)


## Wiring:

Wire to an end-stop or similar pin. Do _not_ connect to voltage, _only_ to pin and GND.

Upload and include runoutunklicky.cfg and change the PIN definition. Test. If it shows incorrectly in klipper add a ! in front of the PIN definition and test again.
