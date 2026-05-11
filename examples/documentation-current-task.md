# Current Contribution: Documentation Example

## Goal

Update local development setup instructions.

## Why this contribution is needed

The current README is missing the database setup command.

## Scope

### Allowed changes

- README local setup section
- Development setup docs

### Not allowed

- Do not change application code.
- Do not modify CI.
- Do not update unrelated docs.

## Required behavior

- A new developer can follow the documented setup steps.
- Commands are accurate.

## Existing behavior to preserve

- Existing deployment docs remain unchanged.
- Existing production notes remain unchanged.

## Required tests

No automated test required unless docs commands can be validated.

## Checks to run

```bash
# Run documented setup commands if practical.
```

## Risks to consider

- Do not document secrets.
- Do not include machine-specific paths.
