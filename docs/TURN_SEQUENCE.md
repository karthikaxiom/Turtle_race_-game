# Per-Turtle Turn Sequence

Each iteration of the active race loop processes one turtle at a time.

For the current turtle, the implementation performs these operations in order:

1. Read the turtle's x-coordinate.
2. Check whether that coordinate is greater than `370`.
3. If the threshold has already been crossed, set `race_on` to false and print the corresponding result.
4. Call `forward(...)` with a newly generated random distance.

The movement call occurs after the threshold check, including when that turtle has just been recognized as a winner.

After one turtle finishes this sequence, the loop advances to the next turtle in `all_turtles`.

The code does not insert an explicit delay between these operations.