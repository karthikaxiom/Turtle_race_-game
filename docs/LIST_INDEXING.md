# Paired List Indexing

The turtle-creation loop uses one index `i` for both configuration lists:

- `colors[i]` assigns the turtle's color.
- `y_positions[i]` assigns its vertical lane.
- The shared horizontal starting coordinate is `-370`.

The two lists must remain aligned by index for each participant to keep its intended color/lane pairing. Their current lengths are both six.

See [Color Mapping](COLOR_MAPPING.md) for the canonical participant/color relationship and [Starting Positions](STARTING_POSITIONS.md) for the coordinates.
