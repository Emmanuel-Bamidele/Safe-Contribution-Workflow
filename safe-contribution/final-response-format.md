# Final Response Format

Use this format after making the contribution.

```md
## Contribution completed

Briefly describe the contribution.

## Files changed

- `path/to/file`: why it changed
- `path/to/file`: why it changed

## Scope control

Confirm:
- What was intentionally changed
- What was intentionally not changed
- Any unrelated issues discovered but not fixed

## Tests and checks run

- `command`: passed / failed / not run
- `command`: passed / failed / not run

If not run, explain why.

## Behavior impact

Describe user-visible or system-visible behavior changes.

## Security considerations

Mention authentication, authorization, input validation, secrets, logging, or data exposure if relevant.

## Compatibility considerations

Mention API, database, config, UI, CLI, or shared type compatibility if relevant.

## Risks

Describe remaining risk.

## Rollback

Explain how to revert safely.

## Follow-up

List any recommended follow-up issues.
```

## Honesty rule

Do not claim success if checks failed or were not run.

Say exactly what happened.
