# Install or Rewrite Project

This file defines operational workflows for COGO when used inside an existing codebase.

## Related docs

- `Human/safety-and-confirmations.md` — when to confirm before acting.
- `Human/stack-detection-checklist.md` — consistent repo/stack inference.
- `Human/migration-playbook.md` — patterns for Workflow B.
- `Human/project-constraints-template.md` — optional human-filled constraints.
- `Human/example-env.md` — document env **names** only; humans copy to real `.env` / secrets store.

## Shared Rules

- Never modify unrelated files.
- Detect existing stack before proposing changes (use `Human/stack-detection-checklist.md`).
- Prefer incremental migrations over big-bang rewrites; see `Human/migration-playbook.md` for Workflow B.
- Keep a rollback path for risky changes.
- Confirm assumptions when confidence is low.

## Workflow A: Install Into Existing Project

Use when command intent matches `/install-project`.

### 1) Read Current Repository

- Inspect top-level files and folders.
- Detect package managers, frameworks, runtime, and infra signals.
- Identify language(s), frontend, backend, database, auth, and deployment setup.

### 2) Fill Project Profile

Create and fill these sections in `COGO/Current-Project.md`:

- Objective
- Current Focus
- Recent Decisions
- Blockers
- Next Steps

Also update any relevant `COGO/Build/*` files based on detected stack.

Record discovered integration env var **names** in `Human/example-env.md` (placeholders only—no real secrets).

### 3) Install COGO Operating Context

- Ensure required COGO files exist.
- Link the detected architecture to COGO documents.
- Record known constraints and team preferences.

### 4) Output Installation Summary

Return:

- Detected stack summary
- What was initialized/updated
- Recommended first implementation task

## Workflow B: Rewrite Project To Different Stack

Use when command intent matches `/rewrite-project`.

### Required Inputs

- Source stack (if unclear, detect it)
- Target stack (must be explicit)
- Migration constraints (timeline, downtime tolerance, compatibility requirements)

### 1) Analyze Current System

- Map existing architecture and key dependencies.
- Identify migration-critical areas (auth, data model, billing, background jobs, APIs).
- Flag high-risk components.

### 2) Generate Rewrite Plan

Apply patterns from `Human/migration-playbook.md` where relevant.

Produce:

- Target architecture
- Component mapping (old -> new)
- Phased migration steps
- Data migration strategy
- Testing and rollback strategy

### 3) Execute Incremental Rewrite

- Migrate one vertical slice at a time.
- Keep app runnable at every major checkpoint.
- Validate each phase with tests before proceeding.

### 4) Output Rewrite Status

Return:

- Completed phases
- Remaining phases
- Risks and blockers
- Next safe step

## Command Routing Contract

If a user message includes command intent:

- `/install-project` -> run Workflow A
- `/rewrite-project` -> run Workflow B

If intent is ambiguous, ask one clarifying question and then continue.
