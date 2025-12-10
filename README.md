# AGENTS.md Template

A standardized template for providing development guidelines to AI coding agents working with your codebase.

## What is AGENTS.md?

AGENTS.md is an open standard for communicating development guidelines, coding standards, and project-specific best practices to AI coding agents like Claude Code, GitHub Copilot, Cursor, Aider, and others.

By including an `AGENTS.md` file in your repository, you give AI agents context about:
- Your development philosophy and principles
- Code quality standards and testing requirements
- Decision-making frameworks
- Project-specific conventions and patterns

## How to Use This Template

1. **Copy to your project**: Add the `AGENTS.md` file to the root of your repository
2. **Customize**: Modify sections to match your project's specific needs, tech stack, and conventions
3. **Commit**: Check it into version control so it's available to all contributors (human and AI)

## AI Agent Support

### Agents with Native Support

Some AI coding agents automatically detect and read `AGENTS.md` files:
- Claude Code
- (Check your agent's documentation for AGENTS.md support)

### Manual Reference Required

For agents that don't automatically detect `AGENTS.md`, you'll need to manually reference it:

**Examples:**
- "Please read the AGENTS.md file before making changes"
- "Follow the guidelines in AGENTS.md for this implementation"
- Copy relevant sections into your prompt or project instructions

### Integration Tips

- **Cursor/VS Code**: Add AGENTS.md to your workspace instructions or `.cursorrules`
- **GitHub Copilot**: Reference in PR templates or contributing guidelines
- **Custom agents**: Configure to read AGENTS.md on initialization

## What's Included

This template covers:
- **Development Philosophy**: Core principles and simplicity guidelines
- **Development Process**: Exploration, implementation cycle, and what to do when stuck
- **Code Standards**: Architecture patterns, quality requirements, and error handling
- **Decision Framework**: Prioritization criteria for choosing between approaches
- **Testing Guidelines**: Best practices for writing and maintaining tests
- **Quality Checklist**: Pre-commit verification items

## Customization

Feel free to:
- Add project-specific sections (e.g., "API Design", "Database Conventions")
- Include language or framework-specific guidelines
- Reference your existing style guides or documentation
- Add examples from your codebase

## Learn More

- [AGENTS.md Standard](https://agents.md/) - The official standard documentation

## License

This template is provided as-is for use in any project. Modify freely to suit your needs.
