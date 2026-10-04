# Shutdown

After the race loop finishes, the program calls `screen.exitonclick()`.

This keeps the graphical window available until a click closes it. The call occurs after the race loop rather than inside the loop, so it is reached after normal race completion as well as after the race state becomes false without a separate early window-close path.
