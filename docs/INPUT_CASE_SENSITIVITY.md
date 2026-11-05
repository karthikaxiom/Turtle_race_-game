# Input Case Sensitivity

The case-handling rule is maintained in [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).

The current source lowercases `user_bet` at comparison time. It does not lowercase the captured `winning_color` value in that expression, and it does not trim whitespace.