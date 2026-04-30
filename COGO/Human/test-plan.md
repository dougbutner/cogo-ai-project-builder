# Test Plan

Use when command intent matches `/test-plan` or "what should we test for this?"

## Workflow

1. **Change summary**: What behavior changed or was added.
2. **Risk areas**: Auth, money, data migration, concurrency, external APIs.
3. **Test levels**:
   - **Unit**: fastest feedback for pure logic.
   - **Integration**: DB, queue, HTTP boundaries with real or test containers where valuable.
   - **E2E**: critical user journeys only (keep count small).
4. **Data fixtures**: Seed or factories needed; anonymized production-like cases if applicable.
5. **Regression**: Existing tests to run; flaky-test note if any.
6. **Exit criteria**: What must pass before merge or deploy.

Offer a minimal plan first; expand only if the human asks.
