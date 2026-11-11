# Module: l10n_mn

- **Module ID:** MOD-271
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_mn`
- **Manifest:** `addons/l10n_mn/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the module to manage the accounting chart for Mongolia.
===============================================================

    * the Mongolia Official Chart of Accounts,
    * the Tax Code Chart for Mongolia
    * the main taxes used in Mongolia

Financial requirement contributor: Baskhuu Lodoikhuu. BumanIT LLC

**Scope evidence:** The module contains 13 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_mn/models/template_mn.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 123 record/template/menu identifiers.
- **Evidence:** `addons/l10n_mn/demo/demo_company.xml:3`, `addons/l10n_mn/demo/demo_company.xml:16`, `addons/l10n_mn/data/vat_report.xml:3`, `addons/l10n_mn/data/vat_report.xml:9`, `addons/l10n_mn/data/vat_report.xml:15`, `addons/l10n_mn/data/vat_report.xml:20`, `addons/l10n_mn/data/vat_report.xml:25`, `addons/l10n_mn/data/vat_report.xml:29`, `addons/l10n_mn/data/vat_report.xml:36`, `addons/l10n_mn/data/vat_report.xml:41`, `addons/l10n_mn/data/vat_report.xml:46`, `addons/l10n_mn/data/vat_report.xml:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_mn`, `base.demo_company_mn`, `account_report_vat_report`, `account_report_vat_report_column`, `vat_report_lineA`, `vat_report_line1`, `vat_report_line2`, `vat_report_line2_tag`, `vat_report_line3`, `vat_report_line4`, `vat_report_line5`, `vat_report_line5_tag`, `vat_report_line6`, `vat_report_line6_tag`, `vat_report_line7`, `vat_report_line7_tag`, `vat_report_line8`, `vat_report_line8_tag`, `vat_report_line9`, `vat_report_line9_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_mn/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_mn/models/template_mn.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_mn/__init__.py`
- `addons/l10n_mn/__manifest__.py`
- `addons/l10n_mn/data/account.account.tag.csv`
- `addons/l10n_mn/data/template/account.account-mn.csv`
- `addons/l10n_mn/data/template/account.fiscal.position-mn.csv`
- `addons/l10n_mn/data/template/account.tax-mn.csv`
- `addons/l10n_mn/data/template/account.tax.group-mn.csv`
- `addons/l10n_mn/data/vat_report.xml`
- `addons/l10n_mn/demo/demo_company.xml`
- `addons/l10n_mn/i18n/l10n_mn.pot`
- `addons/l10n_mn/i18n/mn.po`
- `addons/l10n_mn/models/__init__.py`
- `addons/l10n_mn/models/template_mn.py`
