# Loop Responsibilities

The current race logic has two nested loops.

## Outer while loop

The outer loop uses race_on as its continuation condition. It controls whether another complete pass over the turtle collection can begin.

## Inner for loop

The inner loop visits each object in all_turtles once in list order. For each object it:

1. reads the current x-coordinate,
2. checks the winner threshold,
3. updates race_on when the threshold is satisfied,
4. prints the corresponding result,
5. performs the movement call.

The inner loop itself has no break statement. Therefore changing race_on does not interrupt the remaining iterations of the current inner pass.
