# Finish Detection During a Pass

When a turtle is already beyond the finish threshold at the start of its turn, the program records that turtle's color and switches the race state off.

The loop does not immediately break out of the current `for` traversal. Other turtles later in the same pass are still visited, so the stored winner color can be replaced if another already-finished turtle is encountered.
