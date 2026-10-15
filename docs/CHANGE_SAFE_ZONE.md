# Safe Documentation Change Zone

For documentation maintenance, the safest changes are files under `docs/` that describe behavior already present in `main.py`.

Documentation updates should:

- describe the current implementation rather than inventing features;
- avoid changing runtime behavior;
- avoid adding dependencies;
- keep examples consistent with the source code;
- use focused topics that are not already covered by an existing reference.

Changes to `main.py` should be treated separately from documentation-only maintenance because they can alter the game's runtime behavior.
