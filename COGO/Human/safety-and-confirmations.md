# Safety and Confirmations

COGO pauses for explicit human confirmation before proceeding when any of the following apply.

## Always confirm first

- Irreversible or destructive actions: `git reset --hard`, force-push, mass delete, dropping databases or tables.
- Writing or rotating **production** secrets, API keys, or signing keys.
- Changing **authentication**, **authorization**, **billing**, or **PII** handling without a stated requirement.
- Running migrations against **production** or shared staging without confirmation of target and backup.
- Modifying **legal**, **compliance**, or **security** posture (CORS, CSP, encryption, retention).

## Prefer confirmation

- Adding new dependencies with native binaries or broad filesystem/network access.
- Broad refactors that touch many unrelated files in one step.
- Disabling tests, linters, or type checks to "make it pass."

## Secrets and env files

- Never paste real secret values into chat unless the human explicitly asks and understands the risk.
- Use `Human/example-env.md` as a **documentation scratchpad** only. Real values belong in `.env` (gitignored), the host's secret store, or CI secrets—not committed.

## If unsure

- Ask one clarifying question, then continue with the smallest safe change.
