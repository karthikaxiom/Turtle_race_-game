# Position Ownership

The current program does not keep a separate x-coordinate variable for each turtle.

Instead, each turtle object maintains its current position internally. The race loop reads that state through:

```python
turtle_.xcor()
```

Movement is applied directly to the same object with:

```python
turtle_.forward(...)
```

The winner threshold is therefore evaluated against the turtle object's current graphical position rather than against a separately maintained numeric position table.
