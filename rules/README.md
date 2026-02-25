# Rules

Rules are always-on standards and principles that govern how AI should assist with code across all tasks and interactions. They define the baseline expectations for code quality, security, testing, and other non-negotiable concerns.

Rules are the **most universally supported** tool type -- virtually every AI-enabled editor has a mechanism for them.

## When to Use Rules

Use rules when you need:

- Universal coding standards applied to every AI interaction
- Security, performance, or quality constraints that must always hold
- Consistent baseline behavior regardless of the specific task
- Non-negotiable requirements (input validation, error handling patterns, naming conventions)

If you need task-specific workflow guidance, use [instructions](../instructions/). If you need one-off actions, use [commands](../commands/).

## Writing Guidelines

### File Naming

- Use **kebab-case** with a `.md` extension: `general-coding-rules.md`, `security-rules.md`
- The name should describe the category or domain the rules cover

### Structure

Every rules file should contain:

1. **H1 title** -- the rules category
2. **Sections by topic** -- group related rules under H2 headings (e.g., "Code Style," "Security," "Testing")
3. **Rules as bullet points** -- clear, enforceable statements within each section

### Content Principles

- Use **"must"** and **"must not"** rather than "should" or "consider" -- rules are requirements, not suggestions
- Keep each rule **specific and verifiable** -- an AI (or human) should be able to check compliance
- Provide **brief rationale** for non-obvious rules
- Organize by **topic** so rules are easy to find and reference
- Avoid overly prescriptive rules that constrain the AI unnecessarily
- Stay **editor-agnostic** in the file content itself

## Editor Setup

Rules have the broadest editor support of any tool type.

### Cursor

Adapt rule content into Cursor's `.mdc` format with YAML frontmatter:

```
[PROJECT]/.cursor/rules/<name>.mdc
```

Example frontmatter for always-on rules:

```yaml
---
description: General coding standards
alwaysApply: true
---
```

You can also scope rules to specific files using `globs`:

```yaml
---
description: React component standards
globs: src/components/**/*.tsx
---
```

### VS Code / WebStorm (GitHub Copilot)

Copy rule content into:

```
[PROJECT]/.github/copilot-instructions.md
```

This single file is automatically read by Copilot in VS Code, WebStorm, and all JetBrains IDEs. All content in this file applies to every Copilot interaction in the project.

### Zed

Add rule content to assistant context in:

```
[PROJECT]/.zed/settings.json
```

under the assistant configuration section. Refer to Zed's documentation for the exact schema.

### Windsurf

Copy rule content into:

```
[PROJECT]/.windsurfrules
```

Windsurf automatically applies this file to all AI interactions in the project.

### Cline

Copy rule content into the project rules directory:

```
[PROJECT]/.clinerules/
```

### Codex CLI

Embed rule content in:

```
[PROJECT]/AGENTS.md
```

Codex auto-discovers `AGENTS.md` from the git root.

## Example

See [_example-general-coding-rules.md](./_example-general-coding-rules.md) for a reference implementation. This file exists solely to illustrate the expected format -- it is not intended to be copied into your project as-is.
