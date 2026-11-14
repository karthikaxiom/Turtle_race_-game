# Paired Configuration Lists

The `colors` and `y_positions` lists are indexed together when turtles are created. Index `i` selects both the turtle color and its starting vertical position. The implementation creates six turtles because both lists contain six entries.

## Current pairing

| Index | Color | Starting y |
|---:|---|---:|
| 0 | red | -70 |
| 1 | orange | -40 |
| 2 | yellow | -10 |
| 3 | green | 20 |
| 4 | blue | 50 |
| 5 | purple | 80 |

The creation loop uses the same index for both lists. Changing only one list or reordering one independently would silently change the intended participant-to-lane mapping.

Every turtle shares the starting x-coordinate `-370`. The paired values are setup data; the race loop later traverses the resulting turtle objects in list order.

See [Color Mapping](COLOR_MAPPING.md), [Starting Positions](STARTING_POSITIONS.md), and [List Indexing](LIST_INDEXING.md).
