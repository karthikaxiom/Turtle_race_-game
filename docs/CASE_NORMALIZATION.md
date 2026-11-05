# Result Comparison Normalization

The canonical explanation is [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

Correction to the earlier wording on this page: the source applies `lower()` to `user_bet`, not to `winning_color`. The captured turtle color comes from `pencolor()` and is compared directly with the lowercased user input.