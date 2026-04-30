# Review

Use when command intent matches `/review` or "review this change/architecture."

## Inputs

- Scope: full repo, subsystem, or specific PR/diff (human points to files or describes the change).

## Workflow

1. **Intent**: What problem does this solve?
2. **Architecture fit**: Alignment with existing patterns; coupling and boundaries.
3. **Correctness**: Edge cases, error handling, idempotency where relevant.
4. **Security**: Authz leaks, injection, secrets in code, unsafe defaults.
5. **Performance**: Hot paths, N+1 queries, unnecessary work.
6. **Maintainability**: Naming, file size, testability.
7. **Verdict**: Ship / ship with fixes / rework—with prioritized actionable items.

Stay proportional: small change gets a short review.
