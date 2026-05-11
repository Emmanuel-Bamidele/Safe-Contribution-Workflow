# Risk Checklist

Before finishing, review contribution risk.

## Scope risk

- [ ] Did the change stay within the requested contribution?
- [ ] Were unrelated files avoided?
- [ ] Were unrelated refactors avoided?
- [ ] Was formatting churn avoided?

## Behavior risk

- [ ] Existing behavior is preserved.
- [ ] Edge cases are handled.
- [ ] Failure cases are handled.
- [ ] User-visible behavior changes are documented.

## Team risk

- [ ] The diff is reviewable.
- [ ] Shared files were changed only when necessary.
- [ ] Public contracts were not changed silently.
- [ ] Other teams' areas were not modified unnecessarily.

## Security risk

- [ ] Authentication is not weakened.
- [ ] Authorization is preserved.
- [ ] Inputs are validated.
- [ ] Sensitive data is not logged.
- [ ] Secrets are not committed.

## Data risk

- [ ] Data is not deleted unexpectedly.
- [ ] Migrations are safe.
- [ ] Transactions are used where needed.
- [ ] Existing data remains compatible.

## Operational risk

- [ ] Relevant checks were run.
- [ ] Failures were reported honestly.
- [ ] Rollback is possible.
- [ ] Risk is documented.
