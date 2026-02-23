# Rules

Rules are fundamental principles and standards that govern how AI should assist with code across all tasks and interactions.

## What are Rules?

Rules define overarching guidelines that:
- Apply universally across all AI interactions
- Establish coding standards and best practices
- Set quality expectations and requirements
- Define security and safety constraints
- Provide consistent behavior guardrails

Rules are the most foundational tool type - they set the baseline for all AI assistance.

## File Format

Each rules file is a Markdown document with:
- **Filename**: Descriptive kebab-case name (e.g., `general-coding-rules.md`, `security-rules.md`)
- **Title**: H1 header with the rules category
- **Sections**: Organized by topic or domain
- **Rules**: Clear, enforceable statements
- **Format**: Can use bullets, numbered lists, or subsections

### Example Structure

```markdown
# Rule Category Name

## Topic Area 1

- Rule 1
- Rule 2
- Rule 3

## Topic Area 2

- Rule 1
- Rule 2

## Principles

- Overarching principle 1
- Overarching principle 2
```

## Usage in Different Editors

### Windsurf (Codeium)
1. Copy rules to `windsurf/.windsurfrules` in your project
2. Windsurf automatically applies these rules
3. Rules affect all AI suggestions and completions

### Cursor
1. Add rules to `.cursorrules` file in project root
2. Or include in `.cursor/rules/`
3. Cursor uses these as global context

### GitHub Copilot
1. Include in `.github/copilot-instructions.md`
2. Or add to workspace settings
3. Rules apply across all Copilot interactions

### Other Editors
- Add to project documentation
- Include in AI system prompts or settings
- Reference when onboarding new AI tools
- Use as code review checklist

## Available Rules

- **general-coding-rules.md** - Universal coding standards covering:
  - Code style and quality
  - Testing requirements
  - Error handling
  - Security practices
  - Performance considerations
  - Documentation standards
  - Git practices
  - General principles (SOLID, DRY, KISS, YAGNI)

## Creating Custom Rules

To create new rules:
1. Identify a domain or aspect that needs consistent standards
2. Create a `.md` file with a descriptive name
3. Organize rules by topic or category
4. Write clear, actionable rules (not suggestions)
5. Focus on "must" and "must not" rather than "should"
6. Include rationale for non-obvious rules
7. Consider security, performance, and maintainability
8. Test that AI assistants can follow the rules
9. Update as standards evolve
10. Share via pull request

## Best Practices

- Make rules clear and unambiguous
- Focus on important, enforceable standards
- Organize logically by topic
- Avoid overly prescriptive rules that limit creativity
- Include security and safety rules prominently
- Update regularly as best practices change
- Keep rules concise (AI has token limits)
- Consider team consensus for custom rules
- Document exceptions when necessary

## Types of Rules to Consider

### Code Quality
- Naming conventions
- Code organization
- Complexity limits
- Documentation requirements

### Security
- Input validation
- Authentication/authorization
- Data protection
- Vulnerability prevention

### Testing
- Coverage requirements
- Testing standards
- Test organization

### Performance
- Optimization guidelines
- Resource management
- Scalability considerations

### Process
- Git workflow
- Code review standards
- Deployment practices

## Rules vs Other Tool Types

**Use Rules when:**
- Setting universal standards for all code
- Defining non-negotiable requirements
- Establishing security constraints
- Creating consistent baseline behavior

**Use Instructions when:**
- Defining specific workflows
- Providing task-specific guidance
- Describing multi-step processes

**Use Skills when:**
- Enabling domain expertise
- Defining complex capabilities

**Use Commands when:**
- Creating specific actions
- Enabling one-time operations

**Use Prompts when:**
- Starting AI conversations
- Defining interaction templates

## Combining Rules with Other Tools

Rules work best when combined with other tool types:
- **Rules + Instructions**: Rules ensure quality while instructions guide workflow
- **Rules + Skills**: Skills apply expertise within the bounds of rules
- **Rules + Commands**: Commands execute while respecting rules
- **Rules + Prompts**: Prompts can reference rules for context

## Rule Enforcement

Remember that AI assistants:
- Will try to follow rules but may make mistakes
- Work best with clear, specific rules
- May need reminders for complex or numerous rules
- Benefit from examples of rule application
- Should be reviewed by humans for compliance
