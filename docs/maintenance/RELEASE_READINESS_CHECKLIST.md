# Release Readiness Checklist

This checklist is a practical review aid for preparing a repository snapshot for sharing. It distinguishes repository hygiene and documentation review from proof that the graphical game has been executed successfully. Complete only the checks that apply, and record evidence for any claim of verification.

## 01 — Identify the release candidate

Record the branch, commit SHA, and intended release label or sharing context. A moving branch name alone is not enough to identify the exact snapshot being reviewed.


## 02 — Confirm the intended branch

Verify that the candidate is on the intended branch and that the branch contains the changes expected for this release or handoff.

## 03 — Review the latest commit history

Inspect recent commit subjects and changed paths for accidental work, unexpected generated files, or unrelated maintenance.

## 04 — Inspect the working snapshot

Review the complete repository tree at the candidate revision. Confirm that required source, documentation, and project metadata are present.

## 05 — Check the entry-point file

Confirm that the documented launch command points to the actual application entry point and that the referenced file exists.

## 06 — Verify documentation navigation

Open the documentation index and follow its important links. Check nested relative paths from their actual locations.

## 07 — Check setup instructions

Ensure the setup steps describe the current Python and graphical runtime requirements without adding unsupported dependency claims.

## 08 — Check launch commands

Review shell commands for correct repository paths and platform-appropriate Python executable names. Distinguish alternatives rather than implying every environment uses the same command.

## 09 — Review input guidance

Confirm that user-facing instructions accurately describe the startup dialog, supported colors, and behavior when input is empty or cancelled.

## 10 — Review result guidance

Ensure documentation distinguishes terminal messages from graphics-window content and explains where users should look for the outcome.

## 11 — Check screenshot relevance

If a screenshot is included, verify that it represents the current interface and does not imply controls or features absent from the source.

## 12 — Check license statements

Inspect the repository for a license file before describing reuse permissions. Do not infer an open-source license from public visibility alone.

## 13 — Check attribution and asset references

Review external images, screenshots, and linked assets for attribution or provenance notes where applicable. Do not claim ownership without evidence.

## 14 — Check dependency declarations

Compare dependency files and documentation with actual imports. Avoid listing development-only tools as runtime requirements unless they are needed to launch the game.

## 15 — Check generated artifacts

Look for temporary logs, caches, compiled files, screenshots, and local test outputs that should not be part of the release snapshot.

## 16 — Review repository naming consistency

Check that repository names, file paths, and project titles are consistent across the README, documentation index, and command examples.

## 17 — Review behavior claims against source

Verify claims about race order, random movement, finish detection, result output, and shutdown against the current entry-point implementation.
