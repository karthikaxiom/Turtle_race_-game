# Race State Transitions

The boolean variable `race_on` controls whether another complete pass through the turtle collection may begin.

## Initialization

After all six turtle objects have been created and appended to `all_turtles`, the source assigns:

```python
race_on = True if user_bet else False
```

A truthy dialog result enables the race. A falsey result leaves it disabled; participant creation has already taken place by this point.

## Active processing

While `race_on` remains true, the outer `while` loop starts a pass through `all_turtles`. Each turtle is checked and then moved in list order.

## Finish transition

When a processed turtle already has an x-coordinate greater than `370`, the code sets `race_on` to false, captures its pen color, and prints a win/loss message. There is no assignment back to true and no replay transition in the current script.

Setting the flag to false does not stop the active inner `for` loop. The remainder of that pass can still produce additional checks, movement calls, and result messages. Only after the pass completes does the outer loop stop. See [Race Termination](RACE_TERMINATION.md) for the full consequence of this ordering.
