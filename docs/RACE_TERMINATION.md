# Race Termination

The race loop uses a two-level structure:

- The outer loop continues while `race_on` is true.
- The inner loop visits every turtle in `all_turtles` in its existing list order.

A turtle is considered a detected winner when its x-coordinate is already greater than `370` at the start of that turtle's turn.

The threshold check occurs before the movement call. Therefore:

- A turtle that moves beyond `370` during its current turn is not detected until a later turn.
- Setting `race_on = False` does not break the inner `for` loop.
- Later turtles in the same pass are still checked and moved.
- If multiple turtles already satisfy the threshold in one pass, each can produce a result.
- After the inner loop finishes, the false `race_on` value prevents another outer-loop pass.

The code does not draw a separate finish line; `370` is the logical threshold used for detection.
