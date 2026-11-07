# Program Lifecycle

`main.py` runs as a single script from top to bottom. It does not define a separate application entry-point function.

## Startup

1. Import the standard-library `turtle` and `random` modules.
2. Create the graphics screen and set its size and title.
3. Define the color and vertical-position lists.
4. Show the text-input dialog and store its return value in `user_bet`.
5. Create the `all_turtles` list.
6. Create six turtle objects in list order. For each one, assign its color, lift its pen, move it to the shared starting x-coordinate and indexed y-coordinate, then append it to the list.
7. Initialize `race_on` from whether the stored input is truthy.

The dialog appears before turtle creation. A cancelled dialog does not skip object setup; it causes the race loop to be skipped after setup is complete.

## Active race

When `race_on` is true, the outer `while` loop starts a pass through `all_turtles`. Each turtle's current x-coordinate is checked before its random movement call. A detected finisher sets `race_on` to false and prints a result, but does not break the current inner loop. The current pass therefore completes before the outer condition is checked again.

If more than one turtle is already beyond the threshold during that pass, more than one result can be printed. The source does not guarantee a single result line in that situation.

## Shutdown

After either the completed race path or the cancelled-input path, execution reaches `screen.exitonclick()`. The graphics window remains available until the user clicks it.

Source of truth: `main.py`.
