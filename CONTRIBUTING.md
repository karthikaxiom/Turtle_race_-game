# Contributing

Thanks for considering a contribution to Turtle Race. The project is intentionally a small Python Turtle graphics exercise, so changes should keep the game easy to run and understand.

## Before changing code

1. Read `README.md` for the current behavior and run instructions.
2. Read [the documentation index](docs/README.md) and [documentation rules](docs/DOCUMENTATION_RULES.md) before adding documentation.
3. Check `main.py` before describing or changing behavior. It is the source of truth.

## Scope and design

- Keep changes proportionate to this small, single-file game.
- Prefer Python's standard library unless an additional dependency is clearly necessary and its purpose is explained.
- Do not describe proposed features as if they already exist.
- Preserve the current color order, starting positions, input flow, and finish-check behavior unless the change explicitly intends to alter them.
- Keep user-facing text and documentation consistent with actual program behavior.
- Avoid adding a new document when an existing page can be updated clearly.

## Verifying a change

For a change that affects the running game:

1. Use a Python 3 installation with Tk support and a desktop environment.
2. Run the script from a terminal with `python main.py` or `python3 main.py`.
3. Check the relevant path from the [observable behavior checklist](docs/OBSERVABLE_BEHAVIOR_CHECKLIST.md).
4. Review terminal output as well as the graphics window; result messages are printed to the terminal.
5. For random movement, verify the rules and allowed range rather than expecting a particular turtle to win on every run.

The repository currently documents manual checks; do not claim that an automated test suite or continuous-integration workflow exists unless one is added and verified.

For a documentation-only change, check relative Markdown links and confirm that statements match `main.py`.

## Pull request notes

A useful pull request description should state:

- what behavior or documentation changed;
- why the change is needed;
- whether runtime behavior changed;
- how the change was verified; and
- any limitations or follow-up work.

Keep each change focused. Do not bundle unrelated cleanup with a behavior change.
