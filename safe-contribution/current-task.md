# Current Contribution

Use this file to describe the exact contribution you want to make.

Replace the placeholder content below before asking an agent to work.

---

## Goal

Describe the known contribution.

Example:

```text
Add CSV export to the invoices page.
```

---

## Why this contribution is needed

Explain the reason for the change.

Example:

```text
Users need to export filtered invoice lists for accounting workflows.
```

---

## Scope

### Allowed changes

List files, areas, or behaviors the agent may modify.

```text
- Invoice export button
- Invoice export API route
- CSV formatting helper if needed
- Tests for invoice export
```

### Not allowed

List files, areas, or behaviors the agent should not modify.

```text
- Do not rewrite invoice permissions.
- Do not refactor invoice models.
- Do not change unrelated billing UI.
- Do not reformat unrelated files.
- Do not add dependencies unless justified.
```

---

## Required behavior

Describe what must work after the contribution.

```text
- User can export invoices as CSV.
- Export respects existing invoice filters.
- Export only includes invoices the user is authorized to access.
```

---

## Existing behavior to preserve

Describe behavior that should not change.

```text
- Existing invoice list filters still work.
- Existing invoice permissions still apply.
- Existing billing UI behavior remains unchanged.
```

---

## Required tests

List tests that should be added or updated.

```text
- CSV export works.
- Unauthorized users cannot export another organization's invoices.
- Empty invoice list exports a valid empty CSV.
```

---

## Checks to run

List relevant commands if known.

```bash
npm test
npm run lint
npm run typecheck
npm run build
```

---

## Risks to consider

List any known risks.

```text
- Authorization must be preserved.
- Large exports should not crash the server.
- CSV output should not expose fields users cannot normally see.
```
