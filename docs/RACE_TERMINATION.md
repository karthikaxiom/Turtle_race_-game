# Race Termination

The race uses an outer `while race_on` loop and an inner `for turtle_ in all_turtles` traversal.

A turtle is detected as a finisher when its current x-coordinate is greater than 370 at the start of its turn. When that condition is true, the program sets `race_on = False`, captures the turtle's pen color, and prints the matching win or loss result.

Setting `race_on` to false does not break or return from the inner `for` loop. The current turn still reaches its `forward(...)` call, and turtles later in the list are still checked and moved during the same pass.

This means:

- A turtle that crosses x = 370 during its movement call is detected on a later turn.
- The current inner-loop pass completes after `race_on` becomes false.
- More than one turtle can satisfy the threshold in the same pass, so more than one result line can be printed.
- The next outer-loop pass does not begin because its condition sees `race_on` as false.
- If the startup input is falsey, `race_on` is false from initialization and the race loop is skipped entirely.

The current source has one race flow per script launch and no in-loop restart mechanism. The code does not draw a separate finish line; 370 is a logical coordinate threshold.

Source of truth: `main.py`.
