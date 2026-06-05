# AS.EXE / Axis Shift Utility

## Overview
AS.EXE allows you to adjust line-segment probed programs on the X, Y, and Z axes.
It adjusts the entire program by the amount and direction specified.

## Important limitations
- Works on line-segment programs, not arcs.
- If a main program calls subprograms, run AS on each subprogram separately.
- Programs cannot have any `G92` lines or the utility will not work correctly.

## Installation on OS/2 systems
1. Shell out from the Thermwood screen to the OS/2 full screen using `Ctrl + Esc`.
2. Select the OS/2 full screen from the window list.
3. Change to the `SYSTEM` directory.
4. Insert the AS.EXE floppy disk.
5. Copy `AS.EXE` into the system directory.

## Using AS.EXE
1. Be in the OS/2 full screen and in the `SYSTEM` directory.
2. Type `AS` and press Enter.
3. Enter the input file name and full path.
4. Enter the output file name and full path.
5. Enter X, Y, and Z offsets as needed.
6. The utility converts the file automatically.

## Notes
- Run axis shift on the probed file before making other changes.
- Homing sequences at the end of a program will also be shifted and may need to be corrected manually.
- Best practice is to keep homing in a master program.

## Example caution
If a program ends with moves like `Z0` or `X0Y0`, AS will adjust them too.
