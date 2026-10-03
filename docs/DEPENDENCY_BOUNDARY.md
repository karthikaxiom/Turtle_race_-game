# Dependency Boundary

The current source has two direct imports:

- `turtle`
- `random`

Both are Python standard-library modules.

The program does not import application-specific modules, third-party packages, database clients, web frameworks, or network libraries.

The `turtle` dependency provides the screen, input dialog, turtle objects, positioning, movement, color handling, and final click-to-exit behavior used by the program.

The `random` dependency supplies the integer movement distance for each turtle turn.

No package installation step is represented in the current source, and no dependency manifest is required for these two imports alone.