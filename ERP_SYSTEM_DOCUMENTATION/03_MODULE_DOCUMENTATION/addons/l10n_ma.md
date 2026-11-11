# Module: l10n_ma

- **Module ID:** MOD-266
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ma`
- **Manifest:** `addons/l10n_ma/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Morocco.

This module has been built with the help of Caudigef.

**Scope evidence:** The module contains 19 files, including 8 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 3
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

- **Description:** 3 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ma/models/base_document_layout.py:7`, `addons/l10n_ma/models/account_journal.py:4`, `addons/l10n_ma/models/template_ma.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_ma/controllers/portal.py`, `addons/l10n_ma/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 321 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ma/demo/demo_company.xml:3`, `addons/l10n_ma/demo/demo_company.xml:15`, `addons/l10n_ma/data/account_tax_report_data.xml:3`, `addons/l10n_ma/data/account_tax_report_data.xml:11`, `addons/l10n_ma/data/account_tax_report_data.xml:16`, `addons/l10n_ma/data/account_tax_report_data.xml:21`, `addons/l10n_ma/data/account_tax_report_data.xml:27`, `addons/l10n_ma/data/account_tax_report_data.xml:34`, `addons/l10n_ma/data/account_tax_report_data.xml:39`, `addons/l10n_ma/data/account_tax_report_data.xml:45`, `addons/l10n_ma/data/account_tax_report_data.xml:52`, `addons/l10n_ma/data/account_tax_report_data.xml:58`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_ma`, `base.demo_company_ma`, `tax_report_vat`, `tax_report_column_base`, `tax_report_column_base_tax`, `tax_report_column_pro`, `tax_report_column_tax`, `tax_report_part_a`, `tax_report_line_10`, `tax_report_line_10_base`, `tax_report_line_20`, `tax_report_line_20_base`, `tax_report_line_30`, `tax_report_line_30_base`, `tax_report_line_40`, `tax_report_line_40_base`, `tax_report_line_50`, `tax_report_line_50_base`, `tax_report_line_55`, `tax_report_line_55_base`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_ma/views/portal_address_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ma/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `base.document.layout` (addons/l10n_ma/models/base_document_layout.py:7); inherits `account.journal` (addons/l10n_ma/models/account_journal.py:4); inherits `account.chart.template` (addons/l10n_ma/models/template_ma.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_ma/__init__.py`
- `addons/l10n_ma/__manifest__.py`
- `addons/l10n_ma/controllers/__init__.py`
- `addons/l10n_ma/controllers/portal.py`
- `addons/l10n_ma/data/account_tax_report_data.xml`
- `addons/l10n_ma/data/template/account.account-ma.csv`
- `addons/l10n_ma/data/template/account.depreciation.model-ma.csv`
- `addons/l10n_ma/data/template/account.fiscal.position-ma.csv`
- `addons/l10n_ma/data/template/account.tax-ma.csv`
- `addons/l10n_ma/data/template/account.tax.group-ma.csv`
- `addons/l10n_ma/demo/demo_company.xml`
- `addons/l10n_ma/i18n/ar.po`
- `addons/l10n_ma/i18n/fr.po`
- `addons/l10n_ma/i18n/l10n_ma.pot`
- `addons/l10n_ma/models/__init__.py`
- `addons/l10n_ma/models/account_journal.py`
- `addons/l10n_ma/models/base_document_layout.py`
- `addons/l10n_ma/models/template_ma.py`
- `addons/l10n_ma/views/portal_address_templates.xml`
