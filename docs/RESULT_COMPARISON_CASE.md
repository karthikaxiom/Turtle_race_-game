# Result Comparison Case

The canonical comparison details are maintained in [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

Correction to the earlier wording: the source does not lowercase the detected winner color. The expression is `winning_color == user_bet.lower()`, so the user's text is lowercased and compared with the captured turtle color.