# 5-axis pivot distance and tool length

## Standard pivot distance
NC programs for Thermwood 5-axis machines are posted using a standard pivot distance.
This is the distance from the tip of the tool to the center of rotation on axis 5.

## Tool length compensation
- The automatic tool length switch records a LENGTH value in Tool Management.
- The control sees this as the difference between actual pivot distance and the standard posted pivot distance.
- For dual-ended routers, the primary end is used for the standard calibration.

## Touch-off guidance
When setting a fixture offset or finding Z on a 5-axis machine:
- Account for the standard pivot distance
- If using the auto tool length switch, record the Z absolute position from home, then auto measure the same tool and record the LENGTH value
- Add or subtract the LENGTH value based on its sign

## Pivot distance calibration
Typical method:
1. Place a gauge pin or tool in the router.
2. Put the router straight down.
3. Touch off on a gauge block or indicator.
4. Rotate axis 5 to horizontal.
5. Touch off again.
6. Adjust Z by half the tool diameter to find the centerline distance.

## 5-axis A.T.L. sensor setup
- Load the tool length sensing program
- Edit the M999 macro to set PRIMARY_STD and SECONDARY_STD
- Measure the standard 2.5 inch tool
- Set the recorded length value back into the macro
- Re-measure and verify it reads near zero

## Calibration note
If the machine is knocked out of tram, pivot distance should be rechecked and the auto tool length sensor reset as needed.
