# Race Termination

The race uses an outer `while race_on` loop and an inner `for turtle_ in all_turtles` traversal. A turtle is detected as a finisher when its current x-coordinate is greater than 370 at the start of its turn.

## When the finish check succeeds

The source sets `race_on = False`, captures the current turtle's pen color, and prints the corresponding win or loss message. It does not execute `break`, `return`, or another immediate exit from the inner loop.

The current turtle still reaches its `forward(...)` call, and turtles later in the list are still checked and moved during that same pass. If another later turtle is already beyond the threshold when its turn is processed, it can also print a result. The variable `winning_color` can be assigned again by a later qualifying turtle in that pass.

## What happens next

- A turtle that crosses x = 370 during movement is detected on a later turn.
- The active inner pass completes after `race_on` becomes false.
- More than one result line can be printed in a pass if multiple processed turtles satisfy the condition.
- The outer `while` condition prevents another complete pass from beginning.
- If startup input is falsey, `race_on` starts false after setup and the race loop is skipped entirely.

The current source has one race flow per script launch and no in-loop restart mechanism. It does not draw a separate finish line; 370 is a logical coordinate threshold. See [Threshold Detection Timing](THRESHOLD_DETECTION.md) for the comparison and [Output Branching](OUTPUT_BRANCHING.md) for the messages.

Source of truth: `main.py`.
