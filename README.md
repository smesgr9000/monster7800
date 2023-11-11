# Alternative Atari 7800 compatible PCB for Monster Joystick Retro Kits

monster7800 is an alternative PCB board for the Monster Joysticks 8/16bit *Retro BASIC* and *Deluxe* Joystick Kits to support both buttons on Atari 7800 console. The board also works with some other devices, like the original Atari 7800 Proline joystick and gamepad.

*This project is not associated with Monster Joysticks Ltd.*

![build earlier revision of monster7800](<./monster7800_0.9.JPG>)

## ordering boards

To order the latest version either use KiCad or use release zip from GitHub.
To generate the Gerber files yourself, open _monster7800.kicad_pcb_ in KiCad. Use _Fabrication Output_ > _Gerber_ and select an output folder and agree with _Plot_ with the default configruation. Also use _Fabrication Output_ > _Drill Files_ than select the same output folder and agree with _Generate Drill File_.

The ordering and manufacturing depends on your selected PCB manufacturer. For www.pcbway.com:

- enter length/width (57 x 33mm)
- 2 layers
- 1.6mm thickness
- FR4
- TG 150-160
- 6/6mil Min Tracking
- 0.3mm Hole Size
- Solder Mask - any is fine
- Silkscreen - any is fine
- No Edge Connector
- Finish - any is fine but would suggest HASL
- Tending Vias
- 1oz Finish Copper

Upload a zip containing the above generated files. Currently the price for 5 boards should be 5$.

## soldering

To finish the board two resistors are required. You could reuse and desolder the D-Sub 9 connector and pin header of the shipped Joystick Kit thus marked optional in the list below.

Reference | Part | Amount | Description
--- | --- | --- | ---
R1, R2 | Vishrey MRS25000C6200FCT00 | 2 | 620ohm resistor
J1 | Amphenol 10129379-909004BLF | 1 | optional, if Joystick Kit pin header isn't reused
J2 | Amphenol  D09S33E4GV00LF | 1  | optional, if Joystick Kit D-Sub isn't reused

## building

if the joystick isn't build yet, follow the building instruction of the joystick and use the monster7800 instead of the delivered board. Otherwise open up the top cover and replace the current PCB board with the atari7800.

## compatibility

As the original Atari 7800 joystick a Monster Joystick equipped with this PCB should have the same compatibility list. Some tested devices:

Device | Works | Description
--- | --- | ---
Atari 7800 | Yes | PAL & NTSC tested, buttons could be flipped see original build instructions
Atari 2600 | Yes | PAL Jr tested, both buttons are recognised, but 2600 only support one action
Atari 8bit | Yes | PAL 800XL tested, both buttons are recognised, but computer only support one action
Atari ST | Depends | STE tested, does not work in mouse port (port 0), works fine in joystick port (port 1)

