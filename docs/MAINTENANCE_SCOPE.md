# Maintenance Scope

This repository's documentation describes the behavior of the existing Turtle graphics race implementation.

Documentation-only maintenance should preserve source behavior and improve accuracy, navigation, or explanation without modifying `main.py`. Runtime changes should be treated as separate work and reviewed against the behavior checklist.

When documenting a proposed feature, label it clearly as a proposal; do not describe it as implemented until the source supports it. In particular, the current program has no persistent score, replay flow, input retry, or validation against the configured color list.

This separation keeps maintenance distinct from feature development and makes the documentation auditable against the source. See [Development Scope](DEVELOPMENT_SCOPE.md) and [Change Safe Zone](CHANGE_SAFE_ZONE.md).

## Review standard

Before accepting a documentation-only change, compare its statements with the current source and check nearby pages for conflicting descriptions. Prefer correcting a canonical explanation and linking to it over introducing another near-duplicate page. Keep runtime changes out of a documentation-only maintenance batch, and verify that `main.py` remains unchanged when that is the stated scope.
