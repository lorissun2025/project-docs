---
name: project-docs
description: "Software development project documentation management and progress tracking. Use when: (1) Initializing a new software project and need to create all required documentation (MRD, PRD, Technical Plan, Roadmap), (2) Updating project roadmap after completing tasks, (3) Getting a summary of current project progress, (4) Resuming work on a project after a break and need to understand what's next, (5) Checking if required project documents exist and are complete"
---

# Project Docs

## Overview

Manages documentation for software development projects, ensuring all required documents exist, are properly structured, and kept up-to-date. Tracks progress via detailed roadmaps and helps teams maintain context across development cycles.

## Quick Start

**First time setup**: `Initialize project docs for [project name]`
**Update progress**: `Update roadmap, I just finished [feature/task]`
**Check status**: `What's the current progress and what should I work on next?`
**Resume work**: `I haven't worked on this project in [time period], catch me up`

---

## Core Capabilities

### 1. Project Initialization

Create a complete documentation foundation for a new software project.

**Required Documents**:
- **MRD** (Market Requirements Document) - Market analysis, TAM/SAM/SOM, competitive landscape, business model, pricing strategy
- **PRD** (Product Requirements Document) - Feature definitions, user stories, acceptance criteria, success metrics
- **Technical Plan** - Architecture, tech stack, database design, API specifications, deployment strategy
- **Project Roadmap** - Detailed task breakdown with progress tracking (task IDs, status, owners, dates)
- **Development Checklist** - Setup tasks, environment configuration, tool installation

**Workflow**:
1. Check if `docs/plans/` directory exists
2. Scan for existing documents
3. Create templates for missing documents
4. Generate initial roadmap with Phase 1 tasks
5. Create checklist for immediate setup tasks

**Example trigger**: "Initialize project docs for my AI startup called VibeAILife"

### 2. Progress Tracking

Maintain and update the project roadmap as work progresses.

**Workflow**:
1. Read `docs/plans/PROJECT-ROADMAP.md`
2. Identify completed task(s) from user input
3. Update task status from ⏳ → ✅
4. Update progress percentages
5. Add entry to update log
6. Recalculate next recommended tasks

**Status Codes**:
- ✅ **Completed** - Task done and verified
- 🚧 **In Progress** - Currently being worked on
- ⏳ **Pending** - Planned but not started
- ❌ **Cancelled** - No longer needed
- ⚠️ **Blocked** - Has dependencies or issues

**Example triggers**:
- "Update roadmap, I just finished the authentication system"
- "Mark P1-7-1 through P1-7-5 as complete"
- "Update all UI component tasks to done"

### 3. Status Summary

Provide concise summaries of current project state.

**Outputs**:
- **Overall Progress** - Percentage complete, visual progress bar
- **Phase Status** - Which phases are done/in progress/pending
- **Current Focus** - What should be worked on next
- **Blocking Issues** - Any tasks marked with ⚠️
- **Recent Updates** - Last 3-5 roadmap updates

**Example triggers**:
- "What's the current progress?"
- "Show me project status summary"
- "Give me a quick update on where we are"

### 4. Resume Context

Help developers quickly get back into the flow after time away.

**Workflow**:
1. Read roadmap and check update log
2. Identify last worked-on tasks
3. Show current phase and immediate next tasks
4. Highlight any new blocking issues
5. Provide context on what's changed since last update

**Example triggers**:
- "I haven't worked on this in 2 weeks, catch me up"
- "What was I working on last?"
- "Where did we leave off?"

### 5. Document Validation

Ensure all required documentation exists and is complete.

**Checks**:
- Document existence in `docs/plans/`
- Required sections present (based on templates)
- No TODO placeholders remaining
- Version numbers and dates current

**Example triggers**:
- "Check if all project docs are complete"
- "Validate our documentation"
- "Are we missing any required documents?"

---

## Document Templates

Required document structures are in [assets/templates/](assets/templates/). Reference these when creating missing documents:

- `MRD-TEMPLATE.md` - Market Requirements Document structure
- `PRD-TEMPLATE.md` - Product Requirements Document structure
- `TECHNICAL-PLAN-TEMPLATE.md` - Technical Plan structure
- `ROADMAP-TEMPLATE.md` - Project Roadmap structure
- `CHECKLIST-TEMPLATE.md` - Development Checklist structure

---

## Roadmap Structure

The `PROJECT-ROADMAP.md` file has specific structure that must be maintained:

```markdown
## Phase N: [Name] (Week X-Y)
### Module Name
| TaskID | Task | Status | Owner | Date | Notes |
|--------|------|--------|-------|------|-------|
| P1-1-1 | Description | ✅ | - | 2026-01-20 | |
```

**Task ID Format**: `P{Phase}-{Module}-{Task}`
- Example: `P1-7-3` = Phase 1, Module 7, Task 3

**Progress Calculation**:
```javascript
Phase Progress = (Completed + In Progress) / Total Phase Tasks × 100%
Overall Progress = Σ(Phase Progress × Phase Weight) / Total Weight
```

---

## Common Workflows

### Creating a New Project

```
User: "Initialize project docs for my SaaS app"
→ Check docs/plans/ exists
→ Identify missing documents (typically all)
→ Create each document from templates
→ Generate initial roadmap with Phase 1 breakdown
→ Return summary and next steps
```

### After Completing Work

```
User: "Update roadmap, finished the login UI"
→ Read PROJECT-ROADMAP.md
→ Find "login UI" or related task
→ Update status to ✅, set completion date
→ Recalculate progress percentages
→ Add update log entry
→ Return updated summary
```

### Resuming After Break

```
User: "I haven't worked on this in a month, catch me up"
→ Check update log timestamp
→ Show last update date
→ Display current phase progress
→ List next 3-5 recommended tasks
→ Flag any new blocking issues
```

---

## Directory Structure

Expected project structure:
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

---

## Tips

- **Be Specific**: When updating roadmap, specify exact task names or IDs
- **Use Task IDs**: `P1-7-3` is clearer than "that AI task"
- **Keep Updates Small**: Update roadmap frequently, after each task or small feature
- **Check Dependencies**: Mark tasks as ⚠️ Blocked if waiting on other work
- **Version Everything**: Include dates and version numbers in all documents
