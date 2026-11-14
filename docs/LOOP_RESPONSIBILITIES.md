# Loop Responsibilities

The current race logic has two nested loops.

## Outer `while` loop

The outer loop uses `race_on` as its continuation condition. It controls whether another complete pass over the turtle collection can begin.

## Inner `for` loop

The inner loop visits each object in `all_turtles` once in list order. For each object it:
1. reads the current x-coordinate;
2. checks the strict finish threshold;
3. updates `race_on` and prints a result when the check succeeds;
4. calls the movement method.

The inner loop has no `break`. Changing `race_on` does not interrupt the remaining iterations of the current pass. The outer condition is checked only after the inner loop completes.
