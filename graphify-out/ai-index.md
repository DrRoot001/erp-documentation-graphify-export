# ERP SYSTEM AI Graph Index

## Purpose

Use this index before opening large source files. It provides a compact map from system areas to evidence and implementation artifacts, reducing repeated repository-wide reading during cloning.

## Fast routing

| Task | Start node/section | Then inspect |
|---|---|---|
| Product/module behavior | `module:<name>` | module README, requirements, workflows, tests |
| Database/entity work | `entity:<source-id>` or `section:database` | Entity/Field/Relationship registers and module source |
| API work | `endpoint:API-xxxx` or `section:api` | Endpoint register, controller source, auth/security records |
| Workflow work | `workflow:WF-MOD-xxx` or `section:workflows` | module workflow register and state evidence |
| Security work | `group:<xml-id>` or `section:security` | group, ACL, record-rule, route-security registers |
| Frontend work | `ui:views`, `ui:frontend`, or `ui:templates` | view/template/component registers and module UI evidence |
| Clone planning | `section:roadmap` or `section:governance` | MVP, build order, parity, traceability, runtime backlog |

## Query pattern

1. Select the smallest relevant node set from `graph.json`.
2. Follow `contains`, `satisfies`, `declares`, `exposes`, and `implements` edges.
3. Use each node's `source_file` and `summary` to open only the necessary evidence.
4. Preserve the evidence label; never turn `UNKNOWN` or runtime-pending work into an invented behavior.

## High-value anchors

- Source master index: `ERP_SYSTEM_DOCUMENTATION/MASTER_INDEX.md`
- Blueprint entry point: `CLONEABLE_ERP_BLUEPRINT/00_START_HERE/README.md`
- Module coverage: `CLONEABLE_ERP_BLUEPRINT/13_TRACEABILITY_AND_GOVERNANCE/Module_Coverage_Register.csv`
- Requirements: `CLONEABLE_ERP_BLUEPRINT/13_TRACEABILITY_AND_GOVERNANCE/Requirements_Traceability_Register.csv`
- Runtime backlog: `CLONEABLE_ERP_BLUEPRINT/13_TRACEABILITY_AND_GOVERNANCE/RUNTIME_VALIDATION_BACKLOG.md`

## Graph semantics

`EXTRACTED` means directly supported by an inventory or documented mapping. No `INFERRED` or `AMBIGUOUS` edge is included in this deterministic baseline. A future upstream Graphify semantic run may add those edge types; review them separately.
