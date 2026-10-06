# Rendering State

Each turtle is created with the `turtle` shape, assigned a color, and then switched to pen-up mode before its initial position is set.

Because `penup()` is called before `goto(...)`, the initial placement does not draw a line from the turtle's default origin to its starting coordinate.

The race then uses `forward(...)` for movement while the pen remains up. The source therefore moves the turtle graphics without intentionally drawing movement trails.
