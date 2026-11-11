# Data Dictionary

The machine-readable dictionaries are the authoritative source-derived data dictionary for the clone baseline:

- [`Entity_Register.csv`](Entity_Register.csv): 4,209 model/entity declarations.
- [`Field_Register.csv`](Field_Register.csv): 17,272 field declarations with ORM type, related model, inverse, required, readonly, store, index, deletion, compute, default, label, and selection evidence where available.
- [`Relationship_Register.csv`](Relationship_Register.csv): 5,290 cardinality and relationship metadata.
- [`Constraint_Register.csv`](Constraint_Register.csv): 572 SQL/Python constraint evidence.

Each row carries an evidence status and a runtime-validation status. Missing literal values remain blank/unknown; the clone team must not infer them from field names.
