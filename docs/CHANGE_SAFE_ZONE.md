# Safe Documentation Change Zone

For documentation maintenance, the safest changes are files under `docs/` that describe behavior already present in `main.py`. A documentation-only change should improve explanation or navigation without changing what the game executes.

## Safe documentation work

- Describe the current implementation rather than inventing features.
- Avoid changing runtime behavior or adding dependencies.
- Keep examples, identifiers, constants, and control-flow descriptions consistent with the source.
- Prefer improving a canonical page over creating another narrow reference.
- Preserve historical context in dated maintenance notes without treating it as current behavior.

## Review boundaries

Before committing, compare every behavioral claim with `main.py`, inspect relative links for changed Markdown files, and make sure the diff contains only the intended documentation paths. Check that no code, configuration, generated artifact, or unrelated file was changed as a side effect.

Changes to `main.py` should be treated separately from documentation-only maintenance because they can alter the game's runtime behavior. A proposed runtime improvement must be described as a proposal until it is implemented and reviewed in its own change.
