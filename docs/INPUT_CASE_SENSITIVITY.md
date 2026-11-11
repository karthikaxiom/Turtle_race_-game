# Input Case Sensitivity

The result expression is `winning_color == user_bet.lower()`: it lowercases the user's stored input, not the captured winner color. No whitespace trimming is applied.

The canonical treatment of case conversion and the other input edge cases is [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).
