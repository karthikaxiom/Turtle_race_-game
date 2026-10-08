# Turn Order

The race loop iterates through `all_turtles` in list order. The collection is populated in the same order as the `colors` and `y_positions` lists.

For each turtle in a pass, the program:

1. Checks whether its x-coordinate is greater than `370`.
2. If the threshold is crossed, records the color and sets `race_on` to `False`.
3. Calls `forward(random.randint(0, 10))` for that turtle.

Because the loop does not break immediately when `race_on` changes, later turtles in the same pass can still reach their movement call before the current pass finishes.

Source of truth: `main.py` outer `while` loop and inner `for` loop.
