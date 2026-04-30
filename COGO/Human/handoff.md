# Handoff

Use when command intent matches `/handoff` or "summarize for the next person/session."

## Workflow

1. **Goal**: One paragraph on what the project or active task is trying to achieve.
2. **Current state**: What works, what is in progress, branch names if relevant.
3. **Decisions**: Bullet list with dates or PR references if known.
4. **Environment**: What must be installed; point to `Human/example-env.md` for variable **names** only (no secret values in chat unless human requests).
5. **Blockers**: Explicit unknowns or dependencies on others.
6. **Next steps**: Three concrete tasks in priority order.

Keep the total output skimmable (under roughly one screen when possible).
