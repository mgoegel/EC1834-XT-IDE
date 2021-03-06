# XT-IDE 8-Bit IDE Controller for Robotron EC1834

[Deutsche Version](README-DE.md)

This is a modified version of the original Glitchworks XT-IDE rev 4 controller.

The ISA edge connector is replaced with DIN 41612 connector, used by the Robotron EC1834 PC.

Also the layout of the PCB was modified, to fit the mounting height.

Modification was done by Mario Goegel.

**IMPORTANT NOTES ON Rev 4b (Revision not printed)**

The idea to change the pull down resistors to pull up was an bad idea, as I did not saw all required changes.
The board will just not work, if assembled as planned.

Required changes:

* Pin 2 from RN2 has to be disconnected
* A 10K resistor needs to be connected on U1 pin 12 and GND (may be C1)
* The descriptions are not correct for SW2 ENA and WR - they match the original version, as they are not connected to RP2
* SW2 8K might be out of function - and 28C256 ROMs might not work. Untested, 82C64B are fine.

Fixed in revision 4c

**Disclaimer:**

I don't take responsibility for any damages resulting from these modifications. All changes have been made with the best of intentions and to the best of my knowledge.
Use on your own risk!

Original text from Glitchworks (modified):

[Glitch Works](http://www.glitchwrks.com/) continuing extension of the XT-IDE rev 2 ISA controller. This board, when used with a custom BIOS like the XT-IDE Universal BIOS, allows the use of modern 16-bit IDE devices on the 8-bit ISA bus.

More info on the Glitch Works project to provide boards, kits, and fully assembled units [can be found here](http://www.glitchwrks.com/xt-ide). A writeup on the rev 4 design process [is available here](http://www.glitchwrks.com/2017/11/23/xt-ide-rev4). 

Except for the DIN 41612 connector.

If you're looking for the rev 3 branch, [it can be found here](https://github.com/glitchwrks/xt_ide/tree/rev_3). The README and related documentation have been preserved along with the design files.

### Jumper Settings

[modem7](http://minuszerodegrees.net/) created a great set of jumper diagrams for the rev 4 boards, available [on his site](http://www.minuszerodegrees.net/xtide/rev_4/XT-IDE%20Rev%204%20-%20general.htm).

### Bill of Materials

You can find a BOM with Mouser part numbers [here](https://github.com/glitchwrks/xt_ide/blob/master/bill_of_materials.md). Do note that you can purchase complete parts kits from [The Glitch Works](http://www.glitchwrks.com/xt-ide) in addition to bare PC boards.

### Slot 8 Support

Completely removed in this version!

### Contributors

* Mario Goegel: Modification for EC1834
* Scott Christensen: inspriation 16-bit ATA interface for the 8-bit ISA bus
* Jeff Leyda/Hargle: original production board work, original BIOS work
* Andrew Lynch/N8VEM: layout work, initial group buy(s) on earlier revisions
* modem7: documentation, switch/jumper drawings

**Please contact me or send a pull request to get your name added to the list!**

There were no authors/contributors listed in the XT-IDE rev 2 schematics/board layout I started with. If you have contributed to this project and would like your name here, on the schematic, or on the board layout, please let me know. You can open an issue or submit a pull request.
