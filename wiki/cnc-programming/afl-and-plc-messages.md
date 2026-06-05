# AFL and PLC messages

## Overview
AFL can be mixed with EIA code and used to drive custom behavior in Thermwood programs.

## PLC messages
- To PLC messages let the macro tell the PLC things
- From PLC messages let the PLC tell the macro things
- Some sharemem programs let operators view PLC messages and PLC history
- Common example: `FROMPLCMESS21$` returns the active tool

## Calling executables
- Example syntax: `[NEWPROC, "CALL", "FORE", "file path"]`
- The program can call EXE files and possibly COM files
- BAT files are not the same as directly calling a program in AFL

## Tilde behavior
- A leading `~` can allow the controller to read ahead
- This can speed cycle time but may be dangerous if variable values change ahead of time

## Common AFL examples
- `IF [PRODUCTRUN$="Y"] THEN M81L1`
- `IF [TABLE_1$="R"] THEN [CALL "GMRI.SUB"]`
- `IF [TABL1=0] THEN M83`
- `IF [GETTRANS(4)=2] THEN M81L?`
- `IF [GETMASTER(4)=2] THEN M81L?`

## Useful operations
- Set subprogram path with `SETSUBPROGPATH$`
- Use `INPUT` for operator prompts
- Use `WINDOW ON/OFF` and `PRINT` for screen messages
- Use `WRITELENGTH`, `WRITEDAYLIGHT`, `WRITELIFE`, and `WRITETOOLRAD` for tool management updates
- Use `WRITEGAIN`, `WRITEMAXACCEL`, and `WRITEFFWD` for motion tuning
