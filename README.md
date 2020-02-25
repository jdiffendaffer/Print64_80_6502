
Assembly language demo for printing 64 or 80 column text on a graphics screen
 Acorn Atom 64 column
 Atari 64 or 80 column
 Plus/4 80 column


The font data is not stored with the character data in sequential bytes.
It was faster to store the data in separate tables grouped by byte number.
The first byte of every character, the second byte of every character, etc...
This also eliminates the multiply used to calculate the base address of every character
which is really time consuming on the 6502.


To do: 
Plus/4 version is missing the graphics init code.  
The page alignment for the Atari display list was done manually in the code.
This needs to be changed so that the assembler or linker takes care of it automatically.
Including every version in one started out okay, as it let me optimize every version at the same time,
but at this point it's looking cluttered, and it needs split into separate versions of each system.
This will also make it easier to create an Atari version that scrolls the screen by
changing the display list instead of the much slower memory move.  While this will be much faster,
it requires more code to determine where to print the text in the memory map.

This may not be the latest version of the code
