# No Unrelated Changes

A safe contribution should not damage other people's work.

## Do not change unrelated files

Do not modify files unless they are required for the contribution.

## Do not reformat unrelated files

Avoid formatting churn.

Formatting unrelated files creates noisy diffs and merge conflicts.

## Do not delete unrelated code

Do not delete code just because it looks unused.

If it appears unused, document it as follow-up.

## Do not refactor unrelated modules

Refactoring should only happen when directly required for the contribution.

## Do not change shared contracts casually

Be careful with:

- Public APIs
- Shared types
- Database schemas
- Event payloads
- CLI options
- Environment variables
- Config formats
- User-visible behavior

## Do not fix unrelated bugs

If you find another bug, document it separately.

Only fix it if it blocks the requested contribution.
