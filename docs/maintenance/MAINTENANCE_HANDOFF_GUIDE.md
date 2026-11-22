# Maintenance Handoff Guide

A practical handoff reference for reviewing, maintaining, and documenting the current Turtle Race implementation. This guide complements the behavior-focused pages in the documentation index; it does not override `main.py` or turn future ideas into current features.

## 01. Purpose and audience

This guide supports a maintainer taking over a small, source-led Turtle graphics project. It is a handoff aid, not a replacement for the implementation or canonical behavior pages. Use it to establish what is known, what must be checked, and what should remain untouched until evidence exists.

## 02. Authoritative evidence

Treat the checked-out `main.py` as the authority for current runtime behavior. Documentation, screenshots, commit messages, and recollections are secondary evidence. If they disagree with the source, record the discrepancy and verify whether the source or description is stale.

## 03. Establish the revision

Record the branch name, full commit identifier, working-tree state, and inspection date. A handoff without a revision is ambiguous: later readers cannot tell whether observations describe the same code they are reviewing.

## 04. Separate facts from assumptions

Label statements as observed, inferred, proposed, or unknown. A visible dialog is observed behavior; an assumption about how a user will respond is not. Do not turn a plausible expectation into a guaranteed product property.

## 05. Confirm the launch environment

Check the Python interpreter and whether a graphical desktop session is available. The program uses standard-library `turtle` and `random`, while graphics depend on host Tk support. A successful import alone does not prove a window can be displayed.

## 06. Record launch instructions

Use current setup instructions and verify them against the source. Keep commands minimal and platform-aware. If a command has only been tested on one operating system or desktop environment, state that limitation.

## 07. Capture startup order

Follow the actual statement order: screen setup, input dialog, turtle construction, race-state initialization, loop, and shutdown. The dialog occurs before participant construction, and its return value determines whether the loop runs.

## 08. Describe input precisely

The current program compares the lowercased answer with the winning color; it does not trim surrounding whitespace or validate the answer against the configured palette. Do not describe stricter validation unless code is added and tested.

## 09. Handle cancellation carefully

An empty or cancelled input produces a false race-state value, so the movement loop is skipped. The screen shutdown call still follows. Distinguish this path from a completed race and from an unsupported non-empty guess.

## 10. Keep participant configuration aligned

The six configured colors and six vertical positions are paired by list index during turtle creation. If either list changes, verify their lengths and intended correspondence. Describe the current ordering from source, not a screenshot.

## 11. Explain initial placement

Each participant begins at the same horizontal coordinate and receives its configured vertical lane. The pen is lifted before placement, so initialization does not draw a trail. Distinguish initial placement from later movement.

## 12. Explain movement bounds

Each loop visit requests a random integer from zero through ten, inclusive, and moves that turtle forward by the returned amount. Do not claim fixed speed, equal distance per turn, or a deterministic winner.

## 13. Preserve check-before-move semantics

The finish comparison is evaluated before the current visit's movement. A turtle that crosses the threshold during movement is not reported until its next visit. Do not simplify this into an after-move check.

## 14. Describe the strict threshold

The source tests whether horizontal position is greater than 370, not greater than or equal to 370. Equality does not satisfy the current condition; preserve this distinction in documentation and test cases.

## 15. Account for same-pass processing

Setting the outer race flag to false does not break the inner `for` loop. Remaining turtles in that pass are still visited and moved, and another turtle may also satisfy the finish condition. Do not claim an immediate stop at the first detection.

## 16. Interpret result messages

The result branch compares the detected turtle's pen color with the lowercased raw guess and prints a win or loss message. It writes to the terminal; it does not render a result panel in the turtle window.

## 17. Avoid overstating winner guarantees

Random increments and delayed detection mean the observed message sequence follows loop order and current coordinates. Explain the mechanism rather than claiming a statistically fair or simultaneous finish.

## 18. Understand shutdown behavior

The program calls `screen.exitonclick()` after the race loop or after the loop is skipped. This is a click-to-close interaction for the graphics window. Do not describe automatic closure or replay controls.

## 19. Inventory dependencies honestly

The source imports only `turtle` and `random`, both from Python's standard library. The graphics runtime may still require platform components such as Tk. Do not invent third-party dependencies.

## 20. Keep test evidence reproducible

For a manual check, record revision, environment, input, observed output, and whether the graphics window behaved as expected. Random movement means one run cannot establish every possible ordering or edge case.

## 21. Use controlled test reasoning

Where practical, isolate behavior with a small test harness or reasoned input/coordinate cases without changing the production entrypoint. Mark simulated observations as simulations, not as unmodified end-to-end runs.

## 22. Review documentation links

Open every new relative link from the documentation index. Check spelling, case, path, and target existence. A correct paragraph with a broken navigation link is still incomplete documentation.

## 23. Review claims against source

Search for claims about validation, persistence, replay, scoring, timing, and GUI output. These are common areas where documentation drifts beyond implementation. Remove unsupported claims or label future ideas as proposals.

## 24. Keep maintenance changes scoped

Prefer one coherent documentation topic per change. Avoid combining unrelated source edits, formatting sweeps, generated artifacts, and behavior changes. Narrow scope makes review and rollback easier.

## 25. Inspect the final diff

Review the complete diff for accidental deletions, duplicated sections, malformed Markdown, inconsistent terminology, and unrelated files. Confirm the intended file list matches the stated scope.

## 26. Record known limitations

The current implementation has no replay workflow, persistent score storage, configurable participant count, or graphical result summary. Keep limitations tied to the inspected revision and avoid implying these are permanent design decisions.

## 27. Prepare a useful handoff summary

Name the inspected revision, files changed, checks performed, known limitations, and unresolved questions. A concise handoff should let the next maintainer continue without reconstructing the investigation from the entire commit history.
