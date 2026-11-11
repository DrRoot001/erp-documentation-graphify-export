# Module: l10n_kr

- **Module ID:** MOD-254
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_kr`
- **Manifest:** `addons/l10n_kr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Accounting Module for the Republic of Korea
===========================================
This provides a base chart of accounts and taxes template for use in Odoo.

**Scope evidence:** The module contains 22 files, including 8 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_kr/models/res_partner.py:13`, `addons/l10n_kr/models/template_kr.py:6`, `addons/l10n_kr/models/account_move.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 587 record/template/menu identifiers.
- **Evidence:** `addons/l10n_kr/demo/demo_company.xml:3`, `addons/l10n_kr/demo/demo_company.xml:15`, `addons/l10n_kr/data/res_country_data.xml:3`, `addons/l10n_kr/data/res_country_data.xml:28`, `addons/l10n_kr/data/simplified_tax_report.xml:3`, `addons/l10n_kr/data/simplified_tax_report.xml:15`, `addons/l10n_kr/data/simplified_tax_report.xml:20`, `addons/l10n_kr/data/simplified_tax_report.xml:26`, `addons/l10n_kr/data/simplified_tax_report.xml:32`, `addons/l10n_kr/data/simplified_tax_report.xml:39`, `addons/l10n_kr/data/simplified_tax_report.xml:45`, `addons/l10n_kr/data/simplified_tax_report.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_kr/tests/__init__.py`, `addons/l10n_kr/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_kr`, `base.demo_company_kr`, `kr_partner_address_form`, `base.kr`, `l10n_kr_simplified_tp_vat`, `l10n_kr_simplified_tp_vat_column_balance`, `l10n_kr_simplified_tp_vat_column_varate`, `l10n_kr_simplified_tp_vat_column_rate`, `l10n_kr_simplified_tp_vat_column_tax`, `l10n_kr_simplified_tp_vat_sfi`, `l10n_kr_simplified_tp_vat_stbot`, `l10n_kr_simplified_tp_vat_stbb`, `l10n_kr_simplified_tp_vat_segsw`, `l10n_kr_simplified_tp_vat_segsw_balance`, `l10n_kr_simplified_tp_vat_segsw_rate`, `l10n_kr_simplified_tp_vat_segsw_varate`, `l10n_kr_simplified_tp_vat_segsw_tax`, `l10n_kr_simplified_tp_vat_srtcw`, `l10n_kr_simplified_tp_vat_srtcw_balance`, `l10n_kr_simplified_tp_vat_srtcw_rate`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_kr/data/res_country_data.xml:5`, `addons/l10n_kr/data/res_country_data.xml:7`, `addons/l10n_kr/views/account_move_views.xml:5`, `addons/l10n_kr/views/account_move_views.xml:7`, `addons/l10n_kr/views/res_partner_views.xml:5`, `addons/l10n_kr/views/res_partner_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_kr/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner` (addons/l10n_kr/models/res_partner.py:13); inherits `account.chart.template` (addons/l10n_kr/models/template_kr.py:6); inherits `account.move` (addons/l10n_kr/models/account_move.py:7)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_kr/__init__.py`
- `addons/l10n_kr/__manifest__.py`
- `addons/l10n_kr/data/account.account.tag.csv`
- `addons/l10n_kr/data/general_tax_report.xml`
- `addons/l10n_kr/data/res_country_data.xml`
- `addons/l10n_kr/data/simplified_tax_report.xml`
- `addons/l10n_kr/data/template/account.account-kr.csv`
- `addons/l10n_kr/data/template/account.depreciation.model-kr.csv`
- `addons/l10n_kr/data/template/account.fiscal.position-kr.csv`
- `addons/l10n_kr/data/template/account.tax-kr.csv`
- `addons/l10n_kr/data/template/account.tax.group-kr.csv`
- `addons/l10n_kr/demo/demo_company.xml`
- `addons/l10n_kr/i18n/ko.po`
- `addons/l10n_kr/i18n/l10n_kr.pot`
- `addons/l10n_kr/models/__init__.py`
- `addons/l10n_kr/models/account_move.py`
- `addons/l10n_kr/models/res_partner.py`
- `addons/l10n_kr/models/template_kr.py`
- `addons/l10n_kr/tests/__init__.py`
- `addons/l10n_kr/tests/test_account_move.py`
- `addons/l10n_kr/views/account_move_views.xml`
- `addons/l10n_kr/views/res_partner_views.xml`
