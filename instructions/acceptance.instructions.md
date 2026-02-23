# Acceptance Testing Instructions

When implementing acceptance tests, follow these guidelines:

## Test Structure

- Write tests from the user's perspective
- Focus on business requirements and user stories
- Use descriptive test names that explain the scenario
- Follow Given-When-Then format where applicable

## What to Test

- End-to-end user workflows
- Critical business processes
- User acceptance criteria from requirements
- Integration between different system components
- Real-world usage scenarios

## Best Practices

- Keep tests independent and isolated
- Use realistic test data
- Clean up test data after execution
- Make tests readable and maintainable
- Avoid testing implementation details
- Focus on observable behavior

## Example Structure

```
describe('User Registration Flow', () => {
  it('should allow a new user to register with valid credentials', async () => {
    // Given: A new user wants to register
    // When: They submit the registration form with valid data
    // Then: Their account is created and they are logged in
  });
});
```

## Tools and Frameworks

- Use the testing framework configured in the project
- Leverage page objects or similar patterns for UI tests
- Use appropriate assertion libraries
- Consider using test data builders for complex scenarios
