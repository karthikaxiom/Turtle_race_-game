# Starting Positions

Every turtle is placed at the same horizontal coordinate, x = `-370`, before the race loop begins. The starting y-coordinate is selected using the participant's index in the creation loop.

| Participant | Color | Starting coordinate |
| ---: | --- | --- |
| 1 | red | `(-370, -70)` |
| 2 | orange | `(-370, -40)` |
| 3 | yellow | `(-370, -10)` |
| 4 | green | `(-370, 20)` |
| 5 | blue | `(-370, 50)` |
| 6 | purple | `(-370, 80)` |

The lanes are separated by 30 coordinate units. The program calls `penup()` before `goto(...)`, so initial placement does not draw a line. The same participant index selects the color and y-coordinate, keeping each turtle's identity paired with its lane during the run.

This page describes configured start coordinates, not guaranteed finish positions. See [Color Mapping](COLOR_MAPPING.md) for the color list and [Race Coordinates](COORDINATE_SYSTEM.md) for the screen size and logical finish threshold.
