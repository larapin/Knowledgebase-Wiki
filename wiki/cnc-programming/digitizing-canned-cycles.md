# Digitizing, canned cycles, and utilities

## Digitizing parts
### Using the THM machine
1. Place the finished part on the table and fasten it down.
2. Mark the edges you want to capture.
3. Put a pointy tool or pin in the router.
4. Home the machine.
5. Load a blank file.
6. Enter G91 in the header and step through it.
7. Record points with the HHP.
8. Save the file and bring it into MasterCam for cleanup.

### Off-line digitizing
- Digitize points with external hardware and import the result into MasterCam.
- Thermwood no longer sells digitizers.
- DXF-capable digitizers can still be used and edited further in MasterCam.

## Canned cycle programs
- G81 through G89 can be used as cycles 1 through 9
- Cycle programs are saved in the Macros folder
- Each cycle subprogram must end with M99
- The main program calls the cycle and then returns to it until G80 ends the cycle

## Boundary and scan notes
- The boundary program creates carrier files such as CARRIER, TCARRIER, and MDI
- Boundary scan programs may pause before plunging on Z until Z bias is correct

## Quick check 5-axis tram
- Put a gauge pin in the router
- Trace a mark near the table
- Rotate axis 4 through 360 degrees
- If the pin drifts from the traced mark, the machine is out of tram

## Restarting an NC program
- Stop the machine and record the current line
- Verify clearance for Z move
- Home and reset the machine if needed
- Make sure the proper tool is loaded and measured
- Block step to the restart location and resume carefully
