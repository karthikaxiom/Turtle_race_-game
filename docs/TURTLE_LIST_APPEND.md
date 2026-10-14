# Turtle List Construction

Each newly created turtle is appended to `all_turtles` after its shape, color, pen state, and starting position are configured.

The resulting list preserves creation order. The race loop later traverses this list directly, so movement and finish checks occur in the same stored order for every pass through the loop.
