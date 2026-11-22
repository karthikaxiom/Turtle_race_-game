# Maintenance Handoff Guide

A practical handoff reference for reviewing, maintaining, and documenting the current Turtle Race implementation. This guide complements the behavior-focused pages in the documentation index; it does not override `main.py` or turn future ideas into current features.

## 01. Purpose and audience

This guide supports a maintainer who is taking over a small, source-led Turtle graphics project. It is a handoff aid, not a replacement for the implementation or the canonical behavior pages. Use it to establish what is known, what must be checked, and what should remain untouched until evidence exists.

## 02. Authoritative evidence

Treat the checked-out `main.py` as the authority for current runtime behavior. Documentation, screenshots, commit messages, and recollections are secondary evidence. If they disagree with the source, record the discrepancy and verify whether the source or the description is stale before changing either.

## 03. Establish the revision

Record the branch name, full commit identifier, working-tree state, and date of inspection. A handoff without a revision is ambiguous: later readers cannot tell whether observations describe the same code they are reviewing.

## 04. Separate facts from assumptions

Label statements as observed, inferred, proposed, or unknown. For example, a visible dialog is observed behavior; an assumption about how a user will respond is not. Do not turn a plausible expectation into a guaranteed product property.

## 05. Confirm the launch environment

Check the Python interpreter and whether a graphical desktop session is available. The program uses the standard-library `turtle` and `random` modules, while the graphics stack depends on the host's Tk support. A successful import alone does not prove that a window can be displayed.

## 06. Record launch instructions

Use the repository's current setup instructions and verify them against the present source. Keep commands minimal and platform-aware. If a command has only been tested on one operating system or desktop environment, state that limitation rather than implying universal support.

## 07. Capture startup order

When explaining startup, follow the actual statement order: screen setup, input dialog, turtle construction, race-state initialization, loop, and shutdown. Ordering matters because the dialog occurs before participant construction and the input result determines whether the loop runs.

## 08. Describe input precisely

Document the input as it is implemented. The current program compares the lowercased answer with the winning color; it does not trim surrounding whitespace or validate the answer against the configured palette. Do not describe stricter validation unless code is added and tested.

## 09. Confirm the launch environment

Check the Python interpreter and whether a graphical desktop session is available. The program uses the standard-library `turtle` and `random` modules, while the graphics stack depends on the host's Tk support. A successful import alone does not prove that a window can be displayed.

## 10. Record launch instructions

Use the repository's current setup instructions and verify them against the present source. Keep commands minimal and platform-aware. If a command has only been tested on one operating system or desktop environment, state that limitation rather than implying universal support.

## 11. Capture startup order

When explaining startup, follow the actual statement order: screen setup, input dialog, turtle construction, race-state initialization, loop, and shutdown. Ordering matters because the dialog occurs before participant construction and the input result determines whether the loop runs.

## 12. Describe input precisely

Document the input as it is implemented. The current program compares the lowercased answer with the winning color; it does not trim surrounding whitespace or validate the answer against the configured palette. Do not describe stricter validation unless code is added and tested.

## 13. Handle cancellation carefully

An empty or cancelled input produces a false race-state value, so the movement loop is skipped. The screen shutdown call still follows. Distinguish this path from a completed race and from an unsupported non-empty guess.

## 14. Keep participant configuration aligned

The six configured colors and six vertical positions are paired by list index during turtle creation. If either list changes, verify that their lengths and intended correspondence remain aligned. Describe the current ordering from source rather than relying on a screenshot.

## 15. Explain initial placement

Each participant begins at the same horizontal coordinate and receives its own configured vertical lane. The pen is lifted before placement, so initialization does not draw a trail. A visual description should distinguish initial placement from later movement.

## 16. Explain movement bounds

Each loop visit requests a random integer from zero through ten, inclusive, and moves that turtle forward by the returned amount. Do not claim a fixed speed, equal distance per turn, or deterministic winner.

## 17. Preserve check-before-move semantics

The finish comparison is evaluated before the current visit's movement. A turtle that crosses the threshold during a movement is not reported until its next visit. This timing is a meaningful observable detail and should not be simplified into an after-move check.
