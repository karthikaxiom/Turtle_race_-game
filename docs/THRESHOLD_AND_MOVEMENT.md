# Threshold and Movement Order

For each turtle in the race loop, the program first checks the turtle's current x-coordinate against the logical threshold of `370`.

Only after that check does it call `forward()` for the current turtle. This means the threshold test uses the position at the start of that turtle's turn, before that turn's movement is applied.

The order is therefore: inspect position, handle a threshold match if present, then advance the turtle.