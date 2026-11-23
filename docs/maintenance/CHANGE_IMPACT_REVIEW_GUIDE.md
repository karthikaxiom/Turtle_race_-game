# Change Impact Review Guide

A source-led method for assessing how proposed changes may affect the Turtle Race implementation, its observable behavior, verification evidence, and documentation. Use it to make review decisions explicit without treating proposals as existing features.

## 01. Purpose and boundaries

This guide helps reviewers trace the impact of a proposed change through the small Turtle Race project. It is a review method, not a specification of new runtime features. The inspected source remains authoritative, and every conclusion should be tied to a revision.

## 02. Start from the requested outcome

Rewrite the change request as a concrete outcome before inspecting files. Separate the user-visible problem from a proposed implementation, because the requested outcome may be achievable without changing the production entrypoint.
