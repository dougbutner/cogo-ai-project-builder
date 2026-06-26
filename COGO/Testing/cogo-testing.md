# Testing

Defaults: `STACK.md` (**Vitest** + **Playwright** critical paths). Deterministic, isolated; behavior over implementation; reusable fixtures; mock externals responsibly; fight flakiness.

**Layout:** top-level `/tests` with `unit/`, `integration/`, `e2e/`, `fixtures/`, `mocks/` — prefer outside app dirs unless asked.

**Flow:** implement → tests → edge cases → regression guard.
