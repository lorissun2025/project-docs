# Contributing to Project Docs

Thank you for your interest in contributing to Project Docs! This document provides guidelines and instructions for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Message Guidelines](#commit-message-guidelines)

## Code of Conduct

Please be respectful and constructive in all interactions. We aim to maintain a welcoming and inclusive community for all contributors.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- Use a clear and descriptive title
- Describe the exact steps to reproduce the problem
- Provide specific examples to demonstrate the steps
- Describe the behavior you expected and what actually happened
- Include your environment details (OS, Claude Code version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- Use a clear and descriptive title
- Provide a detailed description of the suggested enhancement
- Explain why this enhancement would be useful
- List some examples of how this feature would be used

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** with clear, descriptive commit messages
3. **Test your changes** thoroughly
4. **Submit a pull request** with a clear description of the changes

#### Pull Request Guidelines

- Keep PRs focused on a single issue or feature
- Update documentation as needed
- Follow the existing code style and format
- Add comments to complex code sections
- Test your changes before submitting

## Development Setup

1. Fork and clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/project-docs.git
   cd project-docs
   ```

2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make your changes and test locally

4. Commit your changes:
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```

5. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

6. Create a Pull Request on GitHub

## Coding Standards

### Markdown Style

- Use consistent markdown formatting
- Keep lines under 100 characters when possible
- Use proper heading hierarchy (# ## ###)
- Include blank lines between paragraphs and list items

### Template Files

When updating template files:
- Maintain the existing structure and format
- Use placeholder text that clearly indicates what should be filled in
- Include helpful comments or instructions where appropriate
- Ensure Chinese and English versions are consistent

### Skill File (SKILL.md)

The main skill file should:
- Clearly describe when to use the skill
- Provide concrete examples
- Maintain the existing structure
- Update workflow descriptions when behavior changes

## Commit Message Guidelines

We follow a simple commit message convention:

```
<type>: <description>
```

### Types

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that don't affect code meaning (formatting, etc.)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `test`: Adding or updating tests
- `chore`: Changes to build process or auxiliary tools

### Examples

```
feat: add new template for API documentation
fix: correct roadmap progress calculation
docs: update README with new installation instructions
refactor: simplify template structure
```

## Adding New Templates

When adding new document templates:

1. Create the template in `assets/templates/`
2. Follow the existing naming convention: `NAME-TEMPLATE.md`
3. Update `SKILL.md` to reference the new template
4. Update `README.md` to document the new template
5. Include a brief description of when to use the template

## Questions?

If you have questions about contributing, please:
1. Check existing issues and discussions
2. Create a new issue with the `question` label
3. We'll respond as soon as possible

Thank you for contributing to Project Docs! 🎉
