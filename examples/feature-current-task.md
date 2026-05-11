# Current Contribution: Feature Example

## Goal

Add CSV export for the invoices list.

## Why this contribution is needed

Users need to export filtered invoice lists for accounting workflows.

## Scope

### Allowed changes

- Invoice list export button
- Invoice export API route
- CSV formatting helper if needed
- Tests for CSV export

### Not allowed

- Do not rewrite invoice permissions.
- Do not refactor invoice models.
- Do not change unrelated billing UI.
- Do not add dependencies unless justified.
- Do not change existing invoice filters.

## Required behavior

- User can export invoices as CSV.
- Export respects existing filters.
- Export includes only authorized invoice data.
- Empty result exports a valid empty CSV.

## Existing behavior to preserve

- Existing invoice list still loads.
- Existing filters still work.
- Existing permissions still apply.

## Required tests

- CSV export returns expected content.
- CSV export respects filters.
- Unauthorized users cannot export another organization's invoices.
- Empty export works.

## Checks to run

```bash
npm test
npm run typecheck
npm run lint
```

## Risks to consider

- CSV should not expose hidden fields.
- Large exports should be bounded or streamed if needed.
