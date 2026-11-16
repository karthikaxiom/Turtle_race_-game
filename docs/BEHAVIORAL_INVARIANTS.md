# Behavioral Invariants

The current program preserves these observable relationships during one launch:

- Six turtle objects are created, one for each paired color and lane entry.
- Every turtle starts at x = `-370`; its y-coordinate comes from the same index as its color.
- Each turtle's pen is lifted before it is positioned and moved.
- Collection order remains red, orange, yellow, green, blue, purple.
- A race begins only when the input dialog returns a truthy value.
- The race checks `xcor() > 370` before each movement call.
- The input is lowercased for comparison, but whitespace is not stripped.
- The result is printed to the terminal, not drawn in the Turtle window.

These are source-derived invariants, not promises about which turtle wins. Random movement can change the finishing order between runs.

## Review boundary

Compare proposed changes with `main.py` and verify that they preserve the relevant invariant or deliberately document a behavior change. Related: [Data Flow](DATA_FLOW.md), [Observable Behavior Checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md), and [Change Safe Zone](CHANGE_SAFE_ZONE.md).

## Practical review probes

- Inspect the six list entries in order and confirm that color and y-position are selected with the same index.
- Trace one active turn and confirm the coordinate read precedes the random movement call.
- Trace a finish-triggering turn and confirm that the flag change does not introduce an early exit from the inner traversal.
- Run with a falsey dialog result and confirm that setup still occurs before the race loop is skipped.

These probes check observable structure; they should not assert a particular random winner.
