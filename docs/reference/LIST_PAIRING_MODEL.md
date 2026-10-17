# List Pairing Model

The race configuration is represented by two parallel lists: colors and vertical positions.

- Index 0 pairs `red` with `-70`.
- Index 1 pairs `orange` with `-40`.
- Index 2 pairs `yellow` with `-10`.
- Index 3 pairs `green` with `20`.
- Index 4 pairs `blue` with `50`.
- Index 5 pairs `purple` with `80`.

The turtle creation loop uses the same index for both lists. This keeps the visual lane assignment deterministic while allowing the turtle objects themselves to be stored in a separate list.
