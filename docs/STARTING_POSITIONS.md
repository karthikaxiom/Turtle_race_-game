# Starting Positions

Every turtle is placed at the same horizontal coordinate, x = `-370`, before the race loop begins.

The six starting y-coordinates are:

`[-70, -40, -10, 20, 50, 80]`

The turtle-creation loop selects a y-coordinate by participant index. The same index selects the color from the `colors` list, so each participant's color and lane remain paired.

The program calls `penup()` before `goto(x=-370, y=y_positions[i])`. The initial placement therefore does not draw a line.

This page describes the shared starting line and the per-participant lane assignment. See [Turtle Color Mapping](COLOR_MAPPING.md) for the fixed color order and [Race Coordinates](COORDINATE_SYSTEM.md) for screen and finish-threshold details.
