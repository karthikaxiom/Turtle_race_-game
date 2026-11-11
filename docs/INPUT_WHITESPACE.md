# Input Whitespace

The result comparison lowercases `user_bet` but does not call `strip()`. Leading or trailing spaces therefore remain part of the input and prevent an otherwise matching color name from comparing equal.

The canonical input edge-case reference is [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md).
