# Contributing to Terminal Skills

Thank you for your interest in contributing to Terminal Skills! This document provides guidelines and instructions for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Creating a New Skill](#creating-a-new-skill)
- [Skill Quality Standards](#skill-quality-standards)
- [Pull Request Process](#pull-request-process)
- [Style Guide](#style-guide)
- [Reporting Issues](#reporting-issues)

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- Keep discussions technical and professional

## How to Contribute

There are several ways to contribute:

1. **Add new skills** - Create skills for tools not yet covered
2. **Improve existing skills** - Fix errors, add examples, improve documentation
3. **Report issues** - Found a bug or outdated command? Let us know
4. **Suggest ideas** - Have an idea for a new skill category?

## Creating a New Skill

### Step 1: Fork and Clone

```bash
# Fork the repository on GitHub, then:
git clone https://github.com/YOUR-USERNAME/terminal-skills.git
cd terminal-skills
```

### Step 2: Create a Branch

```bash
git checkout -b feature/skill-name
```

### Step 3: Create Skill Structure

Create your skill folder under the appropriate category:

```
category/skill-name/
├── SKILL.md          # Required - Main skill file
├── examples/         # Recommended - Usage examples
│   └── example-1.md
├── scripts/          # Optional - Helper scripts
│   └── helper.sh
└── resources/        # Optional - Additional references
    └── reference.md
```

### Step 4: Write SKILL.md

Use this template:

```markdown
---
name: skill-name
description: One-line description of the skill
version: 1.0.0
author: your-github-username
tags: [tag1, tag2, tag3]
---

# Skill Title

## Overview

Describe what this skill covers, its purpose, and target audience.
Include when and why someone would use this skill.

## Prerequisites

- Required tools or software
- Minimum versions
- Permission requirements
- Environment setup

## Core Commands

### Category 1

```bash
# Description of what this command does
command --option value

# Another useful command
another-command --flag
```

### Category 2

```bash
# More commands organized by function
command-group operation
```

## Common Scenarios

### Scenario 1: Descriptive Title

Explain the use case, then provide step-by-step commands:

```bash
# Step 1: Do this
first-command

# Step 2: Then this
second-command

# Step 3: Finally
final-command
```

### Scenario 2: Another Use Case

Another real-world example with commands...

## Best Practices

- Tip 1 for using this tool effectively
- Tip 2 for avoiding common mistakes
- Tip 3 for production environments

## Troubleshooting

| Problem | Cause | Solution |
|---------|-------|----------|
| Error message 1 | Why it happens | How to fix |
| Error message 2 | Why it happens | How to fix |

## References

- [Official Documentation](https://example.com)
- [Useful Tutorial](https://example.com)
```

### Step 5: Test Your Commands

**Important:** All commands should be tested and verified to work.

- Test on the target platform (Linux, macOS, etc.)
- Verify command syntax is correct
- Ensure examples produce expected output
- Check that troubleshooting solutions actually work

### Step 6: Submit Pull Request

```bash
git add .
git commit -m "feat: add skill-name skill"
git push origin feature/skill-name
```

Then create a Pull Request on GitHub.

## Skill Quality Standards

### Required Elements

- [ ] **Frontmatter** - Complete YAML frontmatter with name, description, version, author, tags
- [ ] **Overview** - Clear explanation of what the skill covers
- [ ] **Core Commands** - Essential commands with explanations
- [ ] **Scenarios** - At least 2 real-world use cases
- [ ] **Troubleshooting** - Common problems and solutions

### Recommended Elements

- [ ] **Prerequisites** - Required tools and setup
- [ ] **Best Practices** - Tips for effective usage
- [ ] **References** - Links to official docs and resources
- [ ] **Examples folder** - Additional detailed examples

### Quality Checklist

- [ ] Commands are tested and working
- [ ] No typos or grammatical errors
- [ ] Code blocks specify the language (bash, sql, yaml, etc.)
- [ ] Commands include helpful comments
- [ ] Dangerous commands have warnings
- [ ] Placeholders are clearly marked (e.g., `<your-value>`)

## Pull Request Process

### Before Submitting

1. Ensure your skill follows the template structure
2. Test all commands
3. Check for spelling and grammar
4. Verify links work

### PR Title Format

Use conventional commit format:

- `feat: add new-skill-name skill` - New skill
- `fix: correct command in skill-name` - Bug fix
- `docs: improve skill-name documentation` - Documentation only
- `refactor: reorganize skill-name structure` - Restructuring

### PR Description

Include:
- What skill/change you're adding
- Why it's useful
- Any special considerations
- Testing performed

### Review Process

1. Maintainers will review your PR
2. Address any feedback or requested changes
3. Once approved, your PR will be merged

## Style Guide

### Markdown Formatting

- Use ATX-style headers (`#`, `##`, `###`)
- Use fenced code blocks with language identifiers
- Use tables for structured data
- Keep lines under 120 characters when possible

### Code Blocks

Always specify the language:

````markdown
```bash
# Bash commands
ls -la
```

```sql
-- SQL queries
SELECT * FROM users;
```

```yaml
# YAML configuration
key: value
```
````

### Command Comments

Add helpful comments to commands:

```bash
# Good: Explains what the command does
find /var/log -name "*.log" -mtime +30 -delete  # Delete logs older than 30 days

# Bad: No explanation
find /var/log -name "*.log" -mtime +30 -delete
```

### Placeholders

Use angle brackets for user-provided values:

```bash
# Good
kubectl exec -it <pod-name> -- /bin/bash
docker run -p <host-port>:<container-port> <image>

# Bad
kubectl exec -it pod-name -- /bin/bash
docker run -p 8080:80 nginx
```

### Shell Scripts

For scripts in the `scripts/` folder:

```bash
#!/usr/bin/env bash
# Script: script-name.sh
# Description: What this script does
# Usage: ./script-name.sh [options]

set -euo pipefail

# Your script here
```

## Reporting Issues

### Bug Reports

When reporting a bug, include:

- Skill name and section
- The incorrect command or information
- Expected behavior
- Your environment (OS, tool version)

### Feature Requests

For new skill suggestions:

- Tool or topic name
- Why it would be useful
- Example commands or scenarios

### Creating an Issue

Use GitHub Issues with appropriate labels:

- `bug` - Something is incorrect
- `enhancement` - New skill or improvement
- `documentation` - Documentation improvements
- `question` - General questions

## Recognition

Contributors will be recognized in:

- Git commit history
- Skill file author field
- Project contributors list

## Questions?

If you have questions about contributing:

1. Check existing issues and discussions
2. Open a new issue with the `question` label
3. Be specific about what you need help with

---

Thank you for contributing to Terminal Skills! 🎉

Your contributions help the DevOps community work more effectively with Claude.
