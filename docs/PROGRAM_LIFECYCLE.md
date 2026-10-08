# Program Lifecycle

`main.py` follows a single top-to-bottom execution path:

1. Import `turtle` and `random`.
2. Create and configure the graphics screen.
3. Define the turtle colors and starting y-coordinates.
4. Collect the user's text input.
5. Create six turtle objects, configure them, and store them in `all_turtles`.
6. Set the initial `race_on` state from the input result.
7. Run the race loop while `race_on` is true.
8. Keep the graphics window available with `screen.exitonclick()` after the race loop ends.

There is no separate application entry-point function; the script executes these stages in file order when launched.

Source of truth: `main.py`.
