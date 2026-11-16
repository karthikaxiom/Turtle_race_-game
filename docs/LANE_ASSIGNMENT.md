# Lane Assignment

Turtle creation uses the same participant index to select a color from `colors` and a vertical coordinate from `y_positions`. This pairs each turtle with one stable color and lane for the duration of the run.

The complete coordinate and pairing contract is maintained in [Starting Positions](STARTING_POSITIONS.md) and [Color Mapping](COLOR_MAPPING.md).

## Pairing check

The index is the join key between the color and y-position lists: index `0` pairs red with `-70`, and index `5` pairs purple with `80`. Reordering only one list changes the lane associated with a color even though the participant count remains six. Review both lists together when editing participant configuration.
