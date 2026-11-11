# Table Specifications

The repository does not provide a deployed PostgreSQL schema. Therefore this document defines the implementation procedure rather than inventing physical tables.

For each runtime entity, the clone team shall specify: physical table identity, primary key, columns and types, nullability, defaults, computed/materialized behavior, foreign keys, inverse relationships, unique constraints, indexes, audit fields, company/tenant boundary, deletion behavior, migration version, and retention/lifecycle policy.

Model extensions must be merged into the target entity before table generation. Transient models, abstract models, SQL/query-backed models, and inherited models require separate handling.
