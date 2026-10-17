# Input Normalization Boundary

The startup bet is stored as the value returned by `screen.textinput(...)`.

When a winner is detected, the comparison uses `user_bet.lower()`. This means letter case does not affect a normal color-name comparison. The implementation does not call `.strip()`, so leading or trailing whitespace remains part of the stored value and can prevent an otherwise matching color from comparing equal.

The documentation reflects the current boundary: case is normalized at comparison time, while whitespace is not.
