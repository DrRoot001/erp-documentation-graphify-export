# Database Constraints — Phase 6

Static extraction found 572 constraint-evidence rows, including `_sql_constraints` declarations and ORM `@api.constrains` methods. SQL constraints are applied at database/model initialization; Python constraints run through ORM operations. Exact generated PostgreSQL constraint names, indexes, and inherited effects depend on the installed module graph and database state.

See `Constraint_Dictionary.csv`, `Table_Query_Inventory.csv`, and `Migration_Inventory.csv`.

## Static SQL/migration inventories

- SQL artifacts: `SQL_Artifact_Inventory.csv`.
- Migration artifacts: `Migration_Inventory.csv`.
- Computed/query-backed model evidence: `Table_Query_Inventory.csv`.
