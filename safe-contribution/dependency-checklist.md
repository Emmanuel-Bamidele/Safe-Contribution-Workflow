# Dependency Checklist

Use this before adding or changing dependencies.

## Before adding a dependency

Ask:

- Is this dependency necessary?
- Can the standard library solve this?
- Does the project already have a helper?
- Is the package maintained?
- Is the license acceptable?
- Is the package size reasonable?
- Does it add many transitive dependencies?
- Is it needed in production?
- Does it introduce security risk?

## Avoid

- Dependencies for trivial helpers
- Duplicate libraries
- Unmaintained packages
- Silent major upgrades
- Runtime dependencies for dev-only tasks
- Packages with suspicious install scripts

## If adding a dependency

You must:

- Explain why it is needed.
- Update lockfiles.
- Run relevant tests.
- Mention it in the final response.
- Document any security or bundle-size concerns.
