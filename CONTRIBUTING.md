# Contributing to Synalinks Vibe

Thank you for your interest in contributing to Synalinks Vibe! This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Style Guidelines](#style-guidelines)
- [Submitting Changes](#submitting-changes)

## Code of Conduct

We are committed to providing a welcoming and inclusive environment for all contributors. Please be respectful and constructive in all interactions.

### Our Standards

- Be respectful and inclusive
- Welcome newcomers and help them get started
- Focus on constructive feedback
- Acknowledge contributions from others

## Getting Started

### Prerequisites

Before contributing, ensure you have:
- Python 3.9 or higher
- Git installed and configured
- Cursor IDE (recommended) or VS Code
- Basic understanding of vibe coding principles

### Setting Up Your Development Environment

1. **Fork and Clone the Repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/synalinks-vibe.git
   cd synalinks-vibe
   ```

2. **Set Up Virtual Environment**
   ```bash
   pip install uv
   uv venv
   source .venv/bin/activate  # or .venv\Scripts\activate on Windows
   ```

3. **Install Dependencies**
   ```bash
   uv pip install -r requirements.txt
   ```

4. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

## How to Contribute

### Reporting Bugs

If you find a bug, please create an issue with:
- A clear, descriptive title
- Steps to reproduce the issue
- Expected behavior
- Actual behavior
- Your environment (OS, Python version, etc.)
- Screenshots or error messages if applicable

### Suggesting Features

We welcome feature suggestions! Please create an issue with:
- A clear description of the feature
- Use cases and examples
- Why this feature would be useful
- Any implementation ideas you have

### Improving Documentation

Documentation improvements are always welcome:
- Fix typos or clarify existing docs
- Add examples or use cases
- Improve README or guides
- Add or update API documentation

## Development Workflow

### 1. Documentation Changes

For documentation-only changes:
1. Make your changes
2. Preview the documentation locally if possible
3. Submit a pull request

### 2. Code Changes

For code changes:
1. Write clear, focused code
2. Follow the project's style guidelines
3. Add or update tests if applicable
4. Update documentation as needed
5. Ensure all tests pass

### 3. AI-Assisted Development

This project uses vibe coding principles:
- Use natural language to describe features
- Leverage AI assistance for implementation
- Review and refine AI-generated code
- Document AI interactions in `.ai/session/` if significant

## Style Guidelines

### Python Code Style

- Follow PEP 8 guidelines
- Use type hints for function parameters and return values
- Write docstrings for all public functions and classes
- Keep functions focused and small
- Use meaningful variable names

### Documentation Style

- Use clear, concise language
- Provide examples where helpful
- Use proper Markdown formatting
- Keep line length reasonable (80-100 characters)
- Include code blocks with proper syntax highlighting

### Git Commit Messages

Follow these guidelines for commit messages:
- Use the imperative mood ("Add feature" not "Added feature")
- Keep the first line under 50 characters
- Add a blank line before detailed description
- Reference issues and PRs when relevant

Example:
```
Add vibe coding pattern documentation

- Created comprehensive guide for vibe coding patterns
- Added examples for common use cases
- Updated README with link to new documentation

Fixes #123
```

## Submitting Changes

### Pull Request Process

1. **Before Submitting**
   - Ensure your code follows style guidelines
   - Run tests and ensure they pass
   - Update documentation as needed
   - Rebase your branch on the latest main if needed

2. **Creating the Pull Request**
   - Use a clear, descriptive title
   - Describe what changes you made and why
   - Reference any related issues
   - Include screenshots for UI changes
   - Add test results if applicable

3. **Pull Request Template**
   ```markdown
   ## Description
   Brief description of changes

   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Code refactoring

   ## Testing
   - [ ] Tests pass locally
   - [ ] Added new tests for changes
   - [ ] Updated documentation

   ## Related Issues
   Fixes #(issue number)
   ```

4. **After Submission**
   - Respond to review comments promptly
   - Make requested changes in new commits
   - Keep the PR focused and avoid scope creep

### Review Process

- All submissions require review from maintainers
- Reviews typically happen within 2-3 business days
- Address feedback constructively
- Be patient and respectful with reviewers

## Types of Contributions We're Looking For

### High Priority
- Bug fixes
- Documentation improvements
- Performance optimizations
- Test coverage improvements
- Security fixes

### Welcome Contributions
- New examples and tutorials
- AI prompt templates
- Development tools and utilities
- Integration guides
- Translation of documentation

### Discuss First
- Major architectural changes
- Breaking changes to APIs
- New dependencies
- Changes to core behavior

## Getting Help

If you need help with your contribution:
- Check existing documentation and issues
- Ask in GitHub Discussions
- Join our Discord community
- Tag maintainers in your PR if stuck

## Recognition

We value all contributions and recognize contributors:
- Contributors are acknowledged in release notes
- Significant contributions may be highlighted
- Active contributors may be invited as collaborators

## License

By contributing to Synalinks Vibe, you agree that your contributions will be licensed under the MIT License.

## Questions?

If you have questions about contributing, please:
- Open a GitHub Discussion
- Create an issue with the "question" label
- Reach out in our Discord community

Thank you for contributing to Synalinks Vibe!
