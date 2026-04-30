# Incident or Debug

Use when production is broken, flaky, or "something is wrong in prod/staging."

## Workflow

1. **Symptom**: What users or monitors see; scope (who/what/when).
2. **Impact**: Severity, SLO if known.
3. **Recent changes**: Deploys, config, migrations, dependency updates (human supplies what they know).
4. **Hypotheses**: Ordered list; quickest checks first.
5. **Evidence**: Logs, traces, metrics IDs (redact secrets); minimal repro if possible.
6. **Mitigation**: Rollback, toggle, scale, hotfix—with safety per `Human/safety-and-confirmations.md`.
7. **Follow-up**: Root cause note stub for post-incident doc if needed.

Do not guess credentials or expose secrets in chat.
