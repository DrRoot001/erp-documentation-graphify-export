# Technical Debt — Phase 12

Static inspection found **2,936 TODO/FIXME/deprecation markers** across core, addons, and setup source files, plus **164 `NotImplementedError` occurrences**. These are review signals, not proof that all marked code is defective: some are deliberate extension points, abstract contracts, compatibility shims, tests, or unreachable optional paths.

| Debt signal | Count | Interpretation |
|---|---:|---|
| TODO/FIXME/deprecation markers | 2,936 | Maintenance and future-work indicators requiring triage |
| `NotImplementedError` occurrences | 164 | Explicit unimplemented/abstract paths requiring reachability review |

The machine-readable evidence is [`Debt_Marker_Inventory.csv`](Debt_Marker_Inventory.csv). Priorities are inheritance/runtime schema drift, optional integration configuration, route authorization consistency, migration completeness, test isolation, observability, and deployment-specific capacity.
