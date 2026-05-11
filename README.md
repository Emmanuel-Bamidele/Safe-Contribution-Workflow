# Safe Contribution Workflow

> Prompts, rules, and checklists for making a known code contribution safely in a shared codebase.

This repository is for developers and AI coding agents who already know the change they want to make.

It does **not** help you find something to contribute.

It helps you make your intended contribution safely, with a focused scope, minimal side effects, proper tests, and respect for the existing codebase.

---

## The problem

Large codebases are shared spaces.

A small contribution can accidentally become dangerous when a developer or AI coding agent:

- Touches unrelated files
- Deletes code that looked unused
- Refactors modules outside the task
- Reformats large parts of the repository
- Changes public APIs without warning
- Breaks another team’s feature
- Adds unnecessary dependencies
- Changes database schema casually
- Weakens authentication or authorization
- Updates shared types without understanding impact
- Fixes one bug while creating three new ones
- Claims success without running checks

This repository helps prevent that.

---

## What this repository is for

Use this when you already know the contribution you want to make.

Examples:

- Fix a specific bug
- Add a specific feature
- Update a specific component
- Improve a specific endpoint
- Add a specific test
- Modify a specific workflow
- Refactor a specific bounded area
- Update a specific integration
- Add a specific database field
- Improve a specific documentation page

The purpose is safe execution.

---

## What this repository is not for

This is not for asking an agent to search for work.

It is not for broad cleanup.

It is not for rewriting the architecture.

It is not for “make this codebase better” prompts.

It is not for fixing unrelated issues discovered along the way.

If unrelated issues are discovered, document them separately and continue with the original task unless they block the contribution.

---

## Core idea

The user provides a known contribution:

```text
Add CSV export to the invoices page.
```

or:

```text
Fix the password reset email bug.
```

or:

```text
Add dark mode support to account settings.
```

Then the workflow helps the agent answer:

```text
What is the smallest safe scope?
Which files are likely to change?
Which files should not be touched?
What existing behavior must be preserved?
What tests prove this contribution works?
What security boundaries are involved?
What could break for other teammates?
```

---

## How this works

Copy the `safe-contribution/` folder into your codebase.

Recommended layout:

```text
your-codebase/
  safe-contribution/
    CONTRIBUTION.md
    current-task.md
    current-task.template.md
    scope-rules.md
    no-unrelated-changes.md
    testing-checklist.md
    risk-checklist.md
    compatibility-checklist.md
    security-checklist.md
    database-checklist.md
    dependency-checklist.md
    final-response-format.md
```

Then describe your intended contribution in:

```text
safe-contribution/current-task.md
```

Finally, tell your coding agent:

```text
Read `safe-contribution/CONTRIBUTION.md`.
Read `safe-contribution/current-task.md`.

Make only the contribution described in `current-task.md`.

Do not modify unrelated files.
Do not delete unrelated code.
Do not refactor unrelated modules.
Do not reformat unrelated files.

Add or update tests.
Run relevant checks.
Return your response using `safe-contribution/final-response-format.md`.
```

---

## Should I commit the folder?

You have two options.

### Option A: Commit it

Commit `safe-contribution/` if you want the workflow to be shared by the team.

This is best for:

- Teams
- Open-source projects
- Company repositories
- Repositories with many AI-assisted contributors
- Projects where maintainers want consistent contribution rules

### Option B: Keep it local

Keep `safe-contribution/` local if you are contributing to someone else’s repo or using the workflow only for yourself.

Add this to `.gitignore`:

```gitignore
# Local safe contribution workflow
safe-contribution/
```

Do not forget this step if you do not want the folder committed.

---

## Recommended workflow

Use this sequence:

```text
1. Write the intended contribution in `safe-contribution/current-task.md`.
2. Ask the agent to read `safe-contribution/CONTRIBUTION.md`.
3. Ask the agent to inspect relevant files before editing.
4. Ask the agent to identify the smallest safe scope.
5. Ask the agent to list files it expects to change.
6. Ask the agent to list files or areas it should not touch.
7. Ask the agent to make only the required change.
8. Ask the agent to add or update tests.
9. Ask the agent to run relevant checks.
10. Ask the agent to summarize changes, risks, and anything left untouched.
```

---

## Best first prompt

Use this after copying the folder into a codebase:

```text
Read `safe-contribution/CONTRIBUTION.md`.
Read `safe-contribution/current-task.md`.

I already know the contribution I want to make.

Your job is not to find other work to do.

Your job is to make this contribution safely inside the existing codebase.

Before editing:
- understand the requested contribution
- identify the smallest safe scope
- list files likely to change
- list files that should not be touched
- identify existing behavior to preserve
- identify tests to add or update
- identify risks to other parts of the codebase

During editing:
- change only what is required
- do not refactor unrelated code
- do not delete unrelated files
- do not reformat unrelated files
- do not change public APIs unless required
- do not add dependencies unless justified

After editing:
- summarize what changed
- explain why each file changed
- list tests run
- list checks run
- document risks
- mention anything intentionally left unchanged
```

---

## Repository structure

```text
Safe-Contribution-Workflow/
  README.md
  QUICKSTART.md
  LICENSE
  GITIGNORE-SNIPPET.md

  safe-contribution/
    CONTRIBUTION.md
    current-task.md
    current-task.template.md
    scope-rules.md
    no-unrelated-changes.md
    testing-checklist.md
    risk-checklist.md
    compatibility-checklist.md
    security-checklist.md
    database-checklist.md
    dependency-checklist.md
    final-response-format.md
    contribution-plan-template.md

  examples/
    bug-fix-current-task.md
    feature-current-task.md
    refactor-current-task.md
    documentation-current-task.md
    database-current-task.md
    frontend-current-task.md
    backend-current-task.md

  templates/
    pull-request-template.md
    reviewer-checklist.md
    risk-summary-template.md
    contribution-summary-template.md
```

---

## What the workflow enforces

The contribution should be:

- Known
- Scoped
- Minimal
- Testable
- Reviewable
- Compatible
- Safe for teammates
- Safe for users
- Safe for data
- Safe for production

The agent should not:

- Search for extra work
- Make unrelated improvements
- Rewrite unrelated code
- Delete unrelated files
- Reformat unrelated files
- Change public contracts silently
- Add dependencies casually
- Modify migrations casually
- Hide failing tests
- Claim success without evidence

---

## Good contribution prompt

```text
Read `safe-contribution/CONTRIBUTION.md`.
Read `safe-contribution/current-task.md`.

Make only the contribution described.

Do not modify unrelated files.
Do not refactor unrelated code.
Do not delete code unless directly required.
Do not reformat unrelated files.
Add or update tests.
Run relevant checks.
Use `safe-contribution/final-response-format.md` in your final response.
```

---

## Bad contribution prompts

Avoid:

```text
Improve this codebase.
```

```text
Clean this up while you are there.
```

```text
Fix anything else you notice.
```

```text
Refactor the whole module.
```

```text
Make all tests pass however you can.
```

These are too broad for safe team contribution.

---

## How this fits with other agent workflow repositories

This repository pairs well with:

```text
AI-Agent-Coding-Rules
```

Use that for permanent agent behavior rules inside a repository.

```text
Fix-AI-Written-Code
```

Use that to audit and repair messy AI-generated codebases.

```text
Safe-Contribution-Workflow
```

Use this when you already know the contribution and want to make it safely.

Together:

```text
AI-Agent-Coding-Rules      -> rules agents should always follow
Fix-AI-Written-Code        -> repair messy AI-generated codebases
Safe-Contribution-Workflow -> safely execute one known contribution
```

---

## Suggested repository description

```text
Prompts and checklists for making a known code contribution safely in a shared codebase.
```

---

## Suggested tagline

```text
Make your change without breaking everyone else’s work.
```

---

## Suggested GitHub topics

```text
ai
ai-agents
coding-agents
code-review
software-engineering
developer-tools
contribution-workflow
pull-requests
team-development
safe-refactoring
testing
ci-cd
security
best-practices
```

---

## Contributing

Contributions are welcome.

Good contributions include:

- Better safe contribution prompts
- New task examples
- Framework-specific contribution rules
- Language-specific examples
- Better reviewer checklists
- Better PR templates
- Improvements for open-source maintainers
- Improvements for team workflows

Please keep the workflow focused on known contributions, small diffs, and safe execution.

---

## Disclaimer

This repository provides prompts, checklists, and workflow templates.

It does not guarantee that an AI-generated or human-written contribution is safe.

Always review changes carefully before merging, especially changes involving authentication, authorization, payments, personal data, database migrations, infrastructure, or production systems.

---

## Final note

A good contribution is not just code that works.

A good contribution solves the requested problem while respecting everything around it.

**Safe Contribution Workflow** helps developers and AI agents make changes without stepping on the rest of the codebase.
