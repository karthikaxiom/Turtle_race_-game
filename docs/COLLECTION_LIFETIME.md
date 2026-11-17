# Turtle Collection Lifetime

`all_turtles` is created as an empty list before participant construction. Each configured turtle is appended once, and the completed list is traversed by the race loop.

The same collection remains in use for one launch. The current program does not replace, sort, shuffle, filter, or rebuild it during the race.

## Lifetime boundaries

- **Before creation:** the list exists but contains no participants.
- **After creation:** it contains six turtle references in configured order.
- **During the race:** the loop reads those references and moves the referenced objects.
- **After the race:** the script reaches `screen.exitonclick()`; it does not serialize the list or retain it for another launch.

The collection is process-local state, not saved game data. See [Collection Traversal](COLLECTION_TRAVERSAL.md) and [Data Flow](DATA_FLOW.md).

## Identity versus position

Appending a turtle stores its object reference in the list. Movement changes the referenced object's coordinates without changing the list's membership or order. This is why later turns can inspect updated positions while still visiting participants in the same configured sequence.
