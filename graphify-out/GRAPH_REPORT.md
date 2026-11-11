# ERP SYSTEM Graphify Report

This repository contains a deterministic, source-evidence-backed Graphify-compatible baseline. It is designed to give AI agents a compact traversal surface before they read the full ERP source or documentation.

## Graph inventory

| Node kind | Count |
|---|---:|
| api_endpoint | 669 |
| domain | 14 |
| entity | 4,209 |
| module | 666 |
| requirement | 2,963 |
| section | 14 |
| security_group | 149 |
| system | 1 |
| ui_surface | 3 |
| workflow | 666 |

| Total edges | 10,257 |

## Evidence boundary

- `EXTRACTED` relationships come from the existing inventories and blueprint mappings.
- This baseline does not claim that runtime database tables, API payloads, UI inheritance, tests, or production topology were executed.
- Use the runtime validation backlog at `CLONEABLE_ERP_BLUEPRINT/13_TRACEABILITY_AND_GOVERNANCE/RUNTIME_VALIDATION_BACKLOG.md`.

## Highest-connectivity modules

- `website` — 141 graph connections
- `account` — 116 graph connections
- `mail` — 113 graph connections
- `point_of_sale` — 88 graph connections
- `stock` — 76 graph connections
- `website_slides` — 73 graph connections
- `mrp` — 64 graph connections
- `test_import_export` — 63 graph connections
- `website_forum` — 62 graph connections
- `mass_mailing` — 58 graph connections
- `test_mail` — 57 graph connections
- `website_sale` — 53 graph connections
- `test_website` — 52 graph connections
- `test_http` — 52 graph connections
- `hr_holidays` — 51 graph connections
- `pos_self_order` — 51 graph connections
- `project` — 51 graph connections
- `sale` — 48 graph connections
- `hr` — 47 graph connections
- `survey` — 46 graph connections


## Recommended AI traversal

1. Read `graphify-out/ai-index.md`.
2. Query `graphify-out/graph.json` by node kind, module, requirement, endpoint, entity, or workflow.
3. Follow edges to the authoritative source evidence path.
4. Open the linked blueprint module README only after the graph narrows the task.
5. Treat UNKNOWN/runtime-validation labels as blockers, not facts to fill by assumption.
