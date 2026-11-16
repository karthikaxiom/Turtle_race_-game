# Dependency Boundary

The current `main.py` directly imports only two modules:

- `turtle`: screen setup, input dialog, turtle objects, positioning, movement, color access, and click-to-exit behavior.
- `random`: integer movement distance for each processed turtle turn.

Both are Python standard-library modules. The source does not import a third-party package, database client, web framework, network library, or application-specific module.

The standard-library status does not remove the graphical requirement: `turtle` relies on Tk support and a usable desktop display. A headless session may not open the game window. See [Runtime Dependencies](RUNTIME_DEPENDENCIES.md).