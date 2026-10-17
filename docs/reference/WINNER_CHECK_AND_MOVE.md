# Winner Check and Movement Order

For each turtle turn, the current implementation checks the turtle's x-coordinate before calling `forward(...)`.

The effective order is:

1. Inspect the current x-coordinate.
2. If it is greater than `370`, mark the race state as finished and report the result.
3. Call `forward(...)` using a newly generated random distance from `0` through `10`.

Because movement occurs after the check, crossing the threshold during a turn is not reported until that turtle is encountered again on a later pass. If the race state becomes false during a pass, later turtles in that same pass are still processed before the outer loop stops.
