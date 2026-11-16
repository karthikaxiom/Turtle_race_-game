# Development Scope

The project is a compact, single-file Turtle graphics exercise.

- `main.py` contains the runtime implementation.
- `README.md` introduces the project and its execution.
- `docs/` contains behavior references and maintenance guidance.
- The current runtime imports only Python standard-library modules.

The implementation demonstrates GUI input, lists, object creation, iteration, random movement, conditional branching, and a simple simulation loop. It does not currently include persistence, networking, a browser interface, scoring history, or a replay feature.

Documentation should describe behavior that exists in the source. Feature ideas should be labeled as proposals until implemented and reviewed. See [Maintenance Scope](MAINTENANCE_SCOPE.md) and [Change Safe Zone](CHANGE_SAFE_ZONE.md).

## Scope guard for contributions

A documentation contribution can clarify an existing branch or link related explanations, but should not imply that a proposed enhancement is available at runtime. In particular, adding a page about replay, persistent scores, or input validation must identify it as future work unless `main.py` is changed separately. Keep the single-file implementation as the authority for current behavior.
