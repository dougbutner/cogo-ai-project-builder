# Learn

Build a project-specific COGO LITE bundle in **`JR/`** at the repo root. JR is this project's frozen Cogo config—parameters, memory, and prompts tuned to what was learned while shipping here.

Trigger: `/learn`, "build JR", "export cogo lite for this project", or end of a major milestone when the human wants the bundle updated.

## Inputs

Read before writing:

- `COGO LITE/Parameters.md` (filled fields + State)
- `COGO LITE/Brain.md` (pipe lines)
- Repo stack signals (package manifests, configs, folder layout)
- Durable decisions from the current session if not yet in Brain

## Output — `JR/` layout

Create or update these files. Copy structure from `COGO LITE/`; customize content for **this project only**.

```text
JR/
  Parameters.md   — all fields filled; State current
  Setup.md        — same workflow as COGO LITE/Setup.md; project defaults inlined (no generic stack)
  Planning.md     — same as COGO LITE/Planning.md unless project needs a slimmer gate
  Brain.md        — merge COGO LITE/Brain.md + new project pipe lines
```

Do not duplicate secrets. Env var **names** only.

## Steps

1. **Harvest** — Pull language, purpose, I/O, libs, style, complexity, error handling, comments, and performance from repo reality and `Parameters.md`. Resolve conflicts in favor of what the repo actually uses.
2. **Fill `JR/Parameters.md`** — Every parameter field populated. State reflects current objective, focus, blockers, next.
3. **Tune `JR/Setup.md`** — Replace generic defaults with this project's stack, paths, run/test commands, and deploy target. Keep safety and dispatch; point dispatch at `JR/` files.
4. **Sync `JR/Brain.md`** — Copy existing lines; append new `d`/`p` lines from the project. Dedupe by `id`.
5. **Copy `JR/Planning.md`** — From `COGO LITE/Planning.md` unless the human asked for a shorter planning gate.
6. **Out** — List files written; one paragraph on what changed vs last JR build; flag anything the human should confirm.

## Rules

- JR is the portable Cogo Lite for **this repo**—another agent or session loads `JR/Setup.md` first, not the template `COGO LITE/`.
- Re-run Learn when stack, architecture, or durable prefs change materially.
- No unrelated edits outside `JR/` unless the human asked.
