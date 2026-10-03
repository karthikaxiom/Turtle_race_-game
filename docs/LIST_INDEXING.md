# Paired List Indexing

The current implementation keeps turtle colors and starting vertical positions in two lists:

- `colors`
- `y_positions`

The turtle-creation loop uses the same index for both lists.

For each index, `colors[i]` supplies the turtle color and `y_positions[i]` supplies its starting y-coordinate. The starting x-coordinate is the same fixed value, `-370`, for every turtle.

This creates a positional pairing between the two configuration lists without using a separate mapping or configuration object.

The resulting turtle order remains the order established by the color list.