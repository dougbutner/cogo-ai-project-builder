# Test Structure

Always create a top-level `/tests` directory.

## Structure

/tests
  /unit
  /integration
  /e2e
  /fixtures
  /mocks

## Rules

- Keep tests outside implementation folders unless explicitly requested.
- Centralize shared mocks and fixtures.
- Name tests clearly and consistently.
- Keep test architecture clean and scalable.

## Organization

- Unit tests validate isolated logic.
- Integration tests validate system interactions.
- E2E tests validate real user workflows.
