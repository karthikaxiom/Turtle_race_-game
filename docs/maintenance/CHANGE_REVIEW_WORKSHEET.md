# Maintainer Change Review Worksheet

This worksheet helps reviewers assess a proposed change to the Turtle Race project before it is merged or published. It complements the behavioral matrix and manual execution protocol: its focus is change impact, evidence, scope control, and review quality. The current source remains authoritative; a review item is not proof that a test was executed.

## 01 — State the change intent

Write one concise statement describing the intended outcome. Avoid combining unrelated goals in one change, because a reviewer should be able to tell what success means before inspecting the diff.


## 02 — Identify the authoritative source

Confirm which source revision defines the behavior being reviewed. Documentation, screenshots, and old commits can provide context, but they must not override the current implementation.

## 03 — Separate intended behavior from incidental behavior

List the behavior that the change is meant to alter and the behavior that must remain stable. This distinction prevents an apparently small edit from silently changing unrelated interactions.

## 04 — Classify the change surface

Mark the change as source logic, user-visible presentation, documentation, repository configuration, or tooling. If it spans categories, explain why the coupling is necessary.

## 05 — Trace the input path

For input-related changes, follow the value from dialog return through storage and comparison. Check whether empty, cancelled, padded, uppercase, and unsupported values are affected.

## 06 — Trace initialization dependencies

For setup changes, verify the order of screen creation, dialog invocation, participant construction, and race-state initialization. Reordering can affect observable startup behavior.

## 07 — Review configuration pairing

When changing participant colors or lane positions, inspect the paired lists together. Confirm that each participant retains the intended color-to-position association.

## 08 — Check collection assumptions

If participant count or storage changes, inspect every loop and index assumption that depends on the collection. A configuration edit can have downstream effects beyond drawing another turtle.

## 09 — Verify coordinate assumptions

Review any changes to start coordinates, lane spacing, or finish boundaries as one geometric system. Confirm that the window dimensions still make the intended positions visible.

## 10 — Review appearance and drawing state

For visual changes, check shape, fill and pen colors, pen-up state, and drawing side effects. A turtle can look correct while unexpectedly leaving a trail.

## 11 — Preserve random range semantics

If movement randomness changes, record the lower and upper bounds and whether each endpoint is inclusive. Do not describe a range as equivalent when its endpoints differ.

## 12 — Check random call frequency

Determine whether a change affects how often random values are requested: once per participant, once per pass, or at another scope. Frequency changes can alter the entire race progression.

## 13 — Inspect movement ordering

Trace whether a participant is checked before or after it moves. Reversing those operations changes when a crossing becomes observable.

## 14 — Inspect threshold operators

Review the exact comparison operator at the finish boundary. Greater-than and greater-than-or-equal are different contracts at equality.

## 15 — Follow state changes to loop boundaries

When a flag or state variable changes, identify which loop condition reads it next. A state update does not necessarily interrupt a loop that is already executing.

## 16 — Assess same-pass continuation

Check whether later participants continue to be processed after a finish is detected. If control flow is changed, document whether remaining checks, movements, and messages still occur.

## 17 — Review multiple-finish behavior

Consider whether more than one participant can satisfy the finish condition during one pass. State clearly whether the change preserves, prevents, or intentionally redesigns that possibility.

## 18 — Trace the reported identity

Follow the value used to identify a detected participant into the result message. Ensure the displayed color or label comes from the intended source and is not accidentally inferred from the user's selection.

## 19 — Compare both result branches

Review matching and non-matching input paths together. A change that fixes one message branch may leave the other branch inconsistent or unreachable.

## 20 — Check output destination

Determine whether feedback is printed to the terminal, drawn in the graphics window, or sent elsewhere. Changing the output surface affects how users launch and observe the game.

## 21 — Review shutdown on every path

Trace the end of execution after a completed race and after startup input is cancelled or empty. Confirm that cleanup and window-wait behavior remain intentional on both paths.

## 22 — Identify single-run assumptions

If adding replay, reset, or repeated rounds, review which objects and variables must be recreated or reset. Re-entering a loop alone does not guarantee a clean new game.

## 23 — Check dependency claims

Inspect imports and runtime setup before adding or removing a dependency. Keep documentation aligned with the actual modules used by the program and distinguish standard-library requirements from optional developer tools.

## 24 — Evaluate platform assumptions

For GUI or environment changes, consider desktop availability, Tk support, terminal access, and platform-specific launch commands. Avoid promising identical behavior in headless environments.

## 25 — Review error handling boundaries

Identify which failures are currently handled and which propagate. Do not document graceful recovery unless the implementation actually provides it.

## 26 — Consider accessibility of feedback

Check whether a user can perceive prompts, progress, and results with the current interaction model. If feedback remains terminal-only, state the launch requirement plainly.
