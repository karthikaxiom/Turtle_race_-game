# Screen Shutdown

The script reaches `screen.exitonclick()` after the race loop, whether or not that loop ran. This is the common final interaction for both startup outcomes.

## Completed race

When a processed turtle is detected beyond the finish threshold, `race_on` is set to false. The current inner `for` traversal still completes; the outer `while` loop then stops before another pass begins. Execution proceeds to `screen.exitonclick()` after the loop.

## Falsey input

When the startup dialog returns a falsey value, `race_on` is initialized to false after turtle setup. The race loop is skipped, but execution still reaches the same click-to-exit call.

## Window close action

`screen.exitonclick()` leaves the graphics window available until the user clicks it. The source does not automatically close the window immediately after printing a result, does not provide a separate restart control, and does not request a second guess after a race.

This describes the call present in `main.py`; it does not specify operating-system window-manager behavior beyond the program's click-to-exit request. See [Program Lifecycle](PROGRAM_LIFECYCLE.md) for the shared path.
