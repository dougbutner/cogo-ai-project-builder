# COGO Command Index

One-line map of human commands to instruction files. COGO loads the matching file and runs its workflow.

| Command | Purpose | Instruction file |
| --- | --- | --- |
| `/bootstrap-project` | Greenfield: scaffold context and initial structure | `Human/bootstrap-project.md` |
| `/install-project` | Brownfield: align COGO with an existing repo | `Human/install-project.md` (Workflow A) |
| `/rewrite-project` | Migrate or rewrite to a different stack | `Human/install-project.md` (Workflow B) |
| `/handoff` | Summary for another human or chat session | `Human/handoff.md` |
| `/review` | Architecture or change review | `Human/review.md` |
| `/test-plan` | Testing strategy for a change or feature | `Human/test-plan.md` |
| `/release-notes` | User-facing or internal release notes | `Human/release-notes.md` |

Natural-language triggers (no required slash): production outage, incident response, urgent prod/staging debug → `Human/incident-or-debug.md` (see `COGO.md` Command Dispatch).

## Supporting docs (no slash command required)

| Topic | File |
| --- | --- |
| When to stop and ask | `Human/safety-and-confirmations.md` |
| Repo stack signals | `Human/stack-detection-checklist.md` |
| Incremental migration patterns | `Human/migration-playbook.md` |
| One-shot constraints for humans | `Human/project-constraints-template.md` |
| Production debugging | `Human/incident-or-debug.md` |
| Env vars and secrets scratchpad | `Human/example-env.md` |
| COGO bundle changes | `Human/CHANGELOG.md` |
