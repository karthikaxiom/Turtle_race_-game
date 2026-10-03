# Input Normalization

The current implementation reads text from the startup dialog and stores the returned value in `user_bet`.

When comparing the selected value with a detected turtle color, the code calls:

`user_bet.lower()`

This makes the comparison case-insensitive. For example, uppercase or mixed-case color text can compare equal to the lowercase color assigned to a turtle.

The implementation does not call `.strip()`. Leading or trailing whitespace therefore remains part of the input and can prevent an otherwise matching color from comparing equal.

The normalization is applied only during the result comparison; the original input value is not rewritten before it is stored.