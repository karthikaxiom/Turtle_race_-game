# Result Branches

The canonical description of the win/loss comparison and the exact terminal message formats is [Output Branching](OUTPUT_BRANCHING.md).

The winner color source is maintained separately in [Winner Color Source](WINNER_COLOR_SOURCE.md). This separation keeps the comparison/output behavior distinct from the turtle property used to identify the detected finisher.

## Branch selection inputs

The branch condition compares the detected turtle's pen color with the lowercased guess. It does not compare against the original dialog string, and it does not validate the guess before the race. A whitespace-padded or unsupported guess therefore follows the non-match branch when a turtle is detected.
