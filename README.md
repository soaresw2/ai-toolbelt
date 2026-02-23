# AI Toolbelt

A comprehensive, editor-agnostic collection of AI agent tools organized by type: commands, skills, instructions, prompts, and rules.

## 📋 Overview

AI Toolbelt provides ready-to-use templates and tools for AI-assisted development. Instead of organizing by code editor, we organize by **tool type**, making it easy to:

- Find the right tool for your needs
- Adapt tools to any AI-enabled editor
- Understand what each tool type does
- Mix and match tools for your workflow

Simply browse by tool type, copy what you need, and adapt to your editor's format.

## 🎯 Purpose

AI Toolbelt aims to:

- **Provide editor-agnostic tools** that work across different AI assistants
- **Organize by function** (what the tool does) rather than platform (where it runs)
- **Standardize AI interactions** with reusable, tested templates
- **Accelerate development** with pre-built commands, skills, and guidelines
- **Share best practices** for AI-assisted development
- **Enable customization** - all tools are templates you can modify

## 🗂️ Tool Types

### [Commands](./commands/) - Quick Actions

Short, focused instructions for specific code operations.

**Examples:** Write tests, refactor code, add error handling, document code, optimize performance

**Best for:** One-time actions on selected code, tactical operations

**Use in:** Cursor commands, Copilot chat requests, quick AI prompts

[→ Browse Commands](./commands/)

---

### [Skills](./skills/) - AI Capabilities

Comprehensive definitions of specialized AI expertise and capabilities.

**Examples:** Code review, testing, architecture design

**Best for:** Complex, multi-step tasks requiring domain knowledge

**Use in:** Cursor skills, persistent AI context, capability definitions

[→ Browse Skills](./skills/)

---

### [Instructions](./instructions/) - Workflows

Detailed, structured guidelines for complete development workflows.

**Examples:** Feature implementation, bug fixing, acceptance testing, code review process

**Best for:** End-to-end task guidance, team standards, quality criteria

**Use in:** GitHub Copilot instructions, workflow templates, process documentation

[→ Browse Instructions](./instructions/)

---

### [Prompts](./prompts/) - Conversation Templates

Reusable templates that define AI persona and approach for specific interactions.

**Examples:** Explain code, generate tests, improve code quality

**Best for:** Starting AI conversations, defining AI role, chat templates

**Use in:** Zed prompts, AI chat interfaces, conversation starters

[→ Browse Prompts](./prompts/)

---

### [Rules](./rules/) - Universal Standards

Fundamental principles and standards that govern all AI assistance.

**Examples:** Coding standards, security requirements, best practices

**Best for:** Universal constraints, baseline quality standards, security guidelines

**Use in:** Cursor rules, Windsurf rules, project-wide AI guidelines

[→ Browse Rules](./rules/)

## 🚀 Quick Start

### 1. Choose What You Need

Browse the tool type folders to find what matches your needs:
- Need a quick action? → Commands
- Want specialized expertise? → Skills  
- Implementing a workflow? → Instructions
- Starting an AI chat? → Prompts
- Setting standards? → Rules

### 2. Adapt to Your Editor

Each tool type's README explains how to use it in different editors. Common patterns:

**Cursor:**
- Commands → `.cursor/commands/`
- Skills → `.cursor/skills/<name>/SKILL.md`
- Rules → `.cursorrules`

**GitHub Copilot (VSCode, JetBrains, Visual Studio):**
- Instructions → `.github/instructions/`
- Rules → `.github/copilot-instructions.md`
- Commands/Prompts → Use in Copilot Chat

**Zed:**
- Prompts → `.zed/prompts/`
- Rules → `.zed/settings.json`

**Windsurf:**
- Rules → `.windsurfrules`

**Other AI Tools:**
- Use as reference templates
- Copy into chat interfaces
- Adapt format as needed

### 3. Customize and Use

All tools are templates. Modify them to:
- Match your team's standards
- Fit your project's needs
- Align with your tech stack
- Reflect your workflow

## 📚 Documentation

Each tool type folder contains:
- **README.md** - Explains the tool type, format, and usage
- **Example files** - Templates you can use immediately
- **Usage guide** - How to adapt for different editors

## 🎨 Examples

### Example: Setting up Cursor

```bash
# Copy commands
cp ai-toolbelt/commands/*.md .cursor/commands/

# Copy skills (create folder structure)
mkdir -p .cursor/skills/code-review
cp ai-toolbelt/skills/code-review.md .cursor/skills/code-review/SKILL.md

# Copy rules
cp ai-toolbelt/rules/general-coding-rules.md .cursorrules
```

### Example: Setting up GitHub Copilot

```bash
# Copy instructions
mkdir -p .github/instructions
cp ai-toolbelt/instructions/*.md .github/instructions/

# Copy rules into Copilot instructions
cat ai-toolbelt/rules/*.md >> .github/copilot-instructions.md
```

### Example: Using with any AI

```bash
# Just reference the prompts when chatting
cat ai-toolbelt/prompts/explain-code.md
# Copy the content into your AI chat interface
```

## 🔄 Tool Type Comparison

| Tool Type | Scope | Duration | Interactivity | Best For |
|-----------|-------|----------|---------------|----------|
| **Commands** | Narrow | One-time | Immediate | Quick code actions |
| **Skills** | Broad | Persistent | Contextual | Domain expertise |
| **Instructions** | Workflow | Per-task | Guided | Complete processes |
| **Prompts** | Focused | Per-chat | Conversational | AI interactions |
| **Rules** | Universal | Always-on | Background | Quality standards |

## 🤝 Contributing

We welcome contributions! You can:

- Add new tools (commands, skills, instructions, prompts, rules)
- Improve existing tools
- Share editor-specific tips
- Fix issues or typos
- Suggest better organization

**To contribute:**
1. Fork the repository
2. Create tools in the appropriate folder
3. Follow the format described in that folder's README
4. Test with AI assistants
5. Submit a pull request

## 📖 Learn More

- [Commands README](./commands/README.md) - Deep dive into commands
- [Skills README](./skills/README.md) - Understanding AI skills
- [Instructions README](./instructions/README.md) - Workflow guidance
- [Prompts README](./prompts/README.md) - Effective prompting
- [Rules README](./rules/README.md) - Setting standards

## 📄 License

This project is designed to be freely used and modified for any purpose. Copy, adapt, and share as needed.

---

**Tips:**
- Start simple - try one or two tools first
- Combine tools for better results (e.g., Rules + Instructions + Commands)
- Customize tools to match your context
- Share what works with your team
- Iterate based on results
