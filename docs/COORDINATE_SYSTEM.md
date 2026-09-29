# Race Coordinates

The current implementation uses the turtle graphics coordinate system directly.

## Screen

The screen is configured as 800 × 400 through:

```python
screen.setup(width=800, height=400)
```

## Starting coordinates

Every turtle starts at x = -370. Their vertical coordinates are -70, -40, -10, 20, 50, and 80 in the configured list order.

## Detection threshold

Winner detection checks whether the current turtle's x-coordinate is greater than 370. This is a logical coordinate used by the program; no separate finish-line object is drawn.

Movement changes the turtle's current coordinate through forward(...); the program does not maintain a separate position variable.
