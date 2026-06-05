# Renishaw probe and scanning

## Overview
These notes cover scanning, probe setup and removal, boundary files, and scan utilities.

## Scanning limitations
- Scanning can only be done with the router in the vertical position.
- On 5-axis machines, manual point picking can be done at 90 degrees, but scanning cannot.
- You can only scan a short distance of vertical wall with the router straight down.

## Drop-off guidance
- The drop-off should normally not be more than the radius of the tool being used for scan.
- If needed, build up the surface with wax and smooth it with baby powder.
- After scanning, use probe Pick/Drag mode to clean up the wax area.

## Probe setup and removal
- The machine must be in E-stop.
- On five-axis machines, once the probe has been attached, it must be weighed before continuing.

## Boundary file setup
1. Enter Manual Probe Mode.
2. Pick 3 points for sharp corners.
3. On straight paths, pick points at least every 2 inches.
4. Final point should be approximately 3/8 inch short of the starting point.
5. Save points as a boundary file.

## Scanning a part
- Load the boundary file.
- Press start to run and create the scanned path.

## Files generated
- CARRIER
- TCARRIER
- MDI

## Important note
When running a boundary program during a part scan, the machine will come to the X and Y starting point and hesitate before plunging on Z.
The Z bias must be set for the machine to begin the plunge.
