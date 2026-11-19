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

