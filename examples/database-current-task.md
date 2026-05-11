# Current Contribution: Database Example

## Goal

Add an optional `display_name` field to user profiles.

## Why this contribution is needed

Users need a public display name separate from their legal or account name.

## Scope

### Allowed changes

- User profile schema/model
- Safe migration for optional display name
- Profile API validation
- Profile settings UI if applicable
- Tests for display name behavior

### Not allowed

- Do not rename existing user name fields.
- Do not migrate existing names into display names automatically.
- Do not change authentication.
- Do not change unrelated profile fields.

## Required behavior

- Display name is optional.
- Display name has a maximum length.
- Existing users remain valid.
- Existing profile behavior remains unchanged when display name is empty.

## Existing behavior to preserve

- Existing user account creation still works.
- Existing profile reads still work.
- Existing profile updates still work.

## Required tests

- User can save display name.
- Empty display name is allowed.
- Overlong display name is rejected.
- Existing users without display name still load.

## Checks to run

```bash
npm test
npm run typecheck
npm run build
```

## Risks to consider

- Migration must be safe for existing users.
- Field should not be required initially.
