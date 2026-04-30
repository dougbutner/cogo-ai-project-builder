# COGO Human Commands

Use these commands in chat when working with COGO inside any project.

**Full index:** `COGO/Human/command-index.md`

## How Commands Work

When a command is used (exact or close phrasing), COGO should:

1. Detect the command intent.
2. Load `Human/safety-and-confirmations.md` before destructive, prod, or secret-handling work.
3. Load the mapped instruction file.
4. Execute the workflow in that file step by step.
5. Ask only for missing required inputs.

## Commands

### `/bootstrap-project`

Purpose: Greenfield—scaffold context and minimal runnable slice.

- Trigger phrases: `/bootstrap-project`, "new empty project", "greenfield setup"
- Action: Open `COGO/Human/bootstrap-project.md` and run its workflow.

### `/install-project`

Purpose: Install and align COGO into an existing project.

- Trigger phrases:
  - `/install-project`
  - "install cogo in this project"
  - "set up cogo for this repo"
- Action:
  - Open `COGO/Human/install-project.md`
  - Run Workflow A (Install Into Existing Project)

### `/rewrite-project`

Purpose: Rewrite an existing project to a different stack.

- Trigger phrases:
  - `/rewrite-project`
  - "rewrite this project to [target-stack]"
  - "migrate this project from [source-stack] to [target-stack]"
- Action:
  - Open `COGO/Human/install-project.md`
  - Run Workflow B (Rewrite Project To Different Stack)

### `/handoff`

Purpose: Compact summary for another person or chat session.

- Trigger phrases: `/handoff`, "summarize for handoff", "what should the next session know"
- Action: Open `COGO/Human/handoff.md`

### `/review`

Purpose: Architecture or change review.

- Trigger phrases: `/review`, "review this PR", "review this architecture"
- Action: Open `COGO/Human/review.md`

### `/test-plan`

Purpose: Testing strategy for a change or feature.

- Trigger phrases: `/test-plan`, "what tests do we need"
- Action: Open `COGO/Human/test-plan.md`

### `/release-notes`

Purpose: User-facing or internal release notes.

- Trigger phrases: `/release-notes`, "changelog for this release"
- Action: Open `COGO/Human/release-notes.md`

## Supporting docs (reference)

- Constraints template: `Human/project-constraints-template.md`
- Stack detection: `Human/stack-detection-checklist.md`
- Migrations: `Human/migration-playbook.md`
- Env scratchpad (names only—copy to real `.env`): `Human/example-env.md`
- Production debugging: `Human/incident-or-debug.md`
- Bundle history: `Human/CHANGELOG.md`

## Notes For Humans

- Keep command prompts short and explicit.
- Include constraints up front (deadline, hosting, database, auth, budget)—or fill `Human/project-constraints-template.md`.
- For rewrites, always name the target stack clearly.
