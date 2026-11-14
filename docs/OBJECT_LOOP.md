# Turtle Creation Loop

The creation loop runs six times. Each pass creates a turtle-shaped object, assigns its indexed color, lifts its pen, places it at x = `-370` and the indexed y-coordinate, then appends it to `all_turtles`.

The same index pairs color and lane. The append operation preserves creation order for the later race traversal. Each object is moved in place; the list is not rebuilt as coordinates change.

See [Turtle Configuration](TURTLE_CONFIGURATION.md), [Paired List Indexing](LIST_INDEXING.md), and [Collection Traversal](COLLECTION_TRAVERSAL.md).
