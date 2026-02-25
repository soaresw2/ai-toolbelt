# Skills

Skills are comprehensive definitions of specialized AI expertise. They describe domain knowledge, capabilities, and methodologies that enable an AI agent to handle complex, multi-step tasks in a specific area.

Skills are **primarily a Cursor concept**. Other editors do not have a direct equivalent, but skill content can be adapted into rules or instructions for those editors (see Editor Setup below).

## When to Use Skills

Use a skill when you need:

- Deep domain expertise for a specialized area (code review, testing, security auditing)
- Multi-faceted capabilities that span several related tasks
- Persistent context that applies whenever the AI works in a domain
- A comprehensive reference the AI can draw on across multiple interactions

If you need a quick action, use a [command](../commands/). If you need a step-by-step workflow, use [instructions](../instructions/). If you need always-on standards, use [rules](../rules/).

## Writing Guidelines

### File Naming

- Use **kebab-case** with a `.md` extension: `code-review.md`, `testing.md`, `security-audit.md`
- The name should describe the domain or area of expertise

### Structure

Every skill file should contain:

1. **H1 title** -- the skill name
2. **Introduction** -- one or two sentences describing the skill's purpose
3. **Capabilities** -- bulleted list of what the skill enables the AI to do
4. **Usage** -- how and when the skill should be applied (numbered steps or description)
5. **Best Practices** -- guidelines for getting the best results from the skill

### Content Principles

- Define **clear, comprehensive capabilities** -- the AI needs to know what it can do with this skill
- Provide **domain context** -- include terminology, patterns, and concepts specific to the area
- Make skills **composable** -- they should work alongside other skills, rules, and commands
- Focus on **expertise, not process** -- skills describe what the AI knows, not step-by-step workflows (that is what instructions are for)
- Stay **editor-agnostic** in the file content itself

## Editor Setup

### Cursor -- Primary

Create a named folder for each skill inside your project:

```
[PROJECT]/.cursor/skills/<skill-name>/SKILL.md
```

For example:

```
.cursor/skills/code-review/SKILL.md
```

Cursor automatically loads skills from this location. You can add optional YAML frontmatter:

```yaml
---
name: code-review
description: Comprehensive code review expertise
---
```

Global skills (available across all projects) go in `~/.cursor/skills/`.

### VS Code / WebStorm (GitHub Copilot)

No direct equivalent. Embed skill content into an instruction file:

```
[PROJECT]/.github/instructions/<skill-name>.instructions.md
```

This allows Copilot to apply the expertise contextually.

### Zed

No direct equivalent. Add skill content to the assistant context or save as a prompt in `[PROJECT]/.zed/prompts/` for easy reference.

### Other Editors

Embed skill content into your editor's rules or instruction files. Skills are plain Markdown and can be adapted to any format.

## Example

See [_example-code-review.md](./_example-code-review.md) for a reference implementation. This file exists solely to illustrate the expected format -- it is not intended to be copied into your project as-is.
