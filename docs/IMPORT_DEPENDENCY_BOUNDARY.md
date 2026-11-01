# Import Dependency Boundary

The game imports two standard-library modules at startup:

- `turtle` provides the screen, turtle objects, input dialog, movement, and shutdown interaction.
- `random` provides the per-move distance used during the race.

No third-party package is required by the current `main.py` implementation. The import boundary therefore matches the runtime features used by the game.