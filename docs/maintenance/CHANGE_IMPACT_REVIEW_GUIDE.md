# Change Impact Review Guide

A source-led method for assessing how proposed changes may affect the Turtle Race implementation, its observable behavior, verification evidence, and documentation. Use it to make review decisions explicit without treating proposals as existing features.

## 01. Purpose and boundaries

This guide helps reviewers trace the impact of a proposed change through the small Turtle Race project. It is a review method, not a specification of new runtime features. The inspected source remains authoritative, and every conclusion should be tied to a revision.

## 02. Start from the requested outcome

Rewrite the change request as a concrete outcome before inspecting files. Separate the user-visible problem from a proposed implementation, because the requested outcome may be achievable without changing the production entrypoint.

## 03. Identify the affected surface

List the files and runtime surfaces that could be affected: startup, input, participant setup, movement, finish detection, output, and shutdown. Keep the initial list broad, then narrow it with source evidence.

## 04. Record the baseline revision

Capture the branch and full commit SHA before review. Record whether the working tree is clean. A change-impact analysis without a baseline cannot reliably distinguish existing behavior from proposed behavior.

## 05. Read the current implementation

Inspect the relevant source statements in context, including surrounding control flow. Avoid basing impact decisions on isolated lines, old screenshots, or descriptions copied from earlier revisions.

## 06. Separate behavior from presentation

Determine whether the request changes program behavior, documentation presentation, or both. A wording change should not accidentally imply a runtime change; a runtime change may require several documentation updates.

## 07. Trace startup dependencies

For startup changes, review screen creation, screen configuration, the input dialog, turtle construction, and race-state initialization in execution order. Reordering these steps can change what the user sees and when.

## 08. Trace input dependencies

For input changes, inspect how the dialog value is obtained, tested for truthiness, normalized, validated, and later compared. Do not assume that lowercasing also trims whitespace or validates membership.

## 09. Trace configuration dependencies

The participant colors and vertical positions are paired by list index. Any change to participant count, color order, or lane positions should review the lengths and alignment of all related configuration.

## 10. Trace object lifecycle

Review where turtle objects are constructed, configured, positioned, stored, traversed, and queried. A change to construction or storage can affect later movement and result detection.

## 11. Trace movement behavior

The current movement request is randomized from zero through ten inclusive. If movement changes, assess its range, frequency, ordering, and whether the change affects repeatability or expected race duration.

## 12. Trace finish detection

The current source checks whether a turtle's horizontal coordinate is strictly greater than 370 before its movement for that visit. Any threshold or ordering change affects detection timing and boundary behavior.

## 13. Trace loop termination

The race flag controls the outer loop, while the inner participant loop continues through its current pass. Review both loops before describing a change as an immediate stop or a single-winner event.

## 14. Trace result selection

The current result branch compares the detected turtle's pen color with the lowercased guess. Changes to accepted input or participant identity must be traced through this comparison.

## 15. Trace output destinations

Current win/loss messages are printed to the terminal. If output is moved or duplicated, review terminal behavior, graphics behavior, message ordering, and whether persistent state is actually introduced.

## 16. Trace shutdown behavior

The current program calls `screen.exitonclick()` after the race loop. Any change to shutdown should consider both a completed race and the path where input causes the loop to be skipped.

## 17. List observable changes

Write down what a player would notice before and after the proposed change. Include dialogs, participant appearance, movement, finish timing, messages, and window closure only where affected.

## 18. List non-observable changes

Some changes affect maintainability without changing runtime behavior, such as comments or documentation organization. State explicitly when the player-facing behavior is intended to remain identical.

## 19. Identify compatibility risks

Consider whether existing launch commands, Python versions, graphical environments, or user expectations may be affected. Do not claim compatibility across platforms without evidence.

## 20. Check standard-library assumptions

The current source imports `turtle` and `random`. If a proposal adds dependencies, identify installation, version, platform, and packaging implications before treating the change as low risk.

## 21. Assess GUI environment risks

The turtle interface relies on a graphical environment and Tk support. A source-level change may be correct while remaining untestable in a headless or restricted remote session; record that limitation.

## 22. Consider random-sequence effects

Changing the number or order of random calls can alter outcomes even if the movement range stays the same. Describe such changes as changes to random progression, not merely cosmetic refactoring.

## 23. Consider ordering effects

Changing participant traversal order can alter which finish conditions are observed first and the order of printed messages. Review order-sensitive behavior explicitly.

## 24. Consider boundary conditions

For numeric conditions, test equality, just below, and just above the boundary. Preserve strict versus inclusive comparisons accurately in code review notes and documentation.

## 25. Consider empty and unsupported input

Review empty, cancelled, case-varied, whitespace-padded, and unsupported non-empty answers where applicable. Distinguish current behavior from any proposed validation policy.
