# Result Input Comparison

The source compares `winning_color == user_bet.lower()`. The winner color comes from the detected turtle's pen color; lowercase conversion is applied only to the user's input.

No `strip()` call is made. The comparison ignores letter case in the guess but preserves leading and trailing whitespace. It occurs only after a turtle satisfies the finish check.

See [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) and [Output Branching](OUTPUT_BRANCHING.md).