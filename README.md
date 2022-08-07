# VIC-20-Reloaded
Reimaging of the original VIC-20cr ("cost-reduced") main board in a smaller footprint based
on schmetics of the 251027-01D version as redrawn by Steve Gray. This should represent
changes through ECO 830151 as of 4/12/1983.

## Introduction
This project is a re-implementation of a VIC-20 based on the cost-reduced version from 1983.
It's built using commonly-existing TTL (all of the original types of chips used are still 
generally available) and original core chips from a VIC-20 (the CPU, VIAs, VIC, and original
mask ROMs) which were typically socketed. The memory chips (2114L and 6116), which are not
typically socketed, are still available as used or new-old-stock. 

## How is this version similar?
Since it's based on the original schematics, it's identical operationally and 99% identical
electrically (except as noted in the next section). I also tried to keep the parts placement
relationally similar to the original, recognizing that the board size is different. Parts 
designators are the same.

## How is this version different?
### Size
My main goal was to reimplement the VIC in a smaller form factor. I was able to squeeze it
{mostly} into an S-100 format (which is 10" x 5"; actual is 10.375" x 5.375") size. As such,
this board isn't a drop-in replacement. However, the spacing and placement of the side 
(power/joystick) and the rear (expansion cartridge, video, serial IEC) are
placed at the correct distances from the upper-right corner.

### Ports
Due to the smaller form factor, the cassette port was eliminated (instead opting for a 
6-pin header for an external driver) and the user port was moved to the left side. The 
orientation of the expansion connector was changed to vertical (more like the Atari 2600
which saved about 2" of board space). Using the expansion connector is limited to one
cartridge, or an expansion board that uses two pieces connected by a cable (there is
another repro here that has an example).

### Power
Electrically, I opted for a single 5V power supply (9VAC wasn't needed as there is no
cassette port), and the power switch is slightly different due to parts availability.
The main fuse holder is different, but the same 5x20mm fuse is used. Large axial
capacitor was replaced with smaller radial cap of the same value.

### Other
Since the board is autorouted to a smaller footprint, circuit paths and keepout
areas are different from the original.

## Versions
* v1.0-001: Initial prototype based on original schematic; screen artifacts
* v1.1-001: Second prototype with a rearranged chip layout; screen artifacts.
* v1.1-002: Third prototype. A transcription error was found in the original schematic.  
            Corrected. Works.
* v1.1-002E: Final version.

## Known Bugs
Current Release (1.1-002E):
* None

Prior Release (1.1-002D): 
* An error was introduced in this version as a result of rearranging the data bus lines
  lines on IC UF8 (74LS245). D4 (pin 4) and D5 (pin 5) were reversed. There is a picture
  (ECO_001) which indicates a convenient place to cut two traces and cross-wire them.
  Will be fixed in the next version.
  

