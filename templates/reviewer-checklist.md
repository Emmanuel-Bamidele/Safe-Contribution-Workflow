# Reviewer Checklist

Use this before approving a contribution.

## Scope

- [ ] The PR matches the requested contribution.
- [ ] The diff is focused.
- [ ] Unrelated files were not modified.
- [ ] Unrelated refactors were avoided.
- [ ] Formatting churn was avoided.
- [ ] Deleted code is clearly justified.

## Behavior

- [ ] Required behavior works.
- [ ] Existing behavior is preserved.
- [ ] Edge cases are handled.
- [ ] Failure cases are handled.

## Tests

- [ ] Tests were added or updated.
- [ ] Tests verify behavior, not just implementation.
- [ ] Bug fixes include regression tests where practical.
- [ ] Relevant checks were run.

## Security

- [ ] Authentication was not weakened.
- [ ] Authorization was not weakened.
- [ ] Input validation is appropriate.
- [ ] Sensitive data is not logged.
- [ ] No secrets are committed.

## Compatibility

- [ ] Public APIs were not broken silently.
- [ ] Shared types were changed only if necessary.
- [ ] Database changes are safe.
- [ ] Config or environment changes are documented.

## Team safety

- [ ] The contribution does not step on another team's work.
- [ ] Risk is documented.
- [ ] Rollback is possible.
