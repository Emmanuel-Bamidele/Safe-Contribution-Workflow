# Current Contribution: Bounded Refactor Example

## Goal

Refactor only the user settings validation logic into a reusable helper.

## Why this contribution is needed

The same validation is duplicated in two settings files and has caused inconsistent behavior.

## Scope

### Allowed changes

- User settings validation logic
- Existing settings tests
- New helper file if needed

### Not allowed

- Do not refactor all settings pages.
- Do not change validation rules.
- Do not change API behavior.
- Do not modify unrelated user profile logic.

## Required behavior

- Existing validation behavior remains the same.
- Duplicate validation is consolidated.
- Existing tests pass.

## Existing behavior to preserve

- Same error messages.
- Same accepted values.
- Same rejected values.

## Required tests

- Existing validation tests still pass.
- Add tests for helper if missing.

## Checks to run

```bash
npm test
npm run typecheck
```

## Risks to consider

- This is a refactor; behavior should not change.
