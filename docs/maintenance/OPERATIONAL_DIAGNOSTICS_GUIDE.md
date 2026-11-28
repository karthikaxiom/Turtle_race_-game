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

## 7. Validate Python availability

Confirm that the intended Python interpreter launches and can import the standard-library modules used by the application. Distinguish interpreter selection problems from application logic.

## 8. Check GUI prerequisites

Verify that the machine has a usable graphical display and the Tk support required by Python's turtle module. A headless shell may not be able to open a turtle window.

## 9. Observe startup sequence

Note whether the window appears, whether the prompt appears, and which event happens first. Compare the observed order with the source initialization sequence.

## 10. Diagnose a missing prompt

Check whether the script reached the text-input call and whether a GUI dialog was hidden behind another window. Do not assume the prompt is terminal input.

## 11. Interpret an empty response

An empty or cancelled dialog result is falsey, so the race loop is skipped. The final screen click handler is still reached by normal control flow.
