# Starting Positions

Every turtle is placed at an x-coordinate of `-370` before the race loop begins.

The y-coordinates are defined by:

`[-70, -40, -10, 20, 50, 80]`

The creation loop assigns one y-coordinate to each turtle by index. The turtles therefore start in six distinct horizontal lanes while sharing the same starting x-coordinate.

The program calls `penup()` before `goto()`, so this initial placement does not draw a line.
