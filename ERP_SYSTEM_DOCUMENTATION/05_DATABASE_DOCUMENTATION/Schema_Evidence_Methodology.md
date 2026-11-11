# Schema Evidence Methodology — Phase 6

## Extraction rules

- Entity rows come from Python classes containing literal `_name`, `_inherit`, or `_inherits` metadata.
- Field rows come from class assignments calling `fields.<Type>`, including literal relationship targets and keyword attributes where available.
- Relationship rows include literal `Many2one`, `One2many`, and `Many2many` declarations and their inverse/relation/on-delete metadata when present.
- Constraint rows include `_sql_constraints` assignments and methods decorated with `@api.constrains`.
- SQL rows include repository `.sql` files; migration rows include files under `migrations/` or `migrate/`.
- `_table_query` is reported separately and is empty when no literal declaration is found.

## Limitations

AST extraction cannot resolve dynamic field factories, Python conditionals, inherited fields after registry composition, module installation order, database-generated indexes, PostgreSQL extensions, or deployment-specific schema state. The resulting CSVs are evidence inventories for architecture and review, not a substitute for a live registry/schema export.
