# Verification Evidence Ledger

A structured reference for collecting, describing, and reviewing evidence about the current Turtle Race implementation. It helps keep source facts, observed behavior, inferences, and future proposals distinct. It is not itself proof that any particular test has been run.

## 01. Purpose and scope

This ledger gives maintainers a consistent way to record evidence for claims about the Turtle Race project. It is a review aid, not a test report and not a substitute for inspecting the implementation. Complete only the entries that apply to a change; leave unsupported items explicitly unknown.

## 02. Evidence vocabulary

Use four labels consistently: observed means directly seen during a check; source-confirmed means visible in the inspected implementation; inferred means reasoned from evidence but not directly exercised; proposed means future work. Do not mix these categories in a single unqualified claim.

## 03. Revision identity

Record the full commit SHA, branch, and inspection date before collecting evidence. If the working tree contains uncommitted changes, record that fact and identify the affected paths so another reviewer can reproduce the same state.

## 04. Source of truth

For current behavior, inspect `main.py` at the recorded revision. Treat screenshots, old notes, README wording, and commit messages as supporting context only. Resolve contradictions against the source rather than silently choosing the more convenient description.

## 05. Environment record

Record the operating system, Python version, desktop session, and availability of Tk support when testing the graphical program. A successful source review does not establish that a GUI can open in every runtime environment.

## 06. Interpreter provenance

Capture which Python executable ran the program and how its version was obtained. Avoid assuming that the `python` command resolves to the same interpreter across shells, virtual environments, and operating systems.

## 07. Dependency evidence

The inspected source imports `turtle` and `random`, both standard-library modules. Record any platform graphics prerequisites separately; do not report Tk as a third-party Python package dependency without checking the environment.

## 08. Launch-path evidence

Record the exact launch command and working directory used for a manual run. If the launch procedure differs between Windows, Linux, or a remote shell, keep separate evidence rather than presenting one command as universally portable.

## 09. GUI availability

Mark whether a graphical display was available and whether the turtle window actually appeared. Headless execution, remote shells, and missing Tk support can prevent visible GUI behavior even when source imports succeed.
