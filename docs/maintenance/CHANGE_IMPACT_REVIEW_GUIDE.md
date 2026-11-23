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
