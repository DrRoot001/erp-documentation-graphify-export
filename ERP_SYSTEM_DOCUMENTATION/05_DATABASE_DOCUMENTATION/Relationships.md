# Relationships — Phase 6

The machine-readable relationship dictionary is `Relationship_Dictionary.csv`; it contains 5,290 extracted `Many2one`, `One2many`, `Many2many`, and related relationship declarations.

| Relationship | Count |
|---|---:|
| `Many2one` | 3,547 |
| `Many2many` | 934 |
| `One2many` | 809 |


Relationship cardinality is based on the ORM field type. Target model, inverse field, relation table, and on-delete behavior are recorded only when literal or keyword evidence was available. Inherited and dynamically generated fields require runtime registry inspection.
