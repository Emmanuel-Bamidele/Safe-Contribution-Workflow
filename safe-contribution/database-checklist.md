# Database Checklist

Use this when the contribution touches schema, migrations, models, persistence, or data writes.

## Schema changes

Before schema changes, consider:

- Existing data
- Migration order
- Rollback
- Downtime risk
- Backfill strategy
- Index impact
- Compatibility with current code

## Avoid unsafe migrations

Avoid:

- Adding `NOT NULL` columns without backfill
- Dropping columns immediately
- Renaming columns without compatibility
- Rewriting large tables in one step
- Deleting data without backup
- Changing enum values unsafely
- Adding blocking indexes on large tables

## Safer migration pattern

Use staged migration when needed:

```text
1. Add nullable field or new table.
2. Deploy compatible code.
3. Backfill safely.
4. Verify.
5. Enforce constraints.
6. Remove old path later.
```

## Transactions

Use transactions for:

- Multi-table writes
- Payment updates
- Permission changes
- Account changes
- Inventory changes
- Audit log plus sensitive mutation

## Query safety

Check:

- Tenant filters
- Authorization filters
- Bounded queries
- Pagination
- Index support
- No raw SQL interpolation
