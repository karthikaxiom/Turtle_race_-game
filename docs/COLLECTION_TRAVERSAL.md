# Collection Traversal

`all_turtles` is the single participant collection. The creation loop appends each configured turtle once, and the race loop traverses the same list:

```python
for turtle_ in all_turtles:
    ...
```

The list order is red, orange, yellow, green, blue, purple. Each color is paired with the y-coordinate at the same index.

## Per-pass contract

For every entry in a pass, the program checks the current x-coordinate, handles a qualifying finish, then calls `forward(random.randint(0, 10))`.

There is no `break` after `race_on` becomes false. Python continues the current `for` traversal; later entries can also be checked and can print another result. The outer `while` condition is tested again only after that traversal ends.

The collection is not reordered during a race. See [Iteration Order](ITERATION_ORDER.md), [Inner Loop Continuation](INNER_LOOP_CONTINUATION.md), and [Race Termination](RACE_TERMINATION.md).
