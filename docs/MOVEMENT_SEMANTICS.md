# Movement Semantics

Each active pass iterates through `all_turtles` in list order. For each turtle, the program checks its current x-coordinate and then makes one movement call:

```python
turtle_.forward(random.randint(0, 10))
```

The distance is an integer from 0 through 10, inclusive, and a fresh random draw is made for each processed turtle turn.

## Consequences

- A draw of 0 leaves that turtle in its current position for that movement call.
- The movement call occurs after that turtle's finish-threshold check.
- A movement that takes a turtle beyond x = 370 is observed by a later finish check, not by an immediate post-movement check.
- The movement call still occurs in the current turn when the finish condition has just been detected.
- There is no explicit sleep or fixed delay in the race loop.
- The source does not seed Python's random-number generator. No repeatable seed is configured by the program.

These statements describe the movement mechanism. They do not guarantee that every launch produces a different outcome or identify which turtle will finish first.

Source of truth: `main.py` (`random.randint(0, 10)` and `forward()`).
