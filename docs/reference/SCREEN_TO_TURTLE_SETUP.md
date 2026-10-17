# Screen-to-Turtle Setup

This reference records the setup order used by the current implementation.

1. Create the `turtle` screen.
2. Configure the screen size and title.
3. Collect the user's startup input.
4. Build the six turtle objects.
5. Assign each turtle its configured color and starting position.
6. Enter the race loop only when the input value is truthy.

The ordering matters because the screen and input dialog are established before the turtle list is constructed. The reference documents the existing program rather than changing its runtime behavior.
