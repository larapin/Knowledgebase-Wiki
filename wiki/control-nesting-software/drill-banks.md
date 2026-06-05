# Drill bank setup

## Multi X and Y bank drill setup
- The actuator position number must be set to the center tool in the bank for that axis.
- For a 5-bank drill, the actuator position should be 3 or 7 depending on the bank.
- Control Nesting uses the center position as the bank reference.

## Example call
For a 5-drill X bank call:
```text
T#
M555
M554
M552
M551
```

For a 5-drill Y bank call:
```text
T#
M559
M558
M556
M555
```

## Drill bank parameters
- Drill bank boundary settings were added in version 4.03 and later.
- Boundaries are set relative to G901.
- Negative directions must be entered explicitly when needed.
