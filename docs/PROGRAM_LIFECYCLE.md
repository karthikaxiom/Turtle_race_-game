# Program Lifecycle

`main.py` runs as a single script from top to bottom. It does not define a separate application entry-point function or a persistent application service.

## Startup and participant setup

1. Import the standard-library `turtle` and `random` modules.
2. Create the graphics screen and set its dimensions and title.
3. Define the color and vertical-position lists used by the creation loop.
4. Show the text-input dialog and store its return value in `user_bet`.
5. Create the empty `all_turtles` list.
6. Create six turtle objects in list order. For each one, assign its indexed color, lift its pen, move it to x = `-370` and its indexed y-coordinate, then append it to the list.
7. Initialize `race_on` from the truthiness of the stored input.

The input dialog appears before turtle creation. Cancellation does not skip object setup: all six turtles are still created before the falsey value leaves the race loop disabled.

## Active race

When `race_on` is true, the outer `while` loop begins a pass through `all_turtles`. Each turtle's current x-coordinate is checked before that turtle's random movement call. The threshold is strict (`xcor() > 370`), and the check is not repeated immediately after movement.

A detected finisher sets `race_on` to false and prints a result. That assignment does not break the current inner `for` loop. The current turtle still reaches its movement call, and later turtles in the same pass are still checked and moved. If more than one is already beyond the threshold when processed, more than one result can be printed.

## Shutdown

After the current inner pass completes—or immediately after setup when input was falsey—the outer loop is no longer entered and execution reaches `screen.exitonclick()`. The graphics window remains available until the user clicks it.

## Interpretation boundary

The code does not select a winner through a separate event handler, store a race history, or run an automatic replay cycle. The descriptions here are a map of the existing source, not a promise that random outcomes or completion times will be repeatable.

Source of truth: `main.py`.
