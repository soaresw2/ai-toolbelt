# Commands

Commands are quick, actionable instructions that tell an AI agent to perform specific tasks on selected code or within your project.

## What are Commands?

Commands are short, focused directives that can be invoked through your code editor's AI interface. They typically:
- Operate on selected code or the current file
- Perform a single, well-defined task
- Provide immediate, actionable results
- Can be chained or combined for complex workflows

## File Format

Each command is a standalone Markdown file with:
- **Filename**: Descriptive kebab-case name (e.g., `write-tests.md`, `refactor-code.md`)
- **Title**: H1 header with the command name
- **Description**: Clear explanation of what the command does
- **Guidelines**: Bullet points or numbered steps describing how to execute the task

### Example Structure

```markdown
# Command Name

Brief description of what this command does.

## Guidelines/Steps

- Guideline 1
- Guideline 2
- Guideline 3
```

## Usage in Different Editors

### Cursor
1. Copy command files to `.cursor/commands/` in your project
2. Access via Cursor's command palette
3. Select code and invoke the command

### GitHub Copilot (VSCode, JetBrains, Visual Studio)
1. Copy command files to `.github/copilot-commands/` or reference in chat
2. Use as reference prompts in Copilot Chat
3. Mention the command name in your requests

### Other Editors
- Use as reference templates when prompting your AI assistant
- Copy the content into your editor's AI chat or prompt interface
- Adapt the format to your editor's specific requirements

## Available Commands

- **write-tests.md** - Generate comprehensive unit tests for selected code
- **refactor-code.md** - Improve code quality and structure while maintaining functionality
- **add-error-handling.md** - Add robust error handling to code
- **document-code.md** - Generate documentation for code
- **optimize-performance.md** - Analyze and optimize code performance

## Creating Custom Commands

To create a new command:
1. Create a new `.md` file with a descriptive name
2. Add a clear title and description
3. List specific guidelines or steps
4. Keep it focused on a single task
5. Test it with your AI assistant
6. Share it back to this repository via pull request

## Best Practices

- Keep commands focused on a single task
- Use clear, actionable language
- Provide specific guidelines rather than vague instructions
- Include examples when helpful
- Consider edge cases and error scenarios
- Make commands editor-agnostic when possible
