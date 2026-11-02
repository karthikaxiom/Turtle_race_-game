# Pen-Up Initialization Contract

New turtles call `penup()` during setup before being moved to their starting coordinates.

This means the initial `goto()` positioning is performed with the drawing pen lifted, so setup positioning is not intended to draw connecting lines.
