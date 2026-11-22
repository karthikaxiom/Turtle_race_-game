# Maintenance Handoff Guide

A practical handoff reference for reviewing, maintaining, and documenting the current Turtle Race implementation. This guide complements the behavior-focused pages in the documentation index; it does not override `main.py` or turn future ideas into current features.

## 01. Purpose and audience

This guide supports a maintainer who is taking over a small, source-led Turtle graphics project. It is a handoff aid, not a replacement for the implementation or the canonical behavior pages. Use it to establish what is known, what must be checked, and what should remain untouched until evidence exists.

## 02. Authoritative evidence

Treat the checked-out `main.py` as the authority for current runtime behavior. Documentation, screenshots, commit messages, and recollections are secondary evidence. If they disagree with the source, record the discrepancy and verify whether the source or the description is stale before changing either.

## 03. Establish the revision

Record the branch name, full commit identifier, working-tree state, and date of inspection. A handoff without a revision is ambiguous: later readers cannot tell whether observations describe the same code they are reviewing.

## 04. Separate facts from assumptions

Label statements as observed, inferred, proposed, or unknown. For example, a visible dialog is observed behavior; an assumption about how a user will respond is not. Do not turn a plausible expectation into a guaranteed product property.

## 05. Confirm the launch environment

Check the Python interpreter and whether a graphical desktop session is available. The program uses the standard-library `turtle` and `random` modules, while the graphics stack depends on the host's Tk support. A successful import alone does not prove that a window can be displayed.
