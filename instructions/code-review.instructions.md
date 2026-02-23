# Code Review Instructions

When reviewing code, apply these standards:

## What to Look For

### Correctness
- Does the code do what it's supposed to do?
- Are there any logical errors or bugs?
- Are edge cases handled properly?

### Security
- Are there any security vulnerabilities?
- Is user input properly validated and sanitized?
- Are secrets or sensitive data properly handled?
- Is authentication and authorization implemented correctly?

### Performance
- Are there obvious performance bottlenecks?
- Are expensive operations optimized?
- Is caching used appropriately?

### Maintainability
- Is the code readable and well-organized?
- Are names descriptive and consistent?
- Is the code properly documented?
- Does it follow the project's conventions?

### Testing
- Are there adequate tests?
- Do tests cover edge cases?
- Are tests clear and maintainable?

## Review Approach

1. Understand the purpose and context of the changes
2. Check for critical issues first (security, bugs)
3. Review architecture and design decisions
4. Examine code quality and style
5. Verify test coverage
6. Provide constructive, specific feedback

## Feedback Guidelines

- Be respectful and constructive
- Explain the reasoning behind suggestions
- Distinguish between required changes and nice-to-haves
- Provide examples when suggesting alternatives
- Acknowledge good practices in the code
