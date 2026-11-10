# Input Whitespace Behavior

The current source lowercases `user_bet` at comparison time but does not call `strip()`. Leading or trailing spaces therefore remain and can prevent an otherwise matching color from comparing equal.

See [Input Normalization Boundary](../INPUT_NORMALIZATION_BOUNDARY.md) for the full comparison contract.