# Iteration Order

The race loop visits the turtles in the order they were appended to `all_turtles`.

For each visited turtle, the finish threshold is checked first and the turtle is then moved with a newly generated random distance. This ordering is repeated while the outer race state remains active.