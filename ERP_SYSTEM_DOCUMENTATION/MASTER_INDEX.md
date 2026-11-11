# ERP SYSTEM Documentation Index

## Repository baseline

- Source repository: `DrRoot001/odoo`
- Snapshot: `1cc16ad8a00f3cd35e4e685b433424681a8ce5be`
- Documentation package generated from the repository snapshot; generated files are excluded from the source inventory.
- Inventory coverage: 50,889/50,889 source/repository files enumerated outside `.git` and generated documentation.

## Sections

- [Executive overview](00_EXECUTIVE_OVERVIEW/Executive_Summary.md)
- [Codebase analysis](01_CODEBASE_ANALYSIS/Project_Structure.md)
- [Requirements](02_REQUIREMENTS/Software_Requirements_Specification.md)
- [Functional requirements register](02_REQUIREMENTS/Functional_Requirements_Document.md) — Phase 3 detailed FRD and `Functional_Requirements.csv`
- [Validation rules](02_REQUIREMENTS/Validation_Rules.csv) — constraints, dependencies, security, jobs, reports
- [Requirements traceability](10_TESTING/Requirements_Traceability.csv) — requirement-to-source/test links
- [Master traceability matrix](10_TESTING/Master_Traceability_Matrix.csv) — Phase 13 requirement-to-module/UI/API/database/test chain
- [Traceability gaps](10_TESTING/Traceability_Gaps.csv)
- [Module catalog](03_MODULE_DOCUMENTATION/Module_Catalog.md) — 666 per-addon evidence pages in `03_MODULE_DOCUMENTATION/addons/`
- [Module hierarchy](03_MODULE_DOCUMENTATION/Module_Hierarchy.md) — normalized Phase 2 domain classification
- [Detailed module specifications](03_MODULE_DOCUMENTATION/Module_Detail_Methodology.md) — Phase 4 evidence structure for all 666 modules
- [Module detail index](03_MODULE_DOCUMENTATION/Module_Detail_Index.csv) — aggregate artifact and dependency metrics
- [Feature inventory](03_MODULE_DOCUMENTATION/Feature_Inventory.csv) — one evidence-backed feature row per manifest
- [Coverage matrix](03_MODULE_DOCUMENTATION/Module_Coverage_Matrix.md) — domain artifact totals
- [Architecture](04_SYSTEM_ARCHITECTURE/System_Architecture.md)
- [Database](05_DATABASE_DOCUMENTATION/Database_Overview.md) — Phase 6 ORM/entity/field/relationship extraction
- [Entity dictionary](05_DATABASE_DOCUMENTATION/Entity_Dictionary.md)
- [Field dictionary](05_DATABASE_DOCUMENTATION/Field_Dictionary.csv)
- [Relationship dictionary](05_DATABASE_DOCUMENTATION/Relationship_Dictionary.csv)
- [Constraint dictionary](05_DATABASE_DOCUMENTATION/Constraint_Dictionary.csv)
- [Representative ERD](05_DATABASE_DOCUMENTATION/Representative_ERD.md)
- [Schema evidence methodology](05_DATABASE_DOCUMENTATION/Schema_Evidence_Methodology.md)
- [SQL and migration inventories](05_DATABASE_DOCUMENTATION/SQL_Artifact_Inventory.csv)
- [API](06_API_DOCUMENTATION/API_Overview.md) — Phase 7 route and integration extraction
- [API endpoint inventory](06_API_DOCUMENTATION/API_Endpoint_Inventory.csv)
- [Webhook inventory](06_API_DOCUMENTATION/Webhook_Inventory.csv)
- [Integration inventory](06_API_DOCUMENTATION/Integration_Inventory.csv)
- [Workflows](07_WORKFLOWS/Workflow_Catalog.md) — Phase 5 workflow families and evidence inventory
- [Workflow evidence inventory](07_WORKFLOWS/Workflow_Evidence_Inventory.csv) — module-level workflow surfaces
- [Security](08_SECURITY/Security_Architecture.md) — Phase 8 security/control inventories
- [Security file inventory](08_SECURITY/Security_File_Inventory.csv)
- [Group inventory](08_SECURITY/Group_Inventory.csv)
- [Access/rule inventories](08_SECURITY/Model_Access_Inventory.csv) — Phase 8 security/control inventories
- [UI/UX](09_UI_UX_DOCUMENTATION/Screen_Inventory.md) — Phase 9 XML/navigation/frontend inventory
- [UI/UX evidence methodology](09_UI_UX_DOCUMENTATION/UI_UX_Evidence_Methodology.md)
- [UI/UX traceability](09_UI_UX_DOCUMENTATION/UI_Traceability.md)
- [View/menu/action inventories](09_UI_UX_DOCUMENTATION/View_Inventory.csv) — Phase 9 XML/navigation/frontend inventory
- [Testing strategy](10_TESTING/Testing_Strategy.md) — Phase 10 test evidence and execution limits
- [Existing test coverage](10_TESTING/Existing_Test_Coverage.md)
- [Test file inventory](10_TESTING/Test_File_Inventory.csv)
- [Module test coverage](10_TESTING/Test_Module_Coverage.csv)
- [Evidence-linked test cases](10_TESTING/Evidence_Test_Cases.csv)
- [Testing traceability](10_TESTING/Traceability_Matrix.md)
- [Installation guide](11_DEPLOYMENT_AND_OPERATIONS/Installation_Guide.md) — Phase 11 verified installation surfaces
- [Configuration guide](11_DEPLOYMENT_AND_OPERATIONS/Configuration_Guide.md)
- [Environment variables](11_DEPLOYMENT_AND_OPERATIONS/Environment_Variables.md)
- [Deployment guide](11_DEPLOYMENT_AND_OPERATIONS/Deployment_Guide.md)
- [Backup and recovery](11_DEPLOYMENT_AND_OPERATIONS/Backup_Recovery.md)
- [Maintenance guide](11_DEPLOYMENT_AND_OPERATIONS/Maintenance_Guide.md)
- [Deployment artifact inventory](11_DEPLOYMENT_AND_OPERATIONS/Deployment_Artifact_Inventory.csv)
- [Configuration option inventory](11_DEPLOYMENT_AND_OPERATIONS/Configuration_Option_Inventory.csv)
- [Environment variable inventory](11_DEPLOYMENT_AND_OPERATIONS/Environment_Variable_Inventory.csv)
- [Migration artifact inventory](11_DEPLOYMENT_AND_OPERATIONS/Migration_Artifact_Inventory.csv)
- [Implementation gaps](12_AUDIT_AND_RECOMMENDATIONS/Implementation_Gaps.md) — Phase 12 classified audit findings
- [Technical debt](12_AUDIT_AND_RECOMMENDATIONS/Technical_Debt.md)
- [Security findings](12_AUDIT_AND_RECOMMENDATIONS/Security_Findings.md)
- [Improvement roadmap](12_AUDIT_AND_RECOMMENDATIONS/Improvement_Roadmap.md)
- [Audit finding register](12_AUDIT_AND_RECOMMENDATIONS/Audit_Finding_Register.csv)
- [Debt marker inventory](12_AUDIT_AND_RECOMMENDATIONS/Debt_Marker_Inventory.csv)

## Evidence and limitations

This package documents actual source artifacts and explicitly labels runtime-dependent conclusions as requiring verification. It does not invent a tenant-specific installed module set, database schema, API payloads, performance targets, permissions matrix, or production deployment.

- [Phase 14 final completeness audit](14_FINAL_COMPLETENESS_AUDIT.md)
- [Phase 15 final release handoff](15_FINAL_RELEASE_HANDOFF.md)
- [Phase 16 publication audit](16_PUBLICATION_AUDIT.md)
- [Phase 17 publication status](17_PUBLICATION_STATUS.md)
- [Phase 18 publication review audit](18_PUBLICATION_REVIEW_AUDIT.md)
- [Phase 19 publication current state](19_PUBLICATION_CURRENT_STATE.md)
- [Phase 20 publication snapshot](20_PUBLICATION_SNAPSHOT.md)
