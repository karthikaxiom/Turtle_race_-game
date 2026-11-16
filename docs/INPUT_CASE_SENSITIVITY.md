# Input Case Sensitivity

The result expression is `winning_color == user_bet.lower()`. The lowercase conversion applies to the user's stored input; the detected turtle color is obtained separately from `pencolor()`.

Uppercase or mixed-case entries can match the lowercase configured colors. Leading and trailing spaces remain and prevent equality. This case conversion is not color validation: any truthy text still enables the race.

See [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).