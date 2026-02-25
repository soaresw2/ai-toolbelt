# Open Pull Request (GBP Evo)

Open a pull request with the changes made in the current branch.

## Steps

1. Add and commit all changes, generating a commit message based on the code changes, unless one is provided in the chat.
2. Follow conventional commits guidelines:

- `feat:` new feature
- `fix:` bug fix
- `docs:` documentation only
- `refactor:` code change that neither fixes a bug nor adds a feature
- `chore:` maintenance (deps, config, etc.)

3. If any issues occur when adding and committing changes -- such as linter or type-check failures -- fix them and retry.
4. Open the PR using the template below. Mark it as ready for review and add the labels based on the instructions below:
   **type** (one of): `bug`, `documentation`, `enhancement` — infer from the commit type (`fix` → `bug`, `feat`/`refactor` → `enhancement`, `docs` → `documentation`)
   **impact** (one of): `minor` or `major` — use `major` only for breaking changes, deprecations, or cross-divisional impact; otherwise `minor`
5. For any template section where information is not available, fill in "N/A".
6. Check all checkboxes in the Checklist section by default and let the user uncheck individual ones as needed.

## PR Description Template

# Description

_Please include a summary of the change with the relevant motivation and context. If the PR introduces breaking changes, please state them clearly._

# Pull Request Relations

_List the links to any issues or dependencies that are related to or required for this change._

- Related to:
  - (# capability issue, # other pull requests)

# How Has This Been Tested?

_Please describe the tests that you ran to verify your changes. Provide instructions so they can be reproduced._

- Test A
- Test B

# Checklist

_Place `NA` between brackets when an activity is not applicable._

- [ ] I have identified any breaking changes in the description above.
- [ ] I have performed a self-review of my own code.
- [ ] Any dependent changes have been merged and published in downstream modules.
- [ ] I have added tests that prove my fix is effective or that my feature works.
- [ ] New and existing unit tests pass locally with my changes.
- [ ] The test plan is updated accordingly.
- [ ] Functional/regression test suite passing locally.
- [ ] Documentation is updated accordingly (e.g., setup, architecture, API).
- [ ] Pull request is properly categorized with labels for:
  - **type**: `bug`, `documentation`, or `enhancement`.
  - **impact**: `minor` or `major`.
  - A `major` pull request signifies a change that requires approval from cross-divisional maintainers before it can be merged. For instance:
    - A breaking change in the capability: API changes, behavioral changes, deprecation, library or dependency updates, configuration changes, data format changes, development tool changes, etc.
    - Introduction of new logic that will be supported by other divisions in the future.
    - Changes to metrics/logs that are being ingested by monitoring systems (e.g., Splunk, Datadog).

# Additional Context

_Add any other context or screenshots about this feature/bug fix, if applicable._
