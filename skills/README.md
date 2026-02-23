# Skills

Skills are comprehensive capabilities that define how an AI agent should approach complex, multi-step tasks or domains of expertise.

## What are Skills?

Skills are detailed specifications that enable AI agents to:
- Understand domain-specific knowledge
- Apply specialized techniques and methodologies
- Handle complex, multi-faceted tasks
- Maintain consistency across related operations
- Follow best practices in specific areas

Unlike commands (which are quick actions), skills define ongoing capabilities and expertise.

## File Format

Each skill is a Markdown file with:
- **Filename**: Descriptive kebab-case name (e.g., `code-review.md`, `testing.md`)
- **Title**: H1 header with the skill name
- **Introduction**: Brief description of the skill's purpose
- **Capabilities**: List of what the skill enables
- **Usage**: How the skill should be applied
- **Best Practices**: Guidelines for optimal results

### Example Structure

```markdown
# Skill Name

Brief description of this skill's purpose.

## Capabilities

- Capability 1
- Capability 2
- Capability 3

## Usage

When activated, this skill will:
1. Step 1
2. Step 2
3. Step 3

## Best Practices

- Best practice 1
- Best practice 2
```

## Usage in Different Editors

### Cursor
1. Copy skill files to `.cursor/skills/<skill-name>/` in your project
2. Rename to `SKILL.md` within each skill folder
3. Cursor automatically loads and applies these skills

### GitHub Copilot
1. Add skill content to `.github/copilot-instructions.md`
2. Reference skills in your Copilot workspace settings
3. Copilot uses these as context for all interactions

### Zed
1. Copy skill content to `.zed/settings.json` under assistant context
2. Or create custom slash commands that reference skills

### Other Editors
- Include skill descriptions in your AI assistant's system prompts
- Reference skills when starting complex tasks
- Use as persistent context for your AI sessions

## Available Skills

- **code-review.md** - Comprehensive code review expertise
- **testing.md** - Software testing and quality assurance capabilities

## Creating Custom Skills

To create a new skill:
1. Identify a domain or complex task that requires specialized knowledge
2. Create a `.md` file with a descriptive name
3. Document the capabilities this skill provides
4. Describe how the skill should be applied
5. Include best practices and guidelines
6. Consider what knowledge or context the AI needs
7. Test the skill across different scenarios
8. Share via pull request

## Best Practices

- Define clear, comprehensive capabilities
- Provide context about when to use the skill
- Include domain-specific terminology and concepts
- Consider the skill's scope (not too broad, not too narrow)
- Make skills composable (they can work together)
- Update skills as best practices evolve
- Include examples of the skill in action

## Skills vs Commands

**Use Skills when:**
- The task requires specialized domain knowledge
- Multiple steps or decisions are involved
- Context needs to persist across interactions
- You want to define ongoing AI behavior

**Use Commands when:**
- The task is quick and focused
- It's a one-time action on specific code
- The steps are straightforward and consistent
- You need immediate, tactical results
