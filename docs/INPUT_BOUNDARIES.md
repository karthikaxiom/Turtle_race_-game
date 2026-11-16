# Input Boundaries

The input flow has two distinct boundaries.

## Startup activation

The dialog return value is stored in `user_bet`. After turtle setup, its truthiness initializes `race_on`. A falsey result skips the race loop; a truthy value starts it even when the text is not a configured color.

## Result comparison

When a turtle is detected beyond the threshold, the program compares its pen color with `user_bet.lower()`. The input is lowercased but not stripped, and no startup validation is performed.

See [Input Lifecycle](INPUT_LIFECYCLE.md) and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).