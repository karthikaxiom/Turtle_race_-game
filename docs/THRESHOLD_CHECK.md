# Threshold Check

During each pass through `all_turtles`, the program checks the current turtle's x-coordinate before moving that turtle.

A turtle is treated as having reached the logical finish threshold when `xcor()` is greater than `370`. At that point the program sets `race_on` to `False` and stores that turtle's pen color in `winning_color`.

The current turtle is still moved once after the check because the `forward()` call follows the threshold branch in the same loop iteration.

Source of truth: `main.py` race loop.
