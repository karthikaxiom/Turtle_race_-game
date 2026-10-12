# Pen Color Result Source

The reported winner color is read from the turtle object with `pencolor()` when the finish condition is detected.

The result is therefore derived from the turtle's configured graphics state rather than from a separate color variable maintained by the race loop.
