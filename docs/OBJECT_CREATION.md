# Turtle Object Creation

The current implementation creates the race participants in a single `for` loop.

## Creation sequence

For each index from `0` through `5`, the program:

1. Creates a turtle with the `turtle` shape.
2. Assigns the color at the same index in the `colors` list.
3. Calls `penup()` so movement does not draw a trail.
4. Places the turtle at x = `-370` and the corresponding y-coordinate.
5. Appends the object to `all_turtles`.

The loop therefore creates six objects and stores references to all six in one list.

## Ordering

The list order is also the order used later by the race loop. No sorting or reshuffling occurs after creation.

This means configuration order is preserved from object creation through race processing.