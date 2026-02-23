# Bug Fix Instructions

When fixing bugs, follow this systematic approach:

## Understanding the Bug

1. Reproduce the bug consistently
2. Understand the expected vs actual behavior
3. Identify the root cause, not just symptoms
4. Check if similar bugs exist elsewhere in the codebase

## Implementation

1. Write a failing test that reproduces the bug
2. Fix the bug with minimal changes
3. Ensure the test now passes
4. Verify no regression in existing tests
5. Consider edge cases related to the bug

## Code Changes

- Make targeted, minimal changes
- Avoid refactoring unrelated code
- Maintain consistency with existing code style
- Add comments explaining non-obvious fixes
- Update documentation if the bug revealed gaps

## Testing

- Add regression tests to prevent the bug from reoccurring
- Test edge cases and boundary conditions
- Verify the fix in different scenarios
- Check for performance implications

## Documentation

- Update relevant documentation
- Add comments explaining complex fixes
- Update changelog if applicable
- Reference the bug report or issue number

## Before Committing

- [ ] Bug is reproducibly fixed
- [ ] Tests are added and passing
- [ ] No new bugs introduced
- [ ] Code is reviewed
- [ ] Documentation is updated
