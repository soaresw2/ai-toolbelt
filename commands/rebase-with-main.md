# Rebase with Main

Rebase the current branch onto `main`, intelligently resolving any conflicts that arise.

## Steps

1. **Understand the current branch** before starting the rebase:
   - Run `git log main..HEAD --oneline` to see all commits on this branch.
   - Run `git diff main...HEAD` to understand the full set of changes this branch introduces.
   - Read the relevant changed files to build a mental model of **what this branch is trying to accomplish** — the feature, bug fix, or refactor intent.

2. **Understand what changed on main** since this branch diverged:
   - Run `git log $(git merge-base HEAD main)..main --oneline` to see what was merged into main.
   - For any files that are likely to conflict (files changed on both sides), run `git diff $(git merge-base HEAD main)..main -- <file>` to understand **what changed on main and why**.

3. **Fetch and start the rebase**:
   - Run `git fetch origin main` to ensure main is up to date.
   - Run `git rebase origin/main`.

4. **If conflicts arise**, resolve them intelligently for each conflicting commit:
   - Run `git diff --name-only --diff-filter=U` to list conflicting files.
   - For each conflicting file:
     a. Read the file to see the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
     b. Understand **both sides**:
        - The `main` side: what was the intent of the change on main? Was it a refactor, a new feature, a bug fix, a dependency update?
        - The `branch` side: what is this branch trying to do in this file?
     c. Resolve the conflict by **preserving the intent of both sides**. This means:
        - If main refactored or renamed something, adopt main's structure but apply the branch's logic within it.
        - If main added new code nearby, keep main's additions and integrate the branch's changes alongside them.
        - If both sides modified the same logic for different reasons, merge the behaviors so neither is lost. If they are truly incompatible, prefer the branch's intent (since that's the active work) but incorporate any bug fixes or safety checks from main.
        - If main updated imports, type signatures, or API calls, use main's updated versions and adapt the branch's code to work with them.
     d. After editing the file to resolve conflicts, run `git add <file>`.
   - After all conflicts in the current commit are resolved, run `git rebase --continue`.
   - If more commits have conflicts, repeat step 4 for each one.

5. **Verify the rebase succeeded**:
   - Run `git status` to confirm there are no pending conflicts and the rebase is complete.
   - Run `npm run type-check` to make sure TypeScript compilation still works after the rebase.
   - Run `npm run lint` to check for any linting issues introduced by the merge.
   - If type-check or lint fail, fix the issues — they likely stem from API changes on main that the branch code needs to adapt to.

6. **If the rebase is unrecoverable** (e.g., too many deeply intertwined conflicts that cannot be resolved automatically), run `git rebase --abort` and explain the situation, listing the specific files and reasons that make automatic resolution unsafe.
