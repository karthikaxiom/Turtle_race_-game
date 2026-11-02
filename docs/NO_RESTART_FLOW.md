# No-Restart Flow

The current program contains one startup input stage and one race loop for a single launch.

After the race state becomes false, control leaves the outer loop and proceeds to `screen.exitonclick()`. There is no second input dialog or explicit race-restart loop in the current source.
