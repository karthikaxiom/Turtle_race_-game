# Program Shutdown

After the race loop finishes, the program calls `screen.exitonclick()`. This keeps the turtle graphics window available until the user clicks it, including when the race was skipped because no input was supplied.
