# Graphics Window Lifecycle

The current program uses one turtle graphics screen for the entire launch.

The screen is created near the beginning with turtle.Screen(). Its size and title are configured before the input dialog is shown.

The same screen remains associated with the turtle objects while the program initializes and processes the movement loop.

After the loop finishes, the program calls:

```python
screen.exitonclick()
```

This final call keeps the graphics window available until a click. The implementation does not create a second screen or reopen the screen during the same launch.
