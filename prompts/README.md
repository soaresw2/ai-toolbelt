# Prompts

Prompts are reusable templates that define the persona, context, and expected behavior for AI interactions on specific tasks.

## What are Prompts?

Prompts are structured templates that:
- Define the AI's role or persona for a task
- Provide context and expectations
- Guide the AI's approach and output format
- Can be invoked directly in AI chat interfaces
- Work across different AI tools and editors

Prompts are more conversational than commands and more focused than instructions.

## File Format

Each prompt is a Markdown file with:
- **Filename**: Descriptive kebab-case name (e.g., `explain-code.md`, `generate-tests.md`)
- **Title**: H1 header with the prompt name
- **Persona**: Opening statement defining the AI's role
- **Task Description**: What the AI should do
- **Guidelines**: How the AI should approach the task
- **Optional sections**: Examples, output format, etc.

### Example Structure

```markdown
# Prompt Name

You are an expert [role]. When [context/trigger]:

1. Action 1
2. Action 2
3. Action 3

## Guidelines

- Guideline 1
- Guideline 2

## Output Format (optional)

Description of expected output.
```

## Usage in Different Editors

### Zed
1. Copy prompt files to `.zed/prompts/` in your project
2. Access via Zed's assistant panel
3. Prompts appear as selectable templates

### Cursor
1. Use prompts in Cursor's chat interface
2. Copy prompt content when starting a conversation
3. Save as custom commands if they're frequently used

### GitHub Copilot
1. Paste prompts into Copilot Chat
2. Use as templates for complex requests
3. Combine with instructions for comprehensive guidance

### Claude, ChatGPT, Other AI Chat Interfaces
1. Copy prompt content directly into the chat
2. Customize placeholders or specifics for your context
3. Save as snippets in your editor for quick access

## Available Prompts

- **explain-code.md** - Template for requesting code explanations
- **generate-tests.md** - Guide AI to write comprehensive tests
- **improve-code.md** - Prompt for code quality improvements

## Creating Custom Prompts

To create a new prompt:
1. Identify a common AI interaction pattern
2. Create a `.md` file with a descriptive name
3. Start with a clear persona or role definition
4. Describe the task and expected approach
5. Add specific guidelines or steps
6. Include output format if relevant
7. Test with different AI tools
8. Refine based on results
9. Share via pull request

## Best Practices

- Start with a clear role or persona
- Be specific about the task and context
- Provide structured guidelines
- Use imperative language ("Analyze...", "Provide...", "Focus on...")
- Include examples when helpful
- Consider the output format
- Make prompts reusable across contexts
- Keep prompts focused on one type of interaction
- Test with multiple AI models when possible

## Prompts vs Commands vs Instructions

**Use Prompts when:**
- Starting a conversation with AI
- Need to define AI's role or perspective
- Want reusable chat templates
- Working across different AI tools

**Use Commands when:**
- Quick action on selected code
- Editor-specific automation
- Single-step operations

**Use Instructions when:**
- Defining complete workflows
- Setting ongoing context for a project
- Establishing team standards

## Tips for Effective Prompts

1. **Be Specific**: Vague prompts yield vague results
2. **Set Context**: Help the AI understand the situation
3. **Define Success**: Describe what good output looks like
4. **Iterate**: Refine prompts based on actual usage
5. **Combine**: Use with commands, skills, or instructions
6. **Version**: Keep track of what works and what doesn't
7. **Share**: Contribute effective prompts back to the community
