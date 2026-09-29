# Turtle List Storage

The current implementation uses all_turtles as the collection for the six turtle objects.

The list is created before the initialization loop:

```python
all_turtles = []
```

Each newly configured turtle is appended to the list. The same list is then consumed by the inner for-loop in its stored order.

No second collection is created for the turtle objects, and the list is not written to persistent storage.
