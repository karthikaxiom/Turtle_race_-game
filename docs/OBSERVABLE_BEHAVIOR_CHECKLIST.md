# Observable Behavior Checklist

The following checks describe the current behavior without requiring changes to `main.py`.

- The graphics window is configured before the input dialog is requested.
- The startup dialog accepts text and stores the returned value as the user's selection.
- A non-empty selection enables the race; cancellation leaves the race disabled.
- Six turtles are created with the configured colors and vertical positions.
- Each active turn checks a turtle's current x-coordinate before moving it.
- Movement uses a random integer from `0` through `10`.
- A detected winner produces a terminal result message.
- The outer race loop stops after the active pass completes once `race_on` becomes false.
- `screen.exitonclick()` keeps the graphics window available for a final click.

This checklist is a documentation aid for manual review and does not represent an automated test suite.
