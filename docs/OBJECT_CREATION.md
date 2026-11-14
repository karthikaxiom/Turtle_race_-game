# Turtle Object Creation

The current implementation creates participants in a single `for` loop.

## Creation sequence

For each index from `0` through `5`, the program:
1. creates a turtle with the `turtle` shape;
2. assigns the color at the same index in `colors`;
3. calls `penup()` so movement does not draw a trail;
4. places the turtle at x = `-370` and the corresponding y-coordinate;
5. appends the object to `all_turtles`.

The loop creates six objects and stores references to all six in one list. The list order is also the later race-processing order; no sorting or reshuffling occurs after creation.

See [Turtle Configuration](TURTLE_CONFIGURATION.md), [Paired List Indexing](LIST_INDEXING.md), and [Collection Traversal](COLLECTION_TRAVERSAL.md).
