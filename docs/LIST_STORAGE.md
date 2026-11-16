# Turtle List Storage

The script creates `all_turtles` before the creation loop, appends each configured turtle once, and later traverses that same list in its stored order.

The list holds references to turtle objects, not copies of their coordinates. When `forward(...)` moves an object, the object observed through the list reflects its updated position on later turns.

The collection is in-memory only and is not persisted. See [Collection Traversal](COLLECTION_TRAVERSAL.md), [Collection Lifetime](COLLECTION_LIFETIME.md), and [Data Flow](DATA_FLOW.md).

## Collection invariants

The list is populated once during setup and is not appended to or reordered by the race loop. The loop therefore traverses the same six object references on each pass. Position changes belong to the turtle objects themselves; they do not replace or reorder list entries.
