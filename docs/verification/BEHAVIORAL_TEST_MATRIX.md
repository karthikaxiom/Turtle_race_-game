# Behavioral Verification Matrix

This matrix records reproducible checks for the current single-run Turtle Race implementation. These are verification scenarios, not claims that an automated test suite has run. When a scenario needs deterministic movement, substitute a controlled sequence for `random.randint` in an isolated test harness; do not change production behavior just to make a check pass.

## 01 — Screen dimensions and title

**Purpose:** Verify the initial window contract.

**Setup:** Launch the program in a desktop environment with Tk support.

**Check:** Before the input dialog appears, inspect the created screen configuration.

**Expected:** The screen is configured to 800 by 400 pixels and the title is exactly `Turtle Race ` (including its trailing space).

**Regression signal:** A changed size or title is a user-visible behavior change and should be reviewed explicitly.

## 02 — Participant count and collection size

**Check:** Confirm that a non-empty guess leads to exactly six turtle objects being appended to the participant list. A different count can break the parallel color/position mapping or leave a lane absent.

**Result recording:** Mark this scenario pass/fail against the current source without silently normalizing or correcting the observed behavior.

## 03 — Color-to-lane pairing

**Check:** Inspect participants in creation order. Expected pairs are red/-70, orange/-40, yellow/-10, green/20, blue/50, and purple/80. Reordering either configuration list changes the pairing.

**Result recording:** Mark this scenario pass/fail against the current source without silently normalizing or correcting the observed behavior.

## 04 — Shared starting x-coordinate

**Check:** Before the first movement pass, compare all participants' x-coordinates. Each must begin at -370; only their y-coordinates differ. A staggered start would be a visible behavior change.

**Result recording:** Mark this scenario pass/fail against the current source without silently normalizing or correcting the observed behavior.

## 05 — Turtle shape and pen state

**Check:** Inspect each participant after initialization. Every turtle uses the turtle shape and has its pen lifted before placement, preventing movement trails.

**Result recording:** Mark this scenario pass/fail against the current source without silently normalizing or correcting the observed behavior.

## 06 — Input dialog precedes participant creation

**Check:** Pause at startup and verify that the text-input dialog is requested before the participant-creation loop. Moving the dialog later changes the startup sequence.

**Result recording:** Mark this scenario pass/fail against the current source without silently normalizing or correcting the observed behavior.
