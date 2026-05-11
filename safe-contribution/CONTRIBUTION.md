# Safe Contribution Instructions

Read this before making changes.

This workflow is for a known contribution.

The user already knows what they want to contribute.

Your job is not to search for extra work.

Your job is to execute the requested contribution safely inside the existing codebase.

---

## Mission

Make the requested contribution with the smallest safe change.

Preserve unrelated behavior.

Avoid damaging other people's work.

Keep the diff focused, reviewable, and testable.

---

## Required first step

Before editing files, read:

```text
safe-contribution/current-task.md
```

Then inspect relevant code.

Do not edit files until you can explain:

```text
- What the contribution is
- What the smallest safe scope is
- Which files are likely to change
- Which files or areas should not be touched
- Which behavior must be preserved
- Which tests should be added or updated
- Which risks exist
```

---

## Core rules

You must:

- Make only the requested contribution.
- Keep the diff focused.
- Preserve existing public behavior unless the task requires changing it.
- Add or update tests for behavior changes.
- Run relevant checks when possible.
- Report failures honestly.
- Explain changed files.
- Document risks.

You must not:

- Search for unrelated improvements.
- Refactor unrelated code.
- Delete unrelated code.
- Reformat unrelated files.
- Change public APIs unless required.
- Add dependencies unless justified.
- Modify database migrations casually.
- Weaken authentication or authorization.
- Hide failing tests.
- Suppress errors without explanation.
- Claim success without evidence.

---

## If you discover unrelated problems

If you discover unrelated issues, do not fix them unless they block the contribution.

Instead, document them under:

```text
Follow-up issues discovered
```

Then continue with the original contribution.

---

## If the requested contribution is unsafe

If the contribution would create a security, data, compatibility, or production risk, stop and explain:

```text
- What the risk is
- Why it matters
- Safer alternative
- What confirmation is needed
```

Do not implement an unsafe version silently.

---

## Final response

Use:

```text
safe-contribution/final-response-format.md
```
