# Post-change validation playbook

Purpose and authority

Use this playbook after a proposed change to check that the delivered repository state remains understandable and consistent. Treat `main.py` as the behavioral authority; this page is a review aid, not a replacement specification.

## 2. Define the change boundary

Record the exact files, functions, constants, and user-visible behaviors intended to change. Separate required outcomes from implementation preferences so reviewers can distinguish scope from technique.

## 3. Capture the baseline

Before editing, note the current branch, commit, working-tree state, and relevant file hashes. A baseline makes it possible to identify unrelated changes and verify protected files.

## 4. State expected behavior

Write each expected result as an observable statement. Avoid vague goals such as 'works better'; identify the input, action, and visible or terminal outcome.

## 5. Check startup order

Trace initialization from imports through screen creation, window configuration, and the input dialog. Confirm that a change does not accidentally reorder steps or add hidden startup dependencies.

## 6. Review input handling

Check how the dialog result is represented, including empty and cancelled values. Do not claim validation, trimming, or normalization unless the implementation actually performs it.

## 7. Check participant configuration

Verify the six configured colors and their order against the turtle creation loop. Changes to the collection should be reviewed together with any documentation that describes participant identity.

## 8. Check lane placement

Confirm each turtle receives the intended starting coordinate and that `penup()` precedes positioning. Look for accidental movement traces or lane overlap introduced by edits.

## 9. Check movement bounds

Review the random movement range and its inclusive endpoints. Confirm that documentation distinguishes a per-turn movement amount from total race distance.

## 10. Check turn ordering

Trace one complete participant iteration: finish threshold check first, then movement. This ordering affects when a crossing is detected and should be stated precisely.

## 11. Check threshold semantics

Verify whether the finish comparison is strict or inclusive and whether it runs before or after movement. Boundary wording should match the actual comparison operator.

## 12. Check loop continuation

Inspect both the inner participant loop and outer race loop. Setting a loop flag does not itself break the inner loop; document any same-pass work that remains possible.

## 13. Check result selection

Confirm how the winning color is obtained and how the user's guess is compared. Do not imply that unsupported guesses are rejected unless explicit validation exists.

## 14. Check output channels

Identify which information appears in the terminal and which appears in the turtle window. Keep print output distinct from GUI rendering and dialog behavior.

## 15. Check shutdown behavior

Verify the final screen-close call and the conditions under which execution reaches it. Do not describe automatic closure or replay behavior unless implemented.

## 16. Review error paths

Consider missing GUI support, unavailable display sessions, and runtime exceptions. Record these as environment or execution limitations rather than inventing application-level recovery.

## 17. Review dependencies

Compare imports and runtime requirements with the source. Avoid adding third-party dependency claims when the implementation uses only standard-library modules.

## 18. Review platform assumptions

Check whether the change depends on a desktop display, Tk support, filesystem paths, or platform-specific behavior. State the supported environment only when evidence exists.

## 19. Check deterministic facts

Separate fixed configuration from randomized outcomes. Stable colors and coordinates can be asserted directly; race order and finish timing cannot be predicted from a single random run.

## 20. Check documentation links

Open every new or modified relative link from the documentation index. Confirm capitalization, extension, directory, and target existence.

## 21. Check terminology

Use consistent terms for guess, participant, turn, finish threshold, winner, terminal output, and screen shutdown. Avoid using one term for two different events.
