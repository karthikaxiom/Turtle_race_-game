# Determinism Boundary

The fixed parts of a run are determined by the source configuration: the number of turtles, their colors, their starting positions, the screen dimensions, and the movement call used for each turn.

The movement distance is generated with Python's `random.randint(0, 10)`, so the exact race progression is not predetermined from the source alone.

This boundary explains why the same program structure can produce different race outcomes across launches without any source-code change.
