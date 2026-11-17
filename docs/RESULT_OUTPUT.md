# Result Output

The result messages are printed to the terminal with `print(...)`; they are not rendered inside the graphics window. The exact win/loss branches and message formats are maintained in [Output Branching](OUTPUT_BRANCHING.md).

The detected color is read from the turtle's `pencolor()` property. See [Winner Color Source](WINNER_COLOR_SOURCE.md) for the source of that value. The current implementation does not write a result file or persist a score.

## Output lifecycle

A result is emitted at the moment a qualifying turtle is checked, not deferred until after the loop. The program then continues the current list traversal and may emit another result. There is no final aggregation step that selects one message, stores a score, or writes a report.
