# Text Input Storage

The dialog return value is stored in `user_bet` before turtle objects are created and remains available for race activation and the later result comparison.

Correction to the earlier wording: the source does not lowercase the winner color. It evaluates `winning_color == user_bet.lower()`, applying lowercase conversion to the user's stored input at comparison time.

See [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for the maintained explanations.