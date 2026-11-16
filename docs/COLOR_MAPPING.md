# Turtle Color Mapping

The `colors` list defines six participant colors in source order: red, orange, yellow, green, blue, purple.

| Index | Color | Starting y |
| ---: | --- | ---: |
| 0 | red | -70 |
| 1 | orange | -40 |
| 2 | yellow | -10 |
| 3 | green | 20 |
| 4 | blue | 50 |
| 5 | purple | 80 |

The creation loop uses the same index for `colors[i]` and `y_positions[i]`. Reordering one list without the other changes the color-to-lane pairing. The order is fixed by source; only movement distances are randomized.

See [Starting Positions](STARTING_POSITIONS.md) and [Collection Traversal](COLLECTION_TRAVERSAL.md).