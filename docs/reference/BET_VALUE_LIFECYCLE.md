# Bet Value Lifecycle

The input dialog stores its return value in `user_bet`. That value first controls whether the race loop starts and later participates in the winner comparison.

See [Input Lifecycle](../INPUT_LIFECYCLE.md) for the capture and startup sequence, and [Input Normalization Boundary](../INPUT_NORMALIZATION_BOUNDARY.md) for the later comparison.