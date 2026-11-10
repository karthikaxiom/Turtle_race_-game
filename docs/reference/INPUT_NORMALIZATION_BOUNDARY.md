# Input Normalization Boundary

The comparison lowercases `user_bet` but does not strip whitespace. The source expression is `winning_color == user_bet.lower()`; the winner color itself is not lowercased by that expression.

See [Input Normalization Boundary](../INPUT_NORMALIZATION_BOUNDARY.md) for the complete behavior, including unsupported non-empty values and cancellation.