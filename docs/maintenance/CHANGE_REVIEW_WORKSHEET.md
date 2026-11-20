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
