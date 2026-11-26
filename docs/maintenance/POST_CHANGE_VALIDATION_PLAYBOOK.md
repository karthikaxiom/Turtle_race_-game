# Post-change validation playbook

Purpose and authority

Use this playbook after a proposed change to check that the delivered repository state remains understandable and consistent. Treat `main.py` as the behavioral authority; this page is a review aid, not a replacement specification.

## 2. Define the change boundary

Record the exact files, functions, constants, and user-visible behaviors intended to change. Separate required outcomes from implementation preferences so reviewers can distinguish scope from technique.

## 3. Capture the baseline

Before editing, note the current branch, commit, working-tree state, and relevant file hashes. A baseline makes it possible to identify unrelated changes and verify protected files.
