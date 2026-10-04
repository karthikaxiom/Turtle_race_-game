# Documentation

This directory contains focused references for the current implementation in `main.py`.

## Program structure

- [Module Imports](IMPORTS.md) — the standard-library modules imported by the program.
- [Screen Dimensions](SCREEN_DIMENSIONS.md) — the configured graphical window size.
- [Color Order](COLOR_ORDER.md) — the six turtle colors and their list order.
- [Starting Positions](STARTING_POSITIONS.md) — the initial x/y coordinates and pen state.
- [Turtle Creation Loop](OBJECT_LOOP.md) — the sequence used to construct and store turtle objects.
- [Execution Flow](EXECUTION_FLOW.md) — startup, turtle creation, race loop, and shutdown sequence.
- [Input Behavior](INPUT_BEHAVIOR.md) — dialog values and how they affect race startup and result comparison.
- [Input Comparison](INPUT_COMPARISON.md) — how the entered text is normalized for result comparison.
- [Race Termination](RACE_TERMINATION.md) — the threshold check, same-pass behavior, and loop termination.
- [Output and Environment](OUTPUT_AND_ENVIRONMENT.md) — terminal messages and the runtime requirements for the graphical window.

## Implementation details

- [Configuration Constants](CONSTANTS_AND_CONFIGURATION.md) — fixed values used by the current implementation.
- [Turtle Object Creation](OBJECT_CREATION.md) — object construction and initial configuration.
- [Per-Turtle Turn Sequence](TURN_SEQUENCE.md) — operations performed for each turtle during a race pass.
- [Threshold Detection](THRESHOLD_DETECTION.md) — when the logical threshold is checked.
- [Random Movement Range](MOVEMENT_RANGE.md) — the integer range used for each movement.
- [Result Source](RESULT_SOURCE.md) — where the reported winning color comes from.
- [Runtime Boundary](RUNTIME_BOUNDARY.md) — what happens inside and after the race loop.
- [Data Flow](DATA_FLOW.md) — movement and result data flow through the program.
- [Collection Traversal](COLLECTION_TRAVERSAL.md) — traversal of the turtle collection.
- [Position Ownership](POSITION_OWNERSHIP.md) — which objects hold turtle positions.
- [Rendering and Output](RENDERING_AND_OUTPUT.md) — graphical and terminal output paths.
- [Source Footprint](SOURCE_FOOTPRINT.md) — the small implementation footprint of the program.
- [Loop Responsibilities](LOOP_RESPONSIBILITIES.md) — responsibilities of the major loops.
- [Screen Configuration](SCREEN_CONFIGURATION.md) — screen setup behavior.
- [Turtle Configuration](TURTLE_CONFIGURATION.md) — per-turtle configuration.
- [Movement Semantics](MOVEMENT_SEMANTICS.md) — movement behavior.
- [State Variables](STATE_VARIABLES.md) — key runtime state variables.
- [Control Flow](CONTROL_FLOW.md) — major control-flow boundaries.
- [Module Responsibilities](MODULE_RESPONSIBILITIES.md) — responsibilities of imported modules and program code.
- [Race Coordinates](RACE_COORDINATES.md) — coordinate values used by the race.
- [Initialization Order](INITIALIZATION_ORDER.md) — startup and initialization ordering.
- [Turtle List Storage](TURTLE_LIST_STORAGE.md) — how turtle objects are retained.
- [Graphics Window Lifecycle](GRAPHICS_WINDOW_LIFECYCLE.md) — creation and closing behavior.
- [Input Normalization](INPUT_NORMALIZATION.md) — input normalization behavior.
- [List Indexing](LIST_INDEXING.md) — indexed relationship between configuration lists.
- [Pen State](PEN_STATE.md) — turtle pen-state behavior.
- [Screen Setup Sequence](SCREEN_SETUP_SEQUENCE.md) — screen setup ordering.
- [State Transitions](STATE_TRANSITIONS.md) — race-state transitions.
- [Dependency Boundary](DEPENDENCY_BOUNDARY.md) — dependency boundary of the current program.

These notes describe the current code rather than planned features.
