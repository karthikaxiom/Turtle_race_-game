# Runtime Dependencies

The game imports Python's standard library only. Its direct runtime modules are:

- `turtle` — creates the graphics screen, startup input dialog, turtle objects, and window lifecycle.
- `random` — generates the per-turn forward distance supplied to each turtle.

## Platform requirement

The `turtle` module uses Tk for its graphical interface. Running the script therefore requires a Python environment with Tk support and access to a usable desktop display. A headless terminal alone is not sufficient to display the race window.

## Installation boundary

No third-party Python package is imported by `main.py`, so there is no project-specific package installation step for the imports currently used. This does not guarantee that every Python distribution includes GUI support; Tk availability is an environment prerequisite rather than an extra package imported by the script.

The source does not contain a web renderer or headless fallback. See [Dependency Boundary](DEPENDENCY_BOUNDARY.md) for the import list and [Output and Environment](OUTPUT_AND_ENVIRONMENT.md) for where messages appear.
