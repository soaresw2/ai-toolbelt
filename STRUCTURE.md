# Repository Structure

This document provides a visual overview of the AI Toolbelt repository structure.

```
ai-toolbelt/
│
├── .cursor/                          # Cursor editor AI configurations
│   ├── commands/                     # Quick AI commands for code actions
│   │   ├── write-tests.md
│   │   ├── refactor-code.md
│   │   ├── add-error-handling.md
│   │   ├── document-code.md
│   │   └── optimize-performance.md
│   │
│   └── skills/                       # Specialized AI capabilities
│       ├── code-review/
│       │   └── SKILL.md
│       └── testing/
│           └── SKILL.md
│
├── .github/                          # GitHub Copilot configurations
│   └── instructions/                 # Context-specific AI guidelines
│       ├── acceptance.instructions.md
│       ├── bug-fix.instructions.md
│       ├── code-review.instructions.md
│       └── feature.instructions.md
│
├── .zed/                             # Zed editor AI configurations
│   └── prompts/                      # Custom AI prompt templates
│       ├── explain-code.md
│       ├── generate-tests.md
│       └── improve-code.md
│
├── windsurf/                         # Windsurf (Codeium) AI configurations
│   └── .windsurfrules               # General coding rules and principles
│
├── README.md                         # Main documentation
└── STRUCTURE.md                      # This file
```

## How to Use This Structure

### For Cursor Users
Copy the `.cursor` folder to your project:
```bash
cp -r .cursor /path/to/your/project/
```

### For GitHub Copilot Users (VSCode, Visual Studio, JetBrains)
Copy the `.github` folder to your project:
```bash
cp -r .github /path/to/your/project/
```

### For Zed Users
Copy the `.zed` folder to your project:
```bash
cp -r .zed /path/to/your/project/
```

### For Windsurf Users
Copy the `windsurf` folder to your project:
```bash
cp -r windsurf /path/to/your/project/
```

## Folder Naming Conventions

- **Dotfiles (`.cursor`, `.github`, `.zed`)**: These are hidden folders that editors recognize
- **Plain folders (`windsurf`)**: Regular folders for editors that use different conventions
- **Markdown files (`.md`)**: All configuration files use Markdown for easy editing

## Customization

Each file is a template. Modify them to:
- Add project-specific guidelines
- Remove irrelevant instructions
- Add new commands or skills
- Match your team's workflow

## Adding New Editors

When adding support for a new editor:
1. Research the editor's AI configuration structure
2. Create the appropriate folder structure
3. Add placeholder examples following the editor's conventions
4. Update the README.md with usage instructions
5. Update this STRUCTURE.md file
