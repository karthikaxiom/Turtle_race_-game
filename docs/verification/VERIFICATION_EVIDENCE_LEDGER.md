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

## 10. Startup order

Trace screen creation and configuration, the input dialog, turtle construction, race-state initialization, the loop, and shutdown in source order. If a change reorders these steps, explain its effect on the user-visible startup sequence.

## 11. Input dialog evidence

Record whether the dialog appeared, what prompt was shown, and what value was supplied. Avoid copying personal data or unnecessary user input into a public test record.

## 12. Cancellation path

Check the empty or cancelled input path separately from a normal race. In the current implementation, a falsey answer skips the movement loop, while the final click-to-close call remains in the execution path.

## 13. Unsupported input

The current code lowercases the raw guess for comparison but does not trim whitespace or validate membership in the configured color list. Keep this source-confirmed fact distinct from any future input-validation proposal.

## 14. Case handling

A case-variation check can confirm that the comparison uses a lowercased guess. Record the exact test value and result; do not infer whitespace normalization from case normalization.

## 15. Participant count

The current source constructs six turtle participants. If participant count changes, inspect all coupled configuration and presentation assumptions rather than updating only a single numeric statement.

## 16. Color order

Record the color list in source order and verify that any documentation or screenshot labels use the same ordering. Avoid relying on visual position alone to infer the configured color sequence.

## 17. Lane mapping

The current vertical-position list is paired with the color list by index. A change to either list should trigger a review of list lengths, order, and the intended participant-to-lane mapping.

## 18. Initial coordinates

Verify the configured horizontal starting coordinate and each vertical lane directly from source. If a screenshot is used as evidence, identify it as a visual observation rather than the authoritative numeric specification.

## 19. Pen state

The turtles are set to pen-up before being positioned. If a change modifies pen state, verify whether placement or movement begins drawing trails and update the relevant behavioral documentation.

## 20. Movement range

Each movement request uses a random integer from zero through ten inclusive. Document the range as source-confirmed; a single observed movement does not prove every value in that range was generated.

## 21. Randomness boundary

The movement progression is randomized while participant setup is configured explicitly. Do not describe the race as deterministic or promise that the same participant wins on repeated runs.

## 22. Loop traversal

The program visits participants in list order on each pass through the inner loop. If collection construction or traversal changes, review the effects on finish detection and printed result ordering.

## 23. Finish comparison

The current finish condition is a strict horizontal-coordinate comparison greater than 370. Equality does not satisfy it. Preserve the strictness in test descriptions and boundary-case reasoning.

## 24. Check timing

The finish condition is checked before the current participant's movement request. A turtle that crosses the threshold during movement is detected on a later visit, not immediately after that movement.

## 25. Outer-loop flag

A detected finisher sets the outer race flag to false. Record this separately from inner-loop termination; the current implementation does not break out of the participant loop at that point.

## 26. Same-pass continuation

Remaining participants in the same inner-loop pass may still be checked and moved after the race flag changes. A further participant may also meet the finish condition and produce another message during that pass.

## 27. Result comparison

The win/loss branch compares the detected turtle's pen color with the lowercased guess. If input normalization changes, re-check both the comparison and the wording used to describe accepted guesses.

## 28. Output destination

The current result messages are printed to the terminal. Do not describe them as graphical labels, dialogs, persistent records, or an in-window scoreboard unless implementation evidence supports that change.

## 29. Message wording

When documenting exact output, copy the current format from source and distinguish literal punctuation from explanatory paraphrase. Avoid promising output text that has not been verified against the inspected revision.

## 30. Shutdown path

The program calls `screen.exitonclick()` after the race loop or after the loop is skipped. Verify this behavior in the GUI environment and do not claim automatic closure or a replay flow.

## 31. Repeatability

Randomized movement means that repeated manual runs may produce different winners and timings. Record the input and environment for each run; do not use one run as proof of all possible race outcomes.

## 32. Manual test boundaries

A manual run is useful for checking that the application launches and responds, but it does not exhaustively test random movement, all possible input strings, or every possible same-pass finish combination.

## 33. Controlled test harnesses

If a harness controls random values or substitutes turtle objects, label its results as harness evidence. State which production behaviors are simulated and which were exercised with the actual GUI.

## 34. Screenshot provenance

For each screenshot, record the application revision, environment, test input, and capture purpose. Avoid using an unlabeled screenshot as proof of numeric settings or hidden control-flow details.
