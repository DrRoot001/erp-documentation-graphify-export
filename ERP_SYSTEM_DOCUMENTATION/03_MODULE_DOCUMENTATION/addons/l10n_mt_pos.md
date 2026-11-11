# Module: l10n_mt_pos

- **Module ID:** MOD-275
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_mt_pos`
- **Manifest:** `addons/l10n_mt_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Malta Compliance Letter for EXO Number

**Scope evidence:** The module contains 7 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_mt_pos/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_mt_pos/wizards/compliance_letter.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:2`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:16`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:22`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:23`, `addons/l10n_mt_pos/reports/compliance_letter_report.xml:40`, `addons/l10n_mt_pos/reports/compliance_letter_report.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_mt_pos/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_mt_pos/reports/compliance_letter_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `view_generate_compliance_letter`, `action_generate_compliance_letter`, `Malta EXO`, `Compliance Letter`, `report_compliance_letter`, `report_compliance_letter_template`
- Menus: 2; representative evidence: `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:22`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:23`
- Templates: 1; representative evidence: `addons/l10n_mt_pos/reports/compliance_letter_report.xml:2`
- View/action field declarations: 5; representative evidence: `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:4`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:5`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:18`, `addons/l10n_mt_pos/wizards/compliance_letter_view.xml:19`, `addons/l10n_mt_pos/reports/compliance_letter_report.xml:42`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_mt_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_mt_pos/reports/compliance_letter_report.xml`

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: `compliance.letter.wizard` (addons/l10n_mt_pos/wizards/compliance_letter.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_mt_pos/__init__.py`
- `addons/l10n_mt_pos/__manifest__.py`
- `addons/l10n_mt_pos/reports/compliance_letter_report.xml`
- `addons/l10n_mt_pos/security/ir.access.csv`
- `addons/l10n_mt_pos/wizards/__init__.py`
- `addons/l10n_mt_pos/wizards/compliance_letter.py`
- `addons/l10n_mt_pos/wizards/compliance_letter_view.xml`
