# Documentation

This directory explains the behavior of the current implementation in `main.py`. The source is authoritative; these pages describe and help review what the script actually does. Start with the lifecycle overview, then use the focused guides for a particular concern.

## Start here

- [Program lifecycle](PROGRAM_LIFECYCLE.md) — the complete top-to-bottom execution path and its two startup outcomes.
- [Observable behavior checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md) — manual checks for behavior visible in the current source.
- [Control flow boundaries](CONTROL_FLOW.md) — the nested loops and where execution continues after a finish check.
- [Data flow](DATA_FLOW.md) — how the input, configuration, turtle objects, and result values move through the script.
- [Safe documentation changes](CHANGE_SAFE_ZONE.md) — boundaries for documentation-only maintenance.
- [Documentation rules](DOCUMENTATION_RULES.md) — how to maintain canonical pages and avoid duplicate notes.
- [Contribution guide](../CONTRIBUTING.md) — repository-level expectations for code and documentation changes.

## Setup and input

- [Execution prerequisites](EXECUTION_PREREQUISITES.md) — Python and graphical runtime requirements.
- [Runtime dependencies](RUNTIME_DEPENDENCIES.md) — the modules and GUI support used by the program.
- [Screen configuration](SCREEN_CONFIGURATION.md) — window dimensions and title.
- [Initialization sequence](INITIALIZATION_SEQUENCE.md) — ordering of setup stages.
- [Input lifecycle](INPUT_LIFECYCLE.md) — the dialog and how its return value affects execution.
- [Input normalization boundary](INPUT_NORMALIZATION_BOUNDARY.md) — case conversion, whitespace, and unsupported values.

## Turtles and movement

- [Turtle configuration](TURTLE_CONFIGURATION.md) — creation, appearance, pen state, and placement.
- [Color mapping](COLOR_MAPPING.md) — the configured colors and their participant order.
- [Starting positions](STARTING_POSITIONS.md) — the horizontal start and vertical lanes.
- [Collection traversal](COLLECTION_TRAVERSAL.md) — the order in which turtle objects are processed.
- [Movement semantics](MOVEMENT_SEMANTICS.md) — random movement and per-turn ordering.
- [Determinism boundary](DETERMINISM_BOUNDARY.md) — fixed configuration versus random progression.

## Results and shutdown

- [Threshold detection timing](THRESHOLD_DETECTION.md) — the strict finish comparison and when it is evaluated.
- [Race termination](RACE_TERMINATION.md) — same-pass processing and the end of the outer loop.
- [Output branching](OUTPUT_BRANCHING.md) — win/loss selection and terminal messages.
- [Output and environment](OUTPUT_AND_ENVIRONMENT.md) — the terminal and graphics output surfaces.
- [Screen shutdown](SCREEN_SHUTDOWN.md) — the final click-to-close behavior.

## Supplementary records

- [Reference notes](reference/README_SCOPE.md) — scope of the focused notes in `reference/`.
- [Dated maintenance notes](maintenance/) — chronological records of earlier documentation maintenance.

When pages overlap, prefer the maintained overview linked above and check `main.py` before treating any statement as current. Reference notes are supplementary, and dated maintenance records are historical rather than behavioral specifications.
