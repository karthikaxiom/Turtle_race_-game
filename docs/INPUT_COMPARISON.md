# Result Input Comparison

When a turtle crosses the logical threshold, the program stores that turtle's pen color in `winning_color`.

The result comparison then uses:

`winning_color == user_bet.lower()`

This means the entered text is converted to lowercase for the comparison, while the turtle's color is already represented by lowercase color names.

The comparison is performed only after a turtle satisfies the threshold condition.
