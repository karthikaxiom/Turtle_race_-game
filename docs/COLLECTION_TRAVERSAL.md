# Collection Traversal

The race uses the all_turtles list as its single turtle collection.

The inner loop traverses that list directly:

```python
for turtle_ in all_turtles:
    ...
```

The list order is the creation order: red, orange, yellow, green, blue, purple.

Each traversal step performs the threshold check and then the movement call for the current object. The current implementation does not sort, shuffle, reverse, or otherwise reorder the list during the race.
