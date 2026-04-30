# Migration Playbook

Reference for `/rewrite-project` and large stack moves. Prefer incremental, reversible steps.

## Patterns

- **Strangler fig**: New stack owns new routes or modules; old stack shrinks behind a boundary (proxy, API gateway, or path prefix).
- **Parallel run**: Dual-write or shadow-read between old and new data paths; compare outputs before cutover.
- **Feature flags**: Toggle behavior per tenant or percentage; roll back without redeploy when possible.
- **Data migration**: Backfill in batches; verify counts and checksums; plan downtime or read-only window if required.

## Checkpoints

Each phase should end with:

- Tests passing (or explicitly scoped exceptions documented).
- Rollback step documented (revert flag, migration down, or DNS/route rollback).

## Pair with

- `Human/safety-and-confirmations.md` for production cuts.
- `Human/stack-detection-checklist.md` for accurate source mapping.
