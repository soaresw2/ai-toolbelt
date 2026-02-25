# AI Toolbelt

A shared collection of AI instruction files for development teams. Browse by tool type, copy what you need into your project, and adapt it to your editor.

## Tool Types

| Folder | Purpose | When to Use | Example |
|--------|---------|-------------|---------|
| [commands/](./commands/) | Quick, focused directives for specific code actions or AI personas | You need a one-off action ("write tests") or a reusable chat template ("you are an expert reviewer") | `_example-write-tests.md` |
| [instructions/](./instructions/) | Detailed workflow guidance for complete development processes | You need end-to-end steps for a task type like feature implementation or bug fixing | `_example-feature.instructions.md` |
| [rules/](./rules/) | Always-on standards and principles governing all AI interactions | You need universal coding standards, security constraints, or quality baselines | `_example-general-coding-rules.md` |
| [skills/](./skills/) | Domain expertise definitions for complex, multi-step tasks | You need deep, persistent AI expertise in an area like code review or testing | `_example-code-review.md` |

### How to Choose

- **"Do this specific thing right now"** -- use a **command**
- **"Here's how to approach this type of work"** -- use an **instruction**
- **"Always follow these standards"** -- use a **rule**
- **"Be an expert in this domain"** -- use a **skill**

Commands and instructions are invoked for specific tasks. Rules and skills provide persistent context that applies across all tasks.

## Quick Start

1. Browse the folder that matches your need
2. Read the folder's `README.md` for writing guidelines and editor setup
3. Copy the file into the correct location for your editor (see below)
4. Customize the content to match your project and team standards

## Editor Compatibility

Each folder README contains detailed setup instructions. Here is a summary of where files go for each editor:

| Tool Type | Cursor | VS Code / WebStorm (Copilot) | Zed |
|-----------|--------|------------------------------|-----|
| Commands | `.cursor/commands/` | `.github/instructions/` or Copilot Chat | `.zed/prompts/` |
| Instructions | `.cursor/rules/` or `.cursor/commands/` | `.github/instructions/` | Paste into assistant chat |
| Rules | `.cursor/rules/` (`.mdc` format) | `.github/copilot-instructions.md` | `.zed/settings.json` |
| Skills | `.cursor/skills/<name>/SKILL.md` | `.github/instructions/` | Paste into assistant chat |

Other editors (Windsurf, Cline, Codex CLI) are also covered in the individual folder READMEs.

## Project Governance

This repository includes global instruction files that help AI agents validate changes when you contribute:

| File | Editor |
|------|--------|
| [.cursor/rules/project-guardian.mdc](.cursor/rules/project-guardian.mdc) | Cursor |
| [.github/copilot-instructions.md](.github/copilot-instructions.md) | VS Code, WebStorm, JetBrains IDEs |
| [AGENTS.md](AGENTS.md) | Codex CLI, Cline, and other tools |

These files instruct the AI to verify that new or modified files conform to the folder's guidelines, and to suggest improvements for clarity, completeness, and actionability.

## Contributing

1. Pick the folder that matches the type of file you want to add
2. Read that folder's `README.md` for naming conventions, structure, and content guidelines
3. Create your file following the guidelines
4. The project's global instruction files will help your AI assistant validate the change
5. Submit a pull request

Each folder contains one example file (prefixed with `_example-`) as a format reference. These are **not** meant to be copied as-is into your project. When contributing, add new files alongside the existing example -- do not replace it.

## Repository Structure

```
ai-toolbelt/
  commands/
    README.md
    _example-write-tests.md
  instructions/
    README.md
    _example-feature.instructions.md
  rules/
    README.md
    _example-general-coding-rules.md
  skills/
    README.md
    _example-code-review.md
  .cursor/rules/
    project-guardian.mdc
  .github/
    copilot-instructions.md
  AGENTS.md
  README.md
```
