# Screen Setup Sequence

The graphical screen is initialized before the input dialog and before any turtle objects are created.

The current sequence is:

1. Create the screen with `turtle.Screen()`.
2. Configure the window size to `800 × 400`.
3. Set the window title.
4. Show the text-input dialog.
5. Create the six turtle objects.
6. Enter the race loop when the returned input is truthy.
7. Call `screen.exitonclick()` after the race loop.

The screen therefore exists for the complete lifetime of the program, including the input stage and the final window-close stage.