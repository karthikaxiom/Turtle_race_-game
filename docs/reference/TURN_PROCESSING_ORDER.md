# Turn processing order

The race loop traverses `all_turtles` in list order. For each turtle, the current x-coordinate is checked against the finish threshold before that turtle receives its random forward movement for the same pass.