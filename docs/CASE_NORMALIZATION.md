# Result Comparison Normalization

The source expression is `winning_color == user_bet.lower()`. Lowercasing is applied to the user's stored input, not to `winning_color`, which comes from the turtle's pen color.

The comparison is exact after that conversion. It does not call `strip()`, normalize internal spaces, or validate the value against the configured list before the race starts.

Examples: `RED` can match `red`; ` red ` does not; `teal` is truthy and starts a race but cannot match one of the six configured colors.

See [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).