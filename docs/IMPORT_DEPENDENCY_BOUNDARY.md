# Import Dependency Boundary

The program imports two standard-library modules. `turtle` provides the graphical screen, input dialog, turtle objects, movement, and shutdown interaction. `random` provides the integer distance for each processed movement call.

No third-party package is imported by `main.py`. The graphical runtime still requires Tk support and a usable desktop display; this is an environment prerequisite rather than another project dependency.

See [Dependency Boundary](DEPENDENCY_BOUNDARY.md) and [Execution Prerequisites](EXECUTION_PREREQUISITES.md).