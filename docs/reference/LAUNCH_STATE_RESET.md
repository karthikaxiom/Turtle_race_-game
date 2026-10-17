# Launch State Reset

Each execution starts with fresh module-level state created by the script.

The turtle list is rebuilt, every turtle receives its configured starting position, and the race flag is initialized from the current startup input. No score, winner history, or previous turtle positions are persisted by the project.

As a result, restarting the script creates a new race state rather than continuing a previous run. This reference documents the existing one-launch lifecycle without changing game behavior.
