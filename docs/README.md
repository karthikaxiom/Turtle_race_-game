# Documentation

This directory explains the behavior of the current implementation in `main.py`. Start with the lifecycle overview, then use the focused pages below when investigating a particular part of the program.

## Start here

- [Program lifecycle](PROGRAM_LIFECYCLE.md) — the top-to-bottom execution path.
- [Observable behavior checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md) — manual checks for the behavior currently visible in the source.
- [Safe documentation changes](CHANGE_SAFE_ZONE.md) — boundaries for documentation-only maintenance.
- [Documentation rules](DOCUMENTATION_RULES.md) — how to add or update pages without creating duplicate notes.

## Setup and input

- [Execution prerequisites](EXECUTION_PREREQUISITES.md) — Python and graphical runtime requirements.
- [Runtime dependencies](RUNTIME_DEPENDENCIES.md) — the modules used by the program.
- [Screen configuration](SCREEN_CONFIGURATION.md) — window dimensions and setup.
- [Initialization sequence](INITIALIZATION_SEQUENCE.md) — ordering of setup stages.
- [Input lifecycle](INPUT_LIFECYCLE.md) — the input dialog and how its value affects the run.
- [Input normalization boundary](INPUT_NORMALIZATION_BOUNDARY.md) — what is and is not normalized.
- [Input whitespace](INPUT_WHITESPACE.md) — the effect of leading and trailing spaces.

## Turtles and movement

- [Turtle initial state](TURTLE_INITIAL_STATE.md) — creation, appearance, pen state, and starting position.
- [Color mapping](COLOR_MAPPING.md) — the configured colors and their relationship to turtle order.
- [Collection traversal](COLLECTION_TRAVERSAL.md) — how turtle objects are visited.
- [Movement semantics](MOVEMENT_SEMANTICS.md) — random movement and its per-turn behavior.
- [Finish-check timing](FINISH_CHECK_TIMING.md) — when the threshold is evaluated.
- [Threshold overshoot](THRESHOLD_OVERSHOOT.md) — why a turtle can move beyond the logical finish threshold.

## Results and shutdown

- [First detected finish](FIRST_DETECTED_FINISH.md) — finish detection during a pass through the turtle list.
- [Post-finish movement](POST_FINISH_MOVEMENT.md) — movement calls that still occur after a finish check.
- [Output branching](OUTPUT_BRANCHING.md) — how the program chooses its win or loss message.
- [Winner color source](WINNER_COLOR_SOURCE.md) — where the reported color is read from.
- [Screen shutdown](SCREEN_SHUTDOWN.md) — the final click-to-close behavior.

## Supplementary records

- [Reference notes](reference/README_SCOPE.md) — scope of the focused notes in `reference/`.
- [Dated maintenance notes](maintenance/) — chronological records of earlier documentation maintenance.

The focused notes are not all equally authoritative. When two older pages overlap, use `main.py` as the source of truth and prefer the clearest current explanation. See [Documentation rules](DOCUMENTATION_RULES.md) before adding another page.
