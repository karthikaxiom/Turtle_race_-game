# Turtle Creation Loop

The program creates turtles with a single loop that runs six times.

For each iteration it:

1. creates a `turtle.Turtle` with the `"turtle"` shape;
2. assigns the color at the current index;
3. lifts the pen;
4. moves the turtle to x=`-370` and the indexed y-coordinate;
5. appends the object to `all_turtles`.

The loop count and both configuration lists therefore stay aligned through the shared index.
