# User Guess Lifetime

The value returned by the startup dialog is stored in `user_bet` and remains available until the result comparison. The current implementation does not replace it during the race.

See [Input Lifecycle](INPUT_LIFECYCLE.md) for when the value is captured and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for how it is used later.