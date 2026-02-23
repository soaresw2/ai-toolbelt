# AI Toolbelt

A comprehensive collection of portable AI agent instructions, commands, skills, and rules for modern code editors and AI-powered development tools.

## 📋 Overview

This repository provides ready-to-use AI agent configurations for popular code editors. Each editor has its own folder structure with placeholder examples that you can customize for your specific needs. Simply copy the relevant folder into your project to start using AI assistance tailored to your workflow.

## 🎯 Purpose

AI Toolbelt aims to:

- **Standardize AI interactions** across different code editors and projects
- **Provide reusable templates** for common development tasks
- **Accelerate onboarding** by offering pre-configured AI behaviors
- **Share best practices** for AI-assisted development
- **Reduce configuration overhead** when starting new projects

## 🗂️ Supported Editors and Tools

### Cursor

Copy the `.cursor` folder to your project root to add AI commands and skills.

- **Commands** (`.cursor/commands/`): Quick actions you can invoke on selected code
  - `write-tests.md` - Generate comprehensive unit tests
  - `refactor-code.md` - Improve code quality and structure
  - `add-error-handling.md` - Add robust error handling
  - `document-code.md` - Generate code documentation
  - `optimize-performance.md` - Optimize code performance

- **Skills** (`.cursor/skills/`): Specialized capabilities for the AI agent
  - `code-review/` - Thorough code review assistance
  - `testing/` - Comprehensive testing support

### GitHub Copilot (VSCode, Visual Studio, JetBrains IDEs)

Copy the `.github` folder to your project root for Copilot instructions.

- **Instructions** (`.github/instructions/`): Context-specific guidelines for AI behavior
  - `acceptance.instructions.md` - Acceptance testing guidelines
  - `code-review.instructions.md` - Code review standards
  - `bug-fix.instructions.md` - Bug fixing methodology
  - `feature.instructions.md` - Feature implementation approach

### Zed

Copy the `.zed` folder to your project root for custom AI prompts.

- **Prompts** (`.zed/prompts/`): Custom prompt templates
  - `explain-code.md` - Code explanation prompt
  - `generate-tests.md` - Test generation prompt
  - `improve-code.md` - Code quality improvement prompt

### Windsurf (Codeium)

Copy the `windsurf` folder to your project root for AI rules.

- **Rules** (`.windsurfrules`): General coding principles and guidelines
  - Code style and quality standards
  - Testing requirements
  - Security best practices
  - Documentation guidelines

## 🚀 Getting Started

1. **Choose your editor**: Navigate to the folder for your code editor
2. **Copy to your project**: Copy the entire folder structure to your project root
3. **Customize**: Edit the markdown files to match your project's specific needs
4. **Use**: Invoke commands, skills, or let instructions guide the AI's behavior

### Example: Setting up Cursor

```bash
# From this repository
cp -r .cursor /path/to/your/project/

# Now you can use Cursor's command palette to access:
# - Write Tests
# - Refactor Code
# - Add Error Handling
# - Document Code
# - Optimize Performance
```

### Example: Setting up GitHub Copilot

```bash
# From this repository
cp -r .github /path/to/your/project/

# Copilot will now follow the instructions in .github/instructions/
# when you're working on features, bug fixes, tests, or code reviews
```

## 📝 Customization

All files are markdown templates designed to be edited. Customize them to:

- Match your team's coding standards
- Reflect your project's specific requirements
- Align with your organization's best practices
- Add or remove guidelines as needed

## 🤝 Contributing

Contributions are welcome! If you have:

- Additional commands or skills for existing editors
- Support for new AI-enabled editors
- Improvements to existing templates
- Better organizational structures

Please feel free to submit a pull request.

## 📄 License

This project is designed to be freely used and modified for any purpose. Copy, adapt, and share as needed.

## 🔗 Related Resources

- [Cursor Documentation](https://cursor.sh/docs)
- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Zed Editor Documentation](https://zed.dev/docs)
- [Windsurf Documentation](https://docs.codeium.com/windsurf)

---

**Note**: The templates in this repository are starting points. Adapt them to your specific project needs, team conventions, and workflow preferences. 
