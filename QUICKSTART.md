# Quickstart

Use this repository when you already know the contribution you want to make.

This workflow helps you make that contribution safely inside a shared codebase.

It is not for finding contribution ideas.

It is for executing a known contribution with a clear scope and minimal side effects.

---

## 1. Copy the workflow folder

Copy this folder into your codebase:

```text
safe-contribution/
```

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

---

## 2. Decide whether to commit it

### Commit it if the team should share it

Commit `safe-contribution/` if the workflow should be part of the repository.

This is useful for:

- Teams
- Open-source projects
- Maintainer-led repositories
- Repositories that allow AI-assisted contributions

### Keep it local if it is only for you

If you want to keep it local, add this to `.gitignore`:

```gitignore
# Local safe contribution workflow
safe-contribution/
```

Do not forget this step if you do not want the folder committed.

---

## 3. Define your known contribution

Open:

```text
safe-contribution/current-task.md
```

Describe the exact contribution you want to make.

Example:

```md
# Current Contribution

## Goal

Add CSV export to the invoices page.

## Scope

Allowed:
- Invoice export button
- Invoice export API route
- CSV formatting helper if needed
- Tests for invoice export

Not allowed:
- Rewriting invoice permissions
- Refactoring invoice models
- Changing unrelated billing UI
- Reformatting unrelated files
- Adding dependencies unless justified

## Required behavior

- User can export invoices as CSV.
- Export respects existing invoice filters.
- Export only includes invoices the user is authorized to access.

## Required tests

- CSV export works.
- Unauthorized users cannot export another organization's invoices.
- Empty invoice list exports a valid empty CSV.
```

---

## 4. Give the agent the safe contribution prompt

Paste this into your coding agent:

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

Use `safe-contribution/final-response-format.md` for your final response.
```

---

## 5. Review the agent's plan before it edits

Before editing, the agent should provide:

```text
- Restated contribution
- Smallest safe scope
- Files likely to change
- Files or areas not to touch
- Existing behavior to preserve
- Tests to add or update
- Risks and compatibility concerns
```

If the agent's scope is too broad, stop it and narrow the task.

---

## 6. Let the agent make the contribution

The agent should then:

```text
- Change only required files
- Avoid unrelated refactors
- Avoid unrelated formatting
- Avoid unrelated deletion
- Add or update tests
- Run relevant checks
- Report failures honestly
```

---

## 7. Review the final response

The final response should include:

```text
- What changed
- Why each file changed
- Tests run
- Checks run
- Security considerations
- Compatibility considerations
- Risks
- Anything intentionally not changed
```

---

## 8. Use the reviewer checklist before merging

Use:

```text
templates/reviewer-checklist.md
```

Before merging, confirm:

```text
- The contribution matches the requested task
- The diff is focused
- Unrelated files were not changed
- Existing behavior is preserved
- Tests were added or updated
- Relevant checks were run
- Security and data risks were considered
- The change is safe for other contributors
```

---

## Good use cases

Use this workflow for:

```text
- Fixing a known bug
- Adding a known feature
- Updating a specific UI component
- Improving a specific API endpoint
- Adding a specific test
- Making a bounded refactor
- Updating documentation
- Adding a small database change
- Modifying a specific workflow
```

---

## Bad use cases

Do not use this workflow for prompts like:

```text
Find something to improve.
```

```text
Clean up the whole codebase.
```

```text
Refactor everything.
```

```text
Fix all issues.
```

```text
Make this production-ready.
```

For those cases, use a codebase audit or repair workflow instead.

---

## Main rule

The contribution is already known.

The job is safe execution.

```text
Known task.
Small scope.
Minimal changes.
Tests included.
No unrelated damage.
```
