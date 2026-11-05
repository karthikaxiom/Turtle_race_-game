# Documentation Rules

These rules keep the repository's documentation useful as the code evolves.

## Source of truth

- Treat `main.py` as the authority for current runtime behavior.
- Describe what the code does today; label proposed or hypothetical behavior clearly instead of presenting it as implemented.
- Do not change runtime code as part of documentation-only maintenance.

## When to add a page

Before creating a new page, search the existing documentation and prefer updating the closest relevant page when the subject is already covered.

Create a separate page only when it answers a distinct maintainer or user question that cannot be answered clearly by extending an existing page. A page should explain a meaningful concept, relationship, edge case, or operational procedure—not merely restate one assignment, literal, or line of code.

When related notes already exist, link to the canonical explanation rather than copying the same explanation into another file. Avoid near-duplicate filenames and narrow documents that differ only in wording.

## Consolidating legacy notes

When two or more pages cover the same concept:

1. Choose the clearest page as the canonical reference.
2. Compare the other pages for unique factual details or edge cases.
3. Incorporate useful details into the canonical page, checking every claim against `main.py`.
4. Search the repository for links to each proposed removal.
5. Update navigation and internal links before removing redundant pages.
6. Keep dated maintenance records when they provide historical context; do not treat them as current behavioral specifications.

Do not delete a page merely because its title resembles another. Consolidation is appropriate only after its useful information and inbound links have been accounted for.

## Page quality

A useful page should:

- state its scope in the opening paragraph;
- explain the behavior and why it matters, with source identifiers where helpful;
- distinguish guaranteed behavior from outcomes that depend on random movement or user input;
- mention relevant limitations and edge cases;
- link to adjacent material instead of repeating it.

Keep claims consistent with the current source. Do not invent tests, guarantees, controls, persistence, or features that the program does not implement.

## Index and review

- Add new substantial pages to [the documentation index](README.md).
- Check relative Markdown links when editing an index.
- Use [the safe-change guidance](CHANGE_SAFE_ZONE.md) and [the observable-behavior checklist](OBSERVABLE_BEHAVIOR_CHECKLIST.md) when reviewing documentation changes.
- Treat `reference/` as supplementary focused notes and `maintenance/` as dated maintenance records; neither should replace a clear, maintained overview.

Consolidate legacy overlap in a separately reviewed change, preserving historical records where appropriate.
