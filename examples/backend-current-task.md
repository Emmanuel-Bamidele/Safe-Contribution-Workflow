# Current Contribution: Backend Example

## Goal

Add validation for the `status` query parameter on the orders endpoint.

## Why this contribution is needed

Invalid status values currently reach the service layer and cause inconsistent behavior.

## Scope

### Allowed changes

- Orders endpoint query validation
- Error response for invalid status
- Tests for valid and invalid status values

### Not allowed

- Do not rewrite the orders service.
- Do not change order status names.
- Do not modify unrelated endpoints.
- Do not change authorization behavior.

## Required behavior

- Valid statuses are accepted.
- Invalid statuses return a validation error.
- Existing authorization behavior remains unchanged.

## Existing behavior to preserve

- Existing order listing still works.
- Existing filters still work.
- Existing response shape remains unchanged except validation error for invalid input.

## Required tests

- Valid status returns expected response.
- Invalid status returns validation error.
- Unauthorized request still fails as before.

## Checks to run

```bash
npm test
npm run typecheck
```

## Risks to consider

- Error format should match existing API errors.
