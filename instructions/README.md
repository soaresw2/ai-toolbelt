# Instructions

Instructions are detailed, structured guidelines that define how an AI agent should approach a complete development workflow. They cover multi-step processes like implementing a feature, fixing a bug, or conducting a code review.

## When to Use Instructions

Use instructions when you need:

- End-to-end guidance for a development workflow
- Step-by-step processes with phases, criteria, and checklists
- Team alignment on how specific task types should be approached
- Quality gates and acceptance criteria for a workflow

If you need a quick one-off action, use a [command](../commands/). If you need always-on coding standards, use [rules](../rules/).

## Writing Guidelines

### File Naming

- Use **kebab-case** with an `.instructions.md` suffix: `feature.instructions.md`, `bug-fix.instructions.md`
- The name should describe the workflow or task type

### Structure

Every instruction file should contain:

1. **H1 title** -- the workflow name
2. **Introduction** -- brief description of when and why to use this workflow
3. **Phases or sections** -- organized chronologically or by concern (planning, implementation, testing, review)
4. **Steps within each phase** -- numbered or bulleted, specific and actionable
5. **Checklist** (recommended) -- a summary checklist at the end for quick verification

### Content Principles

- Be **prescriptive** -- instructions should leave little room for interpretation
- Organize **logically** -- chronological order or by area of concern
- Include both **what** to do and **why** (rationale helps the AI make judgment calls)
- Add **quality criteria** so the AI knows what "done" looks like
- Keep each file focused on **one workflow**
- Stay **editor-agnostic** in the file content itself

## Editor Setup

### VS Code / WebStorm (GitHub Copilot) -- Primary

This is the tool type that maps most directly to GitHub Copilot's instruction system. Copy instruction files to:

```
[PROJECT]/.github/instructions/
```

Copilot auto-applies instructions contextually. You can add YAML frontmatter to control when an instruction applies:

```yaml
---
applyTo: "src/**/*.ts"
---
```

This works across VS Code, WebStorm, and all JetBrains IDEs with the Copilot plugin.

### Cursor

Cursor does not have a direct "instructions" concept. Adapt instruction content into one of:

- **Rules**: `[PROJECT]/.cursor/rules/<name>.mdc` with glob patterns to auto-apply when editing matching files
- **Commands**: `[PROJECT]/.cursor/commands/<name>.md` to invoke the workflow manually via `/` in chat

### Zed

No direct equivalent. Reference instruction content in the assistant panel or paste relevant sections into chat when starting a workflow.

### Other Editors

Use instruction files as reference documentation. Paste the relevant sections into your AI assistant's chat when beginning a task.

## Example

See [_example-feature.instructions.md](./_example-feature.instructions.md) for a reference implementation. This file exists solely to illustrate the expected format -- it is not intended to be copied into your project as-is.
