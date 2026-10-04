# Loop Sequence

The current implementation uses two explicit loops.

## Creation loop

The first loop runs six times to construct the turtle objects, configure them, place them, and append them to `all_turtles`.

## Race loop

The outer `while race_on` loop repeats while the race state is true. Inside it, the `for turtle_ in all_turtles` loop processes the stored turtles in list order.

The nested structure means one complete pass processes every stored turtle before the next outer-loop pass begins, unless the outer condition becomes false afterward.