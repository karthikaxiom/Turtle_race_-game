# Operational diagnostics guide

## 1. Diagnostic purpose

Use this guide to investigate a reported runtime issue without assuming that the visible symptom identifies its cause. Start with reproducible observations, compare them with the source, and record the environment in which the behavior occurred.


## 2. Record the symptom

Describe exactly what appeared, what action preceded it, and whether the program continued, stopped, or remained responsive. Preserve original error text where available.

## 3. Capture the environment

Record operating system, Python version, display session, terminal, and launch method. Turtle graphics depends on a functioning desktop GUI environment.

## 4. Confirm the launch target

Check the current directory and the exact script path used to launch the program. A similarly named copy can produce behavior that does not match the repository's current source.

## 5. Verify the source revision

Record the checked-out branch and commit identifier. Confirm that the file being executed belongs to the expected revision before comparing observed behavior with documentation.

## 6. Check working-tree changes

Inspect uncommitted modifications before diagnosing a defect. Local edits can change behavior without appearing in the committed source history.
