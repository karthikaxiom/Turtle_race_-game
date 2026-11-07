# Screen Shutdown

The script reaches `screen.exitonclick()` after the race loop, regardless of whether the loop ran.

## Completed race

When a turtle is detected beyond the finish threshold, `race_on` is set to false. The current inner `for` traversal still completes; the outer `while` loop then stops before another pass begins. Execution proceeds to `screen.exitonclick()`.

## Cancelled input

When the startup dialog returns a falsey value, `race_on` is initialized to false. The turtle objects are still created, but the race loop is skipped. Execution still proceeds to the same click-to-exit call.

## Window close action

`screen.exitonclick()` leaves the graphics window available until the user clicks it. The source does not automatically close the window immediately after printing a result, and it does not provide a separate restart control.

Source of truth: `main.py`.
