# Behavioral Verification Matrix

This matrix records reproducible checks for the current single-run Turtle Race implementation. These are verification scenarios, not claims that an automated test suite has run. When a scenario needs deterministic movement, substitute a controlled sequence for `random.randint` in an isolated test harness; do not change production behavior just to make a check pass.

## 01 — Screen dimensions and title

**Purpose:** Verify the initial window contract.

**Setup:** Launch the program in a desktop environment with Tk support.

**Check:** Before the input dialog appears, inspect the created screen configuration.

**Expected:** The screen is configured to 800 by 400 pixels and the title is exactly `Turtle Race ` (including its trailing space).

**Regression signal:** A changed size or title is a user-visible behavior change and should be reviewed explicitly.
