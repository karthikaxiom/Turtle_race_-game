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
