# Module Imports

The current `main.py` imports two Python standard-library modules:

- `turtle` provides the graphical screen, turtle objects, text-input dialog, movement methods, and click-to-close behavior.
- `random` provides the integer draw used as each movement distance.

The movement expression is `random.randint(0, 10)`, whose endpoints are inclusive. No third-party package is imported by the current source.

The graphical interface requires a desktop environment with the Tk support used by Python's `turtle` module. See [Import Responsibilities](IMPORT_RESPONSIBILITIES.md), [Dependency Boundary](DEPENDENCY_BOUNDARY.md), and [Execution Prerequisites](EXECUTION_PREREQUISITES.md).
