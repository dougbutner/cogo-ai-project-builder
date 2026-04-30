# Bootstrap Project (Greenfield)

Use when command intent matches `/bootstrap-project` or equivalent ("new project", "greenfield", "empty repo").

## Prerequisites

- Human states objective and target stack (or accepts COGO's proposed stack).
- Load `Human/safety-and-confirmations.md` before scaffolding.

## Workflow

### 1) Clarify scope

- Product goal, MVP boundaries, and non-goals.
- Hosting target (local only, VPS, serverless, managed platform).
- Team preferences from `Brain/` or `Human/project-constraints-template.md` if present.

### 2) Initialize project profile

Fill `COGO/Current-Project.md`: Objective, Current Focus, Recent Decisions, Blockers, Next Steps.

### 3) Align COGO Build docs

Update or create the relevant `COGO/Build/*` notes for the chosen stack (frontend, backend, database, auth, infra as applicable).

### 4) Scaffold repository (minimal vertical slice)

- Create the smallest runnable skeleton (app entry, one health or hello path, config pattern).
- Add `.gitignore` patterns for env files and build artifacts.
- Do **not** commit real secrets; populate `Human/example-env.md` with **placeholder names** only.

### 5) Quality baseline

- Document how to run, test, and lint (even if commands are stubbed until tools exist).
- Suggest the first three implementation tasks in priority order.

### 6) Output

- Stack summary
- Files created or touched
- Next steps and open decisions

## Command routing

- `/bootstrap-project` -> run this workflow end to end.
