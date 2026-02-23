# Migration Guide

This document helps you migrate from the old editor-specific structure to the new tool-type organization.

## What Changed?

The repository has been restructured to be **editor-agnostic**, organizing tools by **type** rather than by **editor**.

### Old Structure (Editor-Based)

```
.cursor/
  commands/
  skills/
.github/
  instructions/
.zed/
  prompts/
windsurf/
  .windsurfrules
```

### New Structure (Tool-Type Based)

```
commands/        - Quick actions (formerly in .cursor/commands/)
skills/          - AI capabilities (formerly in .cursor/skills/)
instructions/    - Workflows (formerly in .github/instructions/)
prompts/         - Conversation templates (formerly in .zed/prompts/)
rules/           - Universal standards (formerly in windsurf/.windsurfrules)
```

## File Mapping

### Commands
- `.cursor/commands/*.md` → `commands/*.md`
- No changes to file content or names

### Skills
- `.cursor/skills/code-review/SKILL.md` → `skills/code-review.md`
- `.cursor/skills/testing/SKILL.md` → `skills/testing.md`
- Structure flattened (no subdirectories)

### Instructions
- `.github/instructions/*.instructions.md` → `instructions/*.instructions.md`
- No changes to file content or names

### Prompts
- `.zed/prompts/*.md` → `prompts/*.md`
- No changes to file content or names

### Rules
- `windsurf/.windsurfrules` → `rules/general-coding-rules.md`
- File renamed for clarity

## How to Migrate Your Projects

If you were using the old structure, here's how to update:

### For Cursor Users

**Old way:**
```bash
cp -r ai-toolbelt/.cursor .
```

**New way:**
```bash
# Commands
cp ai-toolbelt/commands/*.md .cursor/commands/

# Skills (note the structure change)
mkdir -p .cursor/skills/code-review
cp ai-toolbelt/skills/code-review.md .cursor/skills/code-review/SKILL.md

mkdir -p .cursor/skills/testing
cp ai-toolbelt/skills/testing.md .cursor/skills/testing/SKILL.md

# Rules
cp ai-toolbelt/rules/general-coding-rules.md .cursorrules
```

### For GitHub Copilot Users

**Old way:**
```bash
cp -r ai-toolbelt/.github .
```

**New way:**
```bash
# Instructions
mkdir -p .github/instructions
cp ai-toolbelt/instructions/*.md .github/instructions/

# Rules
cat ai-toolbelt/rules/*.md >> .github/copilot-instructions.md
```

### For Zed Users

**Old way:**
```bash
cp -r ai-toolbelt/.zed .
```

**New way:**
```bash
# Prompts
mkdir -p .zed/prompts
cp ai-toolbelt/prompts/*.md .zed/prompts/

# Rules (add to settings)
# Copy content from ai-toolbelt/rules/*.md to your .zed/settings.json
```

### For Windsurf Users

**Old way:**
```bash
cp ai-toolbelt/windsurf/.windsurfrules .windsurfrules
```

**New way:**
```bash
cp ai-toolbelt/rules/general-coding-rules.md .windsurfrules
```

## Benefits of the New Structure

1. **Editor-Agnostic**: Tools are organized by function, not by editor
2. **Better Documentation**: Each tool type has a comprehensive README
3. **Easier Discovery**: Find what you need based on what it does
4. **Flexible Adaptation**: Easy to adapt to any AI-enabled editor
5. **Clear Comparisons**: Understand when to use each tool type
6. **Consistent Format**: All tools follow documented format conventions

## Getting Help

- Read the [main README](./README.md) for an overview
- Check each tool type's README for specific guidance:
  - [Commands README](./commands/README.md)
  - [Skills README](./skills/README.md)
  - [Instructions README](./instructions/README.md)
  - [Prompts README](./prompts/README.md)
  - [Rules README](./rules/README.md)

## Questions?

If you have questions about the migration or new structure:
1. Check the README files in each folder
2. Look at the examples in the main README
3. Open an issue on GitHub
4. Submit a pull request with improvements
