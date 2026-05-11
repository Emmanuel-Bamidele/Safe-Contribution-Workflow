# Scope Rules

The contribution must stay inside the smallest safe scope.

## Before editing

Identify:

- The requested contribution
- The smallest safe change
- Files likely to change
- Files that should not change
- Public behavior to preserve
- Tests required
- Risks to other teams or modules

## Allowed changes

Allowed changes must directly support the requested contribution.

Examples:

- Modify a specific component for a UI task.
- Modify a specific endpoint for an API task.
- Modify a specific service for a bug fix.
- Add tests for the changed behavior.
- Update documentation for the changed behavior.

## Not allowed

Do not make unrelated changes such as:

- Broad cleanup
- Opportunistic refactors
- Reformatting unrelated files
- Renaming unrelated variables
- Reorganizing folders
- Rewriting shared modules
- Changing public APIs without need
- Deleting code that only appears unused
- Adding dependencies for convenience

## If scope expands

Stop and explain:

- Why the original scope is not enough
- What new files or areas are involved
- What risk this creates
- Whether the user should approve the expanded scope

Do not silently expand scope.
