# Manual Test Execution Protocol

This guide describes how to execute and record manual checks for the current Turtle Race program without changing its behavior. It complements the behavioral verification matrix: each entry focuses on test setup, observation quality, repeatability, or environment boundaries.

## Test record format

For every run, record the source revision, operating system, Python version, whether Tk is available, the exact input entered, the controlled or observed movement sequence, the visible result, and any terminal output. Distinguish an observed result from an expected result. Do not report a scenario as passed unless it was actually executed.

## 01 — Record the source revision

Before testing, capture the Git commit SHA associated with the source under test. This makes the test record traceable if the implementation changes later.

## 02 — Record the interpreter version

Capture the Python interpreter version used to launch the program. The project uses standard-library modules, but interpreter and GUI environment differences can still affect reproducibility.

## 03 — Record the operating system

Note the operating system and desktop session. Turtle graphics relies on a graphical environment, so a headless shell is not equivalent to a desktop run.

## 04 — Confirm Tk availability

Check that the Python installation can initialize Tk before interpreting a GUI startup failure as a race-logic defect. Record the exact error if the GUI toolkit is unavailable.

## 05 — Separate launch failures from race failures

Record whether the program fails before the input dialog, during turtle construction, inside the race loop, or during shutdown. The failure stage narrows the responsible subsystem.

## 06 — Use a fresh process for each independent case

Launch a new process for each independent scenario. The program is a single-run flow and does not expose an in-window reset or replay operation.


## 07 — Capture the exact input

Write down the exact characters submitted, including capitalization and spaces. A paraphrase such as “blue” is insufficient when the actual value contained whitespace or different casing.

## 08 — Keep one variable under test

Change only one condition between paired runs. For example, compare a plain supported color with the same color plus a trailing space, keeping the rest of the setup constant.

## 09 — Distinguish empty input from cancellation

Record whether the dialog was submitted empty or dismissed. Both are falsey paths in the current program, but the action taken by the tester should remain explicit in the evidence.

## 10 — Observe the startup sequence

Record the order in which the screen is created, the input dialog appears, and turtle objects are initialized. Do not infer the order solely from the final screen.

## 11 — Record participant order

List the six turtles in their creation order. This is the order used by the participant collection during each pass.

## 12 — Capture initial coordinates

Before the first movement pass, record each participant's x/y coordinates. Compare them with the configured common start and lane positions.

## 13 — Capture initial appearance

Record each turtle's shape, color, and pen state before movement. This provides a baseline for identifying visual initialization regressions.

## 14 — Use controlled movement for boundary checks

For exact threshold tests, use an isolated harness that supplies a predetermined movement result. Record the injected value and the turtle position before and after the call; do not claim a random run exercised a particular boundary by chance.

## 15 — Preserve the inclusive random interval

When testing the random-step contract, explicitly include both endpoints, zero and ten, plus at least one interior value. Record the requested draw, not merely the apparent visual distance.

## 16 — Verify each draw independently

Instrument the random function in a disposable harness and count calls during a pass. Compare the call sequence with the participant traversal order.

## 17 — Track positions at check time

For finish-condition scenarios, record each turtle's x-coordinate immediately before its finish comparison. A coordinate observed after movement does not establish what the preceding check saw.

## 18 — Distinguish equality from overshoot

Use separate cases at x = 370 and x = 371. Record them independently because the current finish test is strict greater-than.

## 19 — Observe one complete participant pass

Log the ordered sequence of participant checks and movement requests. This helps identify whether a change has altered traversal order.

## 20 — Continue observing after a finish flag change

When a turtle is detected, continue recording the remainder of that same pass. The current inner loop is not interrupted by setting the outer race flag false.

## 21 — Record every result message

Capture the exact terminal text, including the winning color and whether the message reports a win or loss. Do not replace the actual output with a summary alone.

## 22 — Identify the detected turtle

Record which turtle triggered the finish check and the pen color read at that point. Do not assume the first turtle in creation order must win.

## 23 — Test a matching guess

Pair a known detected color with an input whose lowercase form is identical. Verify the win branch and preserve the exact input string in the record.

## 24 — Test a non-matching guess

Use a non-matching input and a controlled detected turtle. Verify the loss branch and capture the reported color.

## 25 — Observe multiple detections in one pass

In a controlled harness, place more than one turtle beyond the threshold before their turns. Record the order and number of messages emitted during that pass.

## 26 — Check movement after detection

Instrument the movement call for a turtle that already satisfies the finish condition at the beginning of its turn. Record that the call still occurs after result evaluation.

## 27 — Check later participants in the same pass

After an early finish detection, verify whether later collection entries still receive their check and movement operations before the outer loop condition is reconsidered.

## 28 — Record terminal output separately from the GUI

Keep a terminal transcript or exact copied output separate from screenshots of the turtle window. The result messages are printed to the console, not drawn as labels in the graphics window.

## 29 — Verify the window remains interactive at shutdown

After the race loop completes or is skipped, observe the window and test the click-to-exit wait. Record whether the desktop event loop responds as expected.
