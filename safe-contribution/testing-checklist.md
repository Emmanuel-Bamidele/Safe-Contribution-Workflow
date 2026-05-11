# Testing Checklist

Use this checklist before completing the contribution.

## Required test thinking

Ask:

- What behavior changed?
- What behavior must stay the same?
- What is the normal case?
- What is the edge case?
- What is the failure case?
- What is the unauthorized case, if relevant?
- What regression could happen later?

## Add or update tests for

- Bug fixes
- New features
- Validation changes
- Authorization behavior
- API behavior
- Database writes
- External integrations
- UI interactions
- Error handling
- Migration behavior

## Good tests

Good tests verify behavior.

They should answer:

```text
Does the contribution work for the user or system?
```

## Avoid weak tests

Avoid tests that:

- Only assert mocks
- Mock the function being tested
- Have no meaningful assertions
- Depend on test order
- Depend on local hidden state
- Use production services
- Use production credentials
- Only check that something renders without behavior

## Regression rule

If the contribution fixes a bug, add a regression test unless impossible.

If impossible, explain why.

## Commands

Run relevant tests.

Examples:

```bash
npm test
npm run test
npm run typecheck
npm run lint
npm run build
pytest
go test ./...
cargo test
```

Report what was run and what passed or failed.
