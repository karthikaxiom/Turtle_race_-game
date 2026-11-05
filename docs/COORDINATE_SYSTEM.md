# Race Coordinates

The current implementation uses the Turtle graphics coordinate system directly for setup and finish detection.

## Screen dimensions

The screen is configured with `screen.setup(width=800, height=400)`, giving the game a window width of 800 and height of 400.

## Starting positions

Every turtle starts at x = `-370`. The six y-coordinates, in participant order, are:

`[-70, -40, -10, 20, 50, 80]`

The same loop index selects the turtle's color and its y-coordinate. This produces six distinct horizontal lanes with a shared horizontal starting point. The turtle is moved to its initial position after `penup()`, so setup does not draw a trail.

## Finish threshold

The race loop checks whether a turtle's current x-coordinate is greater than `370`. The comparison is strict: a position of exactly 370 does not satisfy the condition. The code does not draw a separate finish-line object; 370 is a logical threshold used by the loop.

Movement occurs in discrete increments, so a turtle can pass the threshold without landing exactly on it. The finish check observes the coordinate on the turtle's next turn, before that turn's movement call.

Source of truth: `main.py` (`screen.setup`, `y_positions`, `goto`, and `xcor() > 370`).
