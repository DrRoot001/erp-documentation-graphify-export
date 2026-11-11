# Database Overview

## Source architecture — VERIFIED

The source persistence architecture uses PostgreSQL through psycopg2, the Odoo SQL layer, an ORM registry, model inheritance, transactions, migrations, and addon-selected runtime materialization. PostgreSQL 16 is the declared minimum in the source release metadata.

## Cloneable data architecture

The clone shall provide relational persistence with transactional writes, explicit migrations, model/entity metadata, relationship constraints, audit/lifecycle fields, multi-company or tenant isolation where evidenced, and registry/schema validation. PostgreSQL is a compatible implementation choice, not a mandatory clone technology.

| Evidence | Count | Status |
|---|---:|---|
| Entity/model declarations | 4,209 | VERIFIED source; runtime table mapping required |
| Field declarations | 17,272 | VERIFIED source; runtime column mapping required |
| Relationship declarations | 5,290 | VERIFIED source; runtime registry required |
| Constraint rows | 572 | VERIFIED source; generated DB names require validation |
| Migration artifacts | 88 | VERIFIED source |
| Literal `_table_query` declarations | 0 | VERIFIED absence in static scan |

## Field types

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


Exact tables, columns, indexes, generated constraints, inherited fields, and materialized views require a configured registry or sanitized deployed schema.
