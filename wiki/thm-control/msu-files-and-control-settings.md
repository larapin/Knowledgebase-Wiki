# MSU files and control settings

## MSU overview
MSU files control many machine behavior settings.
Some versions allow direct programmatic changes; older versions require editing the MSU text file and compiling it into BIN format.

## G95 / constant tip speed behavior
- G95 is used on GEN II and newer controls for constant tip speed behavior
- It uses the tool length and pivot distance together
- The pivot distance in the MSU file must be set correctly
- On V7+, Length and Length Comp work with the posted pivot distance to keep tip speed constant

## S-Ramps / smoothing
- G07F# controls smoothing
- G07F50 is the default value
- G07F0 turns smoothing off

## Fixture offset table changes
On new GEN II interfaces, the fixture offset table:
- Expanded from 100 to 1000 offsets
- Includes descriptions and lock/unlock support
- Uses the new `OFFSET.THM` file

## Hard drive and drive mapping notes
- Older OS/2 systems often kept D:
Data on a separate partition
- Changing default drive location may require MSU changes
- Some setups can be handled by remapping the data share
