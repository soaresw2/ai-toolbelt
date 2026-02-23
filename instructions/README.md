# Instructions

Instructions are context-specific guidelines that define how an AI agent should approach particular types of development tasks or workflows.

## What are Instructions?

Instructions provide detailed, structured guidance for:
- Specific development workflows (e.g., feature implementation, bug fixing)
- Task-specific best practices and methodologies
- Step-by-step approaches to common scenarios
- Quality standards and review criteria
- Process guidelines and checklists

Instructions are more prescriptive than skills and more comprehensive than commands.

## File Format

Each instruction set is a Markdown file with:
- **Filename**: Task-oriented kebab-case name with `.instructions.md` suffix
- **Title**: H1 header describing the task or workflow
- **Sections**: Organized by phase or aspect of the workflow
- **Guidelines**: Detailed steps, criteria, or best practices
- **Checklists**: Optional task lists for verification

### Example Structure

```markdown
# Task Type Instructions

Brief introduction to the task or workflow.

## Phase 1

Guidelines for phase 1:
- Guideline 1
- Guideline 2

## Phase 2

Steps for phase 2:
1. Step 1
2. Step 2

## Best Practices

- Best practice 1
- Best practice 2

## Checklist

- [ ] Item 1
- [ ] Item 2
```

## Usage in Different Editors

### GitHub Copilot (Primary Use Case)
1. Copy instruction files to `.github/instructions/` in your project
2. Copilot automatically uses these as context
3. Instructions apply when working on relevant tasks
4. Name files clearly so Copilot can match them to contexts

### Cursor
1. Copy to `.cursor/` or reference in custom commands
2. Use as templates for complex workflows
3. Reference in agent rules or context

### VSCode with Copilot
1. Place in `.github/instructions/`
2. Copilot reads and applies contextually
3. Works across VSCode, Visual Studio, and JetBrains IDEs

### Other Editors
- Use as reference documentation for AI-assisted workflows
- Copy relevant sections into AI chat when starting tasks
- Maintain as team standards documentation

## Available Instructions

- **acceptance.instructions.md** - Guidelines for writing acceptance tests
- **bug-fix.instructions.md** - Systematic approach to fixing bugs
- **code-review.instructions.md** - Standards for conducting code reviews
- **feature.instructions.md** - Process for implementing new features

## Creating Custom Instructions

To create new instructions:
1. Identify a recurring development workflow or task type
2. Create a `.instructions.md` file named after the task
3. Structure the content by phases, steps, or aspects
4. Include specific, actionable guidelines
5. Add quality criteria or checklists
6. Consider edge cases and common pitfalls
7. Test with your team's AI tools
8. Iterate based on feedback
9. Share via pull request

## Best Practices

- Be specific and prescriptive
- Structure logically (chronologically or by aspect)
- Include both "what" and "why"
- Provide examples where helpful
- Use checklists for verification steps
- Keep instructions focused on one workflow
- Update as processes evolve
- Make them team-agnostic when possible

## Instructions vs Skills vs Commands

**Use Instructions when:**
- Defining a complete workflow or process
- Multiple steps span different activities
- Quality standards need to be specified
- Team alignment on approach is important

**Use Skills when:**
- Defining ongoing AI capabilities
- Domain expertise is needed
- Context persists across multiple tasks

**Use Commands when:**
- Quick, focused actions are needed
- Operating on specific code selections
- One-time tactical operations
