# Human commands

Two bundles. Pick one per repo (or use both: full COGO for domain docs, LITE for daily prompts).

## COGO LITE (five files)

**Entry:** [`COGO LITE/Setup.md`](COGO%20LITE/Setup.md) · **Params:** [`COGO LITE/Parameters.md`](COGO%20LITE/Parameters.md)

| Command | Hotwords | Workflow |
| --- | --- | --- |
| `/setup` | new project, greenfield, empty repo | `Setup.md` — greenfield |
| `/install` | install cogo lite, set up for this repo | `Setup.md` — brownfield |
| `/rewrite` | rewrite to [stack], migrate from [a] to [b] | `Setup.md` — rewrite |
| `/plan` | plan, architecture, milestones | `Planning.md` |
| `/remember` | preference, decision, record | `Brain.md` |
| `/learn` | build JR, export cogo lite for this project | `Learn.md` |

Fill constraints once in `Parameters.md`. Short explicit prompts.

## COGO (full)

**Routing table:** [`COGO/Human/command-index.md`](COGO/Human/command-index.md)

| Command | Hotwords | Workflow |
| --- | --- | --- |
| `/bootstrap-project` | set up project, create template, cogo, setup, new project | [`bootstrap-project.md`](COGO/Human/bootstrap-project.md) |
| `/install-project` | invite cogo, load cogo, set up cogo for this repo | [`install-project.md`](COGO/Human/install-project.md) — **Workflow A** |
| `/rewrite-project` | rewrite to [stack], migrate from [a] to [b] | [`install-project.md`](COGO/Human/install-project.md) — **Workflow B** |
| `/handoff` | handoff, prepare the repo for a new project | [`handoff.md`](COGO/Human/handoff.md) |
| `/review` | review PR, review architecture | [`review.md`](COGO/Human/review.md) |
| `/test-plan` | what tests, test plan | [`test-plan.md`](COGO/Human/test-plan.md) |
| `/release-notes` | changelog, release notes | [`release-notes.md`](COGO/Human/release-notes.md) |

**Incidents** — *prod down*, *outage*, *incident*, *staging broken*: [`incident-or-debug.md`](COGO/Human/incident-or-debug.md)

### COGO supporting links

- [`project-constraints-template.md`](COGO/Human/project-constraints-template.md)
- [`Current-Project.md`](COGO/Current-Project.md)
- [`STACK.md`](COGO/STACK.md)
- [`example-env.md`](COGO/Human/example-env.md)
- [`CHANGELOG.md`](COGO/Human/CHANGELOG.md)

## Notes

- LITE: directive prompts, low vector; params live in `Parameters.md`.
- Full: constraints in template or Current Project; rewrites need **target stack** stated.
