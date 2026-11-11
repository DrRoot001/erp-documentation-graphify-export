# Database Overview — Phase 6

## Engine and access

The repository declares PostgreSQL as the persistence engine, accessed through `psycopg2`, Odoo's SQL connection layer, and the ORM registry. Release metadata states PostgreSQL 16 minimum (`odoo/release.py:32`).

## Static schema evidence

| Evidence | Count |
|---|---:|
| ORM entity/class declarations | 4,209 |
| ORM field declarations extracted | 17,272 |
| Relationship fields extracted | 5,290 |
| Constraint evidence rows | 572 |
| `_table_query` declarations | 0 |
| SQL artifacts | 81 |
| Migration artifacts | 88 |

## ORM field types

- `Many2one`: 3,547
- `Char`: 3,409
- `Boolean`: 2,653
- `Selection`: 1,620
- `Integer`: 1,472
- `Many2many`: 934
- `Float`: 826
- `One2many`: 809
- `Date`: 357
- `Datetime`: 349
- `Text`: 315
- `Monetary`: 312
- `Html`: 224
- `Json`: 122
- `Binary`: 109
- `Image`: 109
- `Properties`: 27
- `Reference`: 26
- `PropertiesDefinition`: 25
- `Many2oneReference`: 23
- `Id`: 3
- `Serialized`: 1

## Relationship types

- `Many2one`: 3,547
- `Many2many`: 934
- `One2many`: 809


## Schema boundary

This is a source-derived schema evidence layer, not a deployed database dump. Odoo model inheritance, installed addon selection, module updates, PostgreSQL version, configuration, and migration history determine the final tables, columns, indexes, constraints, and views. Exact database metadata requires registry introspection or a sanitized PostgreSQL schema from the target deployment.
