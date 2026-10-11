# Behavioral Invariants

The current program preserves a small set of observable relationships during a run:

- Each turtle is created from the paired `colors` and `y_positions` entries.
- Each turtle keeps its assigned color after initialization.
- A race remains active while no processed turtle has crossed the finish threshold.
- The selected input remains available for the final comparison.
- The program reports the winning turtle color when the race stops.

These invariants describe the behavior of the existing implementation without changing its source code.
