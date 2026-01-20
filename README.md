# Project Docs - Claude Code Skill

> Software development project documentation management and progress tracking skill for Claude Code

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-orange)](https://claude.com/claude-code)
[![Markdown Lint](https://github.com/lorissun2025/project-docs/actions/workflows/markdown-lint.yml/badge.svg)](https://github.com/lorissun2025/project-docs/actions/workflows/markdown-lint.yml)
[![Spell Check](https://github.com/lorissun2025/project-docs/actions/workflows/spell-check.yml/badge.svg)](https://github.com/lorissun2025/project-docs/actions/workflows/spell-check.yml)

## Overview

**Project Docs** is a skill for Claude Code that helps manage documentation for software development projects. It ensures all required documents exist, are properly structured, and kept up-to-date. It also tracks progress via detailed roadmaps and helps teams maintain context across development cycles.

## Features

- **Project Initialization**: Create a complete documentation foundation for new software projects
- **Progress Tracking**: Maintain and update project roadmaps as work progresses
- **Status Summary**: Get concise summaries of current project state
- **Resume Context**: Quickly get back into the flow after time away
- **Document Validation**: Ensure all required documentation exists and is complete

## Required Documents

This skill helps you create and maintain the following project documents:

- **MRD** (Market Requirements Document) - Market analysis, TAM/SAM/SOM, competitive landscape, business model, pricing strategy
- **PRD** (Product Requirements Document) - Feature definitions, user stories, acceptance criteria, success metrics
- **Technical Plan** - Architecture, tech stack, database design, API specifications, deployment strategy
- **Project Roadmap** - Detailed task breakdown with progress tracking (task IDs, status, owners, dates)
- **Development Checklist** - Setup tasks, environment configuration, tool installation

## Installation

1. Clone this repository
2. Copy the `project-docs` folder to your Claude Code skills directory:
   ```bash
   cp -r project-docs ~/.claude/skills/
   ```
3. Restart Claude Code
4. The skill will be automatically loaded

## Usage

### Quick Start Commands

```bash
# First time setup
"Initialize project docs for [project name]"

# Update progress
"Update roadmap, I just finished [feature/task]"

# Check status
"What's the current progress and what should I work on next?"

# Resume work
"I haven't worked on this project in [time period], catch me up"
```

### Example Workflow

```
User: "Initialize project docs for my AI startup called VibeAILife"
→ Checks docs/plans/ directory
→ Identifies missing documents
→ Creates each document from templates
→ Generates initial roadmap with Phase 1 breakdown
→ Returns summary and next steps
```

## Document Templates

The skill includes the following templates:

| Template | Description |
|----------|-------------|
| `MRD-TEMPLATE.md` | Market Requirements Document structure |
| `PRD-TEMPLATE.md` | Product Requirements Document structure |
| `TECHNICAL-PLAN-TEMPLATE.md` | Technical Plan structure |
| `ROADMAP-TEMPLATE.md` | Project Roadmap structure |
| `CHECKLIST-TEMPLATE.md` | Development Checklist structure |

## Roadmap Structure

The `PROJECT-ROADMAP.md` file uses the following structure:

```markdown
## Phase N: [Name] (Week X-Y)
### Module Name
| TaskID | Task | Status | Owner | Date | Notes |
|--------|------|--------|-------|------|-------|
| P1-1-1 | Description | ✅ | - | 2026-01-20 | |
```

**Task ID Format**: `P{Phase}-{Module}-{Task}` (e.g., `P1-7-3` = Phase 1, Module 7, Task 3)

**Status Codes**:
- ✅ **Completed** - Task done and verified
- 🚧 **In Progress** - Currently being worked on
- ⏳ **Pending** - Planned but not started
- ❌ **Cancelled** - No longer needed
- ⚠️ **Blocked** - Has dependencies or issues

## Expected Directory Structure

```
project-root/
├── docs/
│   └── plans/
│       ├── PROJECT-ROADMAP.md       # Progress tracking (required)
│       ├── MRD.md                   # Market analysis (required)
│       ├── PRD.md                   # Product requirements (required)
│       ├── TECHNICAL-PLAN.md        # Technical specs (required)
│       └── DEV-CHECKLIST.md         # Setup tasks (required)
└── [project code]
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

- Report bugs via [Issues](https://github.com/lorissun2025/project-docs/issues/new?template=bug_report.md)
- Request features via [Issues](https://github.com/lorissun2025/project-docs/issues/new?template=feature_request.md)
- Submit pull requests with your improvements

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built for [Claude Code](https://claude.com/claude-code)
- Inspired by industry-standard product development practices

## Author

Created by [sunsensen](https://github.com/sunsensen)

---

**Note**: This skill is designed to work with Claude Code. Make sure you have the latest version installed.
