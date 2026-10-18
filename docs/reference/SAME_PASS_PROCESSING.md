# Same-Pass Processing

When a turtle triggers the finish condition, `race_on` becomes false, but the current `for` pass continues. Later turtles in that pass are still checked and moved before the outer loop ends.
