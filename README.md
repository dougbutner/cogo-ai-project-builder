# What is COGO?

You’re not duct-taping prompts into a chat and hoping the repo stays coherent. **[COGO](https://github.com/dougbutner/cogo-ai-project-builder)** is a drop-in “how we build” layer: planning, stack memory, safety rails, and human commands—so AI assistance reads like part of the project, not a one-off thread.

Everything lives under [`COGO/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO). Clone or copy this [repo](https://github.com/dougbutner/cogo-ai-project-builder), keep your app code wherever you want, and let the [`COGO/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO) folder carry the blueprint.

> 🦁  
> **Disclaimer:** This is an opinionated template. Tune [`Brain/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Brain) and [`Build/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Build) until they match *your* team—then treat them as source of truth.

## Getting started

1. Skim [`COGO/COGO.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/COGO.md)—that’s the operating contract for the assistant (principles, workflow, command routing).
2. Align stack choices in [`COGO/STACK.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/STACK.md) so decisions stop getting re-litigated every session.
3. Write what you’re actually doing in [`COGO/Current-Project.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Current-Project.md)—objective, focus, blockers, next steps.
4. For chat shortcuts (install, bootstrap, handoff, etc.), open [`COGO/Human/HUMAN-README.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/HUMAN-README.md) and the full map in [`COGO/Human/command-index.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/command-index.md).
5. Before a big greenfield build, walk [`COGO/Planning/cogo-initial-planning.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Planning/cogo-initial-planning.md)—skeleton → pseudocode approvals → code.

For the bundle changelog when you fork or copy [this repository](https://github.com/dougbutner/cogo-ai-project-builder), peek [`COGO/Human/CHANGELOG.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/CHANGELOG.md).

---

## Features (what each piece is for)

### Core doctrine — [`COGO/COGO.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/COGO.md)

**Perfect for:** Teaching any assistant how you want software built (simple > clever, vertical slices, no random refactors).

**Key strengths:**

- Single entrypoint for principles and default workflow  
- Hooks into [`Human/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Human) command routing so slash-style intents land on the right playbook  

**Best used for:** Every session reset—“read COGO first” beats re-explaining taste from scratch.

---

### Stack memory — [`COGO/STACK.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/STACK.md)

**Perfect for:** Freezing language, frameworks, hosting, and conventions so generated code stops drifting.

**Key strengths:**

- One place to resolve “what runtime is canonical?” fights  
- Pairs cleanly with [`Build/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Build) domain notes  

**Best used for:** Onboarding humans *and* models onto the same technical baseline.

---

### Live project context — [`COGO/Current-Project.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Current-Project.md)

**Perfect for:** Short-term truth—what we’re building *right now*, what’s blocked, what’s next.

**Key strengths:**

- Fast to edit; high signal per line  
- Feed it after `/install-project` or `/bootstrap-project` workflows in [`Human/install-project.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/install-project.md) / [`Human/bootstrap-project.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/bootstrap-project.md)  

**Best used for:** Keeping multi-chat work pointed at the same north star.

---

### Brain (long-term prefs) — [`COGO/Brain/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Brain)

**Perfect for:** Stuff that shouldn’t expire when a sprint ends—taste, anti-patterns, “never do this again.”

**Key strengths:**

- Durable memory separate from day-to-day [`Current-Project`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Current-Project.md) churn  
- Example: [`cogo-dopamine.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Brain/cogo-dopamine.md) for loves/hates/reinforcement  

**Best used for:** Calibration—what “good” feels like on *your* projects.

---

### Planning — [`COGO/Planning/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Planning)

**Perfect for:** Thinking before typing—especially greenfield, where structure mistakes are expensive.

**Key strengths:**

- [`cogo-initial-planning.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Planning/cogo-initial-planning.md): internal prep → **full skeleton** (approval) → **pseudocode overview** (approval) → code  
- Sibling docs for broader planning habits in the same [folder](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Planning)  

**Best used for:** First-time new-project mode; after that, lighter planning still fits [`COGO.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/COGO.md) defaults.

---

### Testing doctrine — [`COGO/Testing/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Testing)

**Perfect for:** Making “done” mean tested—not “compiles on my machine.”

**Key strengths:**

- Shared vocabulary for structure + expectations  
- Pairs with `/test-plan` in [`Human/test-plan.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/test-plan.md)  

**Best used for:** Anything that touches money, auth, data shapes, or deploy cadence.

---

### Build domains — [`COGO/Build/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Build)

**Perfect for:** Modular depth—frontend, backend, database, auth, infra—without one mega-doc.

**Key strengths:**

- Load only what’s relevant (matches the token-efficiency rule in [`COGO.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/COGO.md))  
- [`patterns/cogo-patterns.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Build/patterns/cogo-patterns.md), [`architecture/cogo-architecture.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Build/architecture/cogo-architecture.md), etc.  

**Best used for:** Deep dives after the skeleton is approved—don’t stuff everything into chat.

---

### Human commands & safety — [`COGO/Human/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Human)

**Perfect for:** Repeatable chat workflows—bootstrap, install brownfield, rewrite stack, handoff, review, release notes, incidents.

**Key strengths:**

- [`HUMAN-README.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/HUMAN-README.md) + [`command-index.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/command-index.md) as the routing table  
- [`safety-and-confirmations.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/safety-and-confirmations.md) before prod / secrets / destructive moves  
- [`example-env.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/COGO/Human/example-env.md) for **variable names only**—you copy real values into a proper `.env` or secret store  

**Best used for:** Turning fuzzy prompts into something the assistant can execute safely.

---

### Workspace placeholders — [`Templates/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Templates), [`Scripts/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Scripts), [`Projects/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO/Projects)

**Perfect for:** Housekeeping—snippets, automation, or multi-project notes that belong with COGO, not scattered in random folders.

**Key strengths:**

- Keeps the “meta” stuff out of application source  
- Easy to extend as your [repo](https://github.com/dougbutner/cogo-ai-project-builder) evolves  

**Best used for:** Anything you’d otherwise lose in Notion or Slack threads.

---

### Naming convention (quick ref)

- Repo root stays lean—[`README.md`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/README.md), [`LICENSE`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/LICENSE), et al.  
- Doctrine roots live in [`COGO/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO) (`COGO.md`, `STACK.md`, `Current-Project.md`, …).  
- Most nested docs follow `cogo-*.md` under their topic folder inside [`COGO/`](https://github.com/dougbutner/cogo-ai-project-builder/tree/main/COGO).

---

## License

This [repository](https://github.com/dougbutner/cogo-ai-project-builder) stays under the included [`LICENSE`](https://github.com/dougbutner/cogo-ai-project-builder/blob/main/LICENSE).
