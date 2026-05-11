# Compatibility Checklist

Use this when the contribution touches shared behavior.

## Public API compatibility

Check whether the contribution changes:

- HTTP routes
- Request shape
- Response shape
- Error codes
- Pagination
- Sorting
- Filtering
- Webhook payloads
- SDK behavior
- CLI behavior

If yes, document the impact.

## Internal compatibility

Check whether the contribution changes:

- Shared types
- Shared utilities
- Database models
- Event names
- Queue payloads
- Config names
- Environment variables
- Feature flags

## User compatibility

Check whether the contribution changes:

- User-visible behavior
- UI text
- Form behavior
- Permissions
- Notifications
- Exports
- Reports
- Defaults

## Safe compatibility rule

Do not break compatibility unless the task explicitly requires it.

If compatibility must break, explain:

- What breaks
- Why it is necessary
- Who is affected
- Migration path
- Rollback plan
