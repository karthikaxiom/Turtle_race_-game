# Module Responsibilities

The current implementation imports two Python standard-library modules.

## `turtle`

Used for screen creation and configuration, the startup text-input dialog, turtle objects, color and position methods, movement, and click-to-close behavior. The graphical interface depends on a desktop environment with Tk support.

## `random`

Used at each processed turtle turn to generate a movement distance:

```python
random.randint(0, 10)
```

Both endpoints are included. A zero draw is valid and leaves that turtle's position unchanged for that movement call.

No third-party package is imported by `main.py`. See [Imports](IMPORTS.md) and [Dependency Boundary](DEPENDENCY_BOUNDARY.md).
