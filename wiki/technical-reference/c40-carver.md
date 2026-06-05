# C40 Carver machine

## Overview
Some C40 carvers in the field were upgraded to Windows, but they do not use tool management.
They use macros to operate tool changes and spindle ON.

## Definitions
- **Flat work**: Any part created with the probe without a rotary axis.
- **Round work**: Primarily done on carvers and also on Rotary Playback devices for 3-axis machines.
- **Headstock**: The driving part of the rotary axis.
- **Tailstock**: Spring-loaded device opposite the headstock that maintains pressure on the part.
- **Probe offset**: Offset values for round work only.
- **Acceleration**: How quickly the machine ramps up and down, in in/sec².
- **Gains**: How strongly the motors react to direction changes.
- **Tangency factor**: A setting from 1 to 40.
- **Microns**: Unit of measure for probe deflection.
- **Bias**: Preloaded deflection on each axis.
- **Deadband**: Gray area with no deflection.
- **Feed gain**: Multiplier affecting how quickly the machine slows for inclines.
- **Broach pass**: Prompts the operator for broach pass amount and increment.
- **Scan time**: Affects program creation only.
- **Run time**: Applied to the final NC program.

## Helpful notes
- Backup `Scanset.bin` before major changes.
- If the probe drifts, increase deadband or decrease bias.
- If the probe hops, slow the scan feed, increase Z bias, or fill the drop-off with wax.
- Always begin the boundary on the tailstock end for round work.
- A good starting step over is usually 10% of cutter diameter.

## Menus
- **Manual Mode**: point and drag modes, deadband settings
- **Hunt Mode**: gains, accelerations, bias, tangency
- **General Menu**: run/index speeds, probe offsets, scan speeds, step over, rotation angles
- **Touch Mode Setup**: settings for auto measure and initial touch on scans

## Broach pass removal
The following lines are examples of probe file logic that would be removed to eliminate broach pass behavior in a flat scan file.

```text
[OPEN "RUNCOUNT.THM" FOR INPUT AS #1]
[INPUT #1, RUNNUM]
[INPUT #1, BROACHOFF]
[INPUT #1, BROACHINCR]
[CLOSE #1]
[RUNNUM = RUNNUM + 1]
IF [RUNNUM > 1] THEN M81L23
IF [ALREADYDONE = 9999] THEN M81L23
[WINDOW ON]
[CLS]
[PRINT "ENTER BROACH PASS OFFSET"]
[INPUT BROACHOFF]
[PRINT "ENTER BROACH PASS INCREMENT"]
[INPUT BROACHINCR]
[WINDOW OFF]
[ALREADYDONE = 9999]
[OPEN "RUNCOUNT.THM" FOR OUTPUT AS #1]
[PRINT #1, RUNNUM]
[PRINT #1, BROACHOFF]
[PRINT #1, BROACHINCR]
[CLOSE #1]
M80L23
[CURROFF=-BROACHOFF]
G90G01
G09F8.0
```
