# Result Input Comparison

The maintained comparison expression is documented in [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

Correction to the earlier wording on this page: the source compares `winning_color == user_bet.lower()`. It lowercases the user's stored input, not the captured winner color. The comparison runs only after a turtle satisfies the finish threshold.