# Dual table machines

## Overview
Control Nesting supports dual-table machines with special settings.

## Configuration
- Select the Dual Table option in Control Nesting settings.
- Define the needed offsets and machine configuration, such as XU or YV.

## Behavior
- The first sheet posts to the primary table.
- The next sheet posts to the secondary table.
- Additional sheets alternate between tables.
- Axis redirects are written automatically with the secondary table offset.

## Manual table tie option
- If the Manual Table Tie switch is ON, the two tables can be treated as one large working surface.

## Dual head machine note
- Set G901 so it is centered on the width of the material used for nesting.
- Enter half of the actual material width in the load screen.
