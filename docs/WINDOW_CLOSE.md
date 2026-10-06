# Window Close Behavior

After the race loop finishes, the program calls `screen.exitonclick()`.

This keeps the graphics window available for a click before the program exits, including when the race was not started because the input dialog returned a falsey value.
