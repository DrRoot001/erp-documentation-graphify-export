# Model Relationships

Implement relationship semantics from `Relationship_Register.csv`: `Many2one` references, `One2many` inverses, and `Many2many` association structures. Preserve source evidence for target model, inverse field, relation table, and on-delete behavior when present.

Where any relationship attribute is absent from static extraction, record it as `UNKNOWN` and resolve it through source review or runtime registry inspection. Do not select cascade/set-null/restrict behavior from generic ERP conventions.
