# Commands

Commands are quick, focused directives that tell an AI agent to perform a specific task. They can be action-oriented ("write tests for this code") or persona/template-style ("you are an expert code reviewer -- analyze this code"). This folder also covers what some editors call "prompts."

## When to Use Commands

Use a command when you need:

- A single, well-defined action on selected code or a file
- A reusable template for a common AI interaction
- An AI persona for a specific type of task
- Immediate, tactical results without multi-step workflows

If you need multi-step workflow guidance, use [instructions](../instructions/). If you need always-on standards, use [rules](../rules/).

## Writing Guidelines

### File Naming

- Use **kebab-case** with a `.md` extension: `write-tests.md`, `explain-code.md`, `add-error-handling.md`
- The filename should clearly describe what the command does

### Structure

Every command file should contain:

1. **H1 title** -- the command name, matching the filename in natural language
2. **Brief description** -- one or two sentences explaining what the command does
3. **Guidelines or steps** -- bullet points or numbered steps the AI should follow

Optional sections:

- **Output format** -- if the command should produce a specific format
- **Examples** -- sample input/output to clarify expectations

### Content Principles

- Keep each command focused on **one task**
- Use **imperative language** ("Write...", "Analyze...", "Refactor...")
- Be **specific** -- vague commands produce vague results
- Include **constraints** (e.g., "follow the project's existing test patterns")
- Stay **editor-agnostic** in the file content itself; editor-specific setup goes in this README

## Editor Setup

### Cursor

Copy command files to your project:

```
[PROJECT]/.cursor/commands/
```

Commands are invokable via `/` in Cursor's chat panel. Both project-level (`.cursor/commands/`) and global (`~/.cursor/commands/`) locations are supported.

### VS Code (GitHub Copilot)

VS Code does not have a dedicated commands folder. Instead:

- Paste command content directly into **Copilot Chat**
- Or save as an instruction file at `[PROJECT]/.github/instructions/<name>.instructions.md` with a YAML frontmatter `applyTo` glob so Copilot applies it contextually

### WebStorm / JetBrains (GitHub Copilot)

Same as VS Code -- Copilot reads `.github/instructions/` across all JetBrains IDEs.

### Zed

Copy command files to:

```
[PROJECT]/.zed/prompts/
```

Zed surfaces these as "prompts" in the assistant panel. The file format is the same plain Markdown.

### Other Editors

Paste the command content into your AI assistant's chat interface. Commands are plain Markdown and work with any AI tool.

## Example

See [write-tests.md](./write-tests.md) for a reference implementation.
