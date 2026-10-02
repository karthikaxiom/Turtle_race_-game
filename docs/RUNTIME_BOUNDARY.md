# Runtime Boundaries

The project has a small runtime boundary defined by the imports and the final window operation in `main.py`.

## Imported modules

The source imports only:

- Python's standard-library `turtle` module for the graphical window and turtle objects.
- Python's standard-library `random` module for movement distances.

No third-party package is imported by the program.

## Graphical runtime

The program creates a `turtle.Screen()` window, creates graphical turtle objects, and finishes with `screen.exitonclick()`.

The implementation therefore expects an environment capable of providing the graphical support required by Python's `turtle` module.

## Terminal output

The win/loss result is emitted with Python's `print(...)`, so that output belongs to the process's terminal/standard output rather than the graphics canvas.

No database, file-based save system, network service, or external runtime state is used by the current source.