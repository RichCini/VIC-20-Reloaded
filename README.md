# VIC-20-Reloaded
Reimaging of the original VIC-20cr ("cost-reduced") main board in a smaller footprint based
on schmetics of the 251027-01D version as redrawn by Steve Gray. This should represent
changes through ECO 830151 as of 4/12/1983.

# Introduction
This project is a re-implementation of a VIC-20 based on the cost-reduced version from 1983.
It's built using commonly-existing TTL (all of the original types of chips used are still 
generally available) and original core chips from a VIC-20 (the CPU, VIAs, VIC, and original
mask ROMs) that were typically socketed. The memory chips (2114L and 6116) are still available
in the used or new-old-stock market. 

# How is this version similar?
Since it's based on the original schematics, it's identical operationally and 99% identical
electrically (except as noted in the next section). I also tried to keep the parts placement
similar to the original. Parts designators are the same.

# How is this version different?
My main goal was to reimplement the VIC in a smaller form factor. I was able to squeeze it
{mostly} into an S-100 format (which is 10" x 5"; actual is 10.375" x 5.375"). 

Due to the smaller form factor, the cassette port was eliminated (instead opting for a 
6-pin header for an external driver) and the user port was moved to the left side. The 
expansion cartridge was changed to vertical (more like the Atari 2600; saved about 2" of 
board space).

Electrically, I opted for a single 5V power supply (9VAC wasn't needed as there is no
cassette port), and the power switch is slightly different due to parts availability.
I also added a small fuse on the keyboard connector to facilitate using it with an 
off-board PS/2 converter.

Also, since the board is autorouted to a smaller footprint, circuit paths and keepout
areas are different.
