# Output Branching

When a turtle is already beyond the finish threshold at the start of its turn, the program captures its current pen color:

```python
winning_color = turtle_.pencolor()
```

It then compares that value with `user_bet.lower()`:

- A match prints `You've won! The <color> turtle is the winner!`
- A non-match prints `You've lost! The <color> turtle won.`

The result is sent to standard output with `print(...)`; it is not drawn inside the graphics window. The displayed color is read from the detected turtle's pen color, rather than from the user's input.

## Multiple detections in one pass

Printing a result does not break the inner `for` loop. If a later turtle in the same pass is also already beyond the threshold when checked, it is compared and reported as well. Each qualifying turtle can therefore produce its own message in list order, and `winning_color` is assigned again for that later turtle.

The source does not maintain a separate immutable winner record or suppress later messages. See [Race Termination](RACE_TERMINATION.md) for the loop ordering and [Input Normalization Boundary](INPUT_NORMALIZATION_BOUNDARY.md) for the comparison details.

Source of truth: `main.py`.
