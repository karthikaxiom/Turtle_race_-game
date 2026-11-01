# Turtle Pen State

Each turtle calls `penup()` before it is moved to its starting position.

The initial positioning operation therefore does not draw a line from the turtle's default location. Subsequent forward movement also starts with the pen raised because no later code calls `pendown()`.