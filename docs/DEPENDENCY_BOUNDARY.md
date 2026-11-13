# Dependency Boundary

The current `main.py` has two direct imports:

- `turtle`
- `random`

Both are Python standard-library modules. `turtle` provides the screen, input dialog, turtle objects, positioning, movement, color handling, and click-to-exit behavior. `random` supplies the integer movement distance for each processed turtle turn.

The source does not import application-specific modules, third-party packages, database clients, web frameworks, or network libraries. No third-party installation step is implied by these two imports alone.

There is still an environment requirement: the `turtle` module depends on a working Tk-based graphical environment. A Python installation without the required GUI support, or a session without a usable display, may not be able to open the game window. See [Runtime Dependencies](RUNTIME_DEPENDENCIES.md) for the user-facing runtime prerequisite.
