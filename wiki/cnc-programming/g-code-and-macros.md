# G-code and macros

## Typical G-code usage

### G07F# - S Ramp Control
- Controls smoothing of segmented motion
- F values range from 1 to 100
- F0 turns the feature off
- Default is G07F50 on power-up

### G08F# - Arc Factor
- Sets maximum circular speed
- F values range from 0.1 to 5
- Default is G08F1

### G09F# - Tangency Factor
- Tangency factor values range up to 40
- Default is G09F1 on power-up
- Values above about 8 are usually not recommended

### G94
- Used to make rotary motion react more like linear motion during multi-axis moves

### G96
- Constant tip speed for 4 or 5 axis motions
- Can improve cycle time in certain applications

### G02 / G03
- G02 = clockwise arc
- G03 = counterclockwise arc
- I and J are used as incremental center offsets

## Typical tool change code
```text
S#####
T# M3
G0 X# Y#
M31
G0 Z#
```

## Typical ending sequence
```text
M05
G990
G90 G0 Z0
X0 Y0 V0 C0 B0
M02
```

## Tool calls
- Newer versions use T# for tool calls
- Older versions may use M# style tool calls
- Dual-head machines may balance heads based on daylight values

## Special macros and commands
- M31: wait for router to reach full speed
- M137/M138: left front door E-stop disable/enable
- M139/M140: right front door E-stop disable/enable
- M551-M559: drill bank drill calls
- G10/G11: mirror commands
- G54: tooling compensation in absolute programs when cutter comp is off
- G92: fixture offset and cutout adjustment use cases
- Axis oscillation can be used on THM v5.05

## Tangency factor guidance
- Values 1 to 8 are generally recommended
- Higher values reduce stopping at non-tangent transitions
- Very high values can negatively affect cut quality
