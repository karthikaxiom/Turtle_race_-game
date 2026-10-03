# Turtle Pen State

Each turtle is created with the standard `turtle.Turtle` object and then configured with `penup()`.

Because the pen is lifted before the initial `goto(...)` and before the race movement begins, those movements do not draw trails on the graphics window.

The program does not call `pendown()` later in the race loop.

The reported turtle color is obtained with `pencolor()`. This reads the turtle's pen color even though the pen itself remains lifted for movement.