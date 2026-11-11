# Entity Relationships

The source relationship register contains 5,290 declarations. Cardinality is derived from ORM field types, not from naming.

| Relationship type | Count | Clone requirement |
|---|---:|---|
| `Many2one` | 3,547 | Implement cardinality, inverse behavior, deletion policy, and transaction semantics from the register and source. |
| `Many2many` | 934 | Implement cardinality, inverse behavior, deletion policy, and transaction semantics from the register and source. |
| `One2many` | 809 | Implement cardinality, inverse behavior, deletion policy, and transaction semantics from the register and source. |


Inherited models and dynamically resolved fields must be merged through the clone's metadata/registry process before generating physical schema. A source `_inherit` declaration is not automatically a new table.
