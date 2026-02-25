# Update Unit Tests

Assess current test coverage, then create new tests and fix existing ones to achieve full branch and function coverage.

## Steps

1. Identify the project's test runner and configuration (e.g., Jest, Vitest) by inspecting config files and `package.json` scripts.
2. Run the full test suite with `--watchAll=false` (or the runner's equivalent) and with coverage enabled, so the command exits after completion.
3. Analyze the coverage report to identify uncovered branches and functions.
4. Review existing test files to learn the project's testing patterns -- file naming, describe/it structure, mocking approach, and assertion style.
5. For each uncovered branch or function, write concise test cases -- only the minimum needed to cover every branch and function. Keep test blocks simple and non-verbose.
6. Do not add coverage-ignore comments (e.g., `/* istanbul ignore */`, `/* v8 ignore */`) to manipulate coverage numbers.
7. Follow any project-level testing guidelines found in documentation, linter configs, or README files.
8. Re-run the test suite with coverage after changes to confirm all new and existing tests pass and coverage targets are met.
