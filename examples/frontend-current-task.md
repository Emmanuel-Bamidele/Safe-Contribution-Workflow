# Current Contribution: Frontend Example

## Goal

Add loading and error states to the project members table.

## Why this contribution is needed

The table currently appears empty while data is loading, confusing users.

## Scope

### Allowed changes

- Project members table component
- Related loading/error UI
- Tests for table states

### Not allowed

- Do not redesign the project page.
- Do not change member permissions.
- Do not change API data fetching behavior unless required.
- Do not modify unrelated tables.

## Required behavior

- Loading state appears while members are loading.
- Error state appears if loading fails.
- Empty state still appears when there are no members.
- Existing member list behavior remains unchanged.

## Existing behavior to preserve

- Existing table columns remain unchanged.
- Existing actions remain unchanged.
- Existing permissions remain unchanged.

## Required tests

- Shows loading state.
- Shows error state.
- Shows empty state.
- Shows members when data loads.

## Checks to run

```bash
npm test
npm run lint
```

## Risks to consider

- Do not hide real empty state behind loading state.
