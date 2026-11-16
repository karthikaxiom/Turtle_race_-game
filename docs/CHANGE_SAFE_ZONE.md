# Safe Documentation Change Zone

The safest maintenance changes are documentation updates that describe behavior already present in `main.py`.

## Review checklist

- Compare each behavioral claim with the current source.
- Keep identifiers, constants, comparison operators, and operation order exact.
- Prefer improving a canonical page over creating another narrow reference.
- Preserve historical context without presenting it as current behavior.
- Inspect relative Markdown links in every changed page.
- Confirm the diff contains only intended documentation paths.

Runtime changes to `main.py` are separate work. Proposed validation, replay, logging, or scoring features must not be described as implemented until the source contains them.