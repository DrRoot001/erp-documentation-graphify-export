# Module: l10n_mx

- **Module ID:** MOD-277
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_mx`
- **Manifest:** `addons/l10n_mx/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Minimal accounting configuration for Mexico.
============================================

This Chart of account is a minimal proposal to be able to use OoB the
accounting feature of Odoo.

This doesn't pretend be all the localization for MX it is just the minimal
data required to start from 0 in mexican localization.

This modules and its content is updated frequently by openerp-mexico team.

With this module you will have:

 - Minimal chart of account tested in production environments.
 - Minimal chart of taxes, to comply with SAT_ requirements.

.. _SAT: http://www.sat.gob.mx/

**Scope evidence:** The module contains 31 files, including 16 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 13 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_mx/models/res_config_settings.py:6`, `addons/l10n_mx/models/template_mx.py:6`, `addons/l10n_mx/models/account_tax.py:5`, `addons/l10n_mx/models/account_account.py:4`, `addons/l10n_mx/models/account_move_line.py:4`, `addons/l10n_mx/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 72 record/template/menu identifiers.
- **Evidence:** `addons/l10n_mx/demo/demo_company.xml:3`, `addons/l10n_mx/demo/demo_company.xml:16`, `addons/l10n_mx/demo/demo_company.xml:21`, `addons/l10n_mx/data/l10n_mx_uom.xml:6`, `addons/l10n_mx/data/l10n_mx_uom.xml:10`, `addons/l10n_mx/data/l10n_mx_uom.xml:14`, `addons/l10n_mx/data/account_report_diot.xml:3`, `addons/l10n_mx/data/account_report_diot.xml:19`, `addons/l10n_mx/data/account_report_diot.xml:25`, `addons/l10n_mx/data/account_report_diot.xml:31`, `addons/l10n_mx/data/account_report_diot.xml:37`, `addons/l10n_mx/data/account_report_diot.xml:43`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_mx/tests/test_account_account.py`, `addons/l10n_mx/tests/common.py`, `addons/l10n_mx/tests/__init__.py`, `addons/l10n_mx/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_mx`, `base.demo_company_mx`, `base.demo_bank_mx`, `product_uom_service_unit`, `product_uom_activity`, `product_uom_job`, `diot_report`, `diot_report_paid_8_n_wnc`, `diot_report_paid_8_n_r`, `diot_report_paid_8_s_wnc`, `diot_report_paid_8_s_r`, `diot_report_paid_16_wnc`, `diot_report_paid_16_r`, `diot_report_paid_16_imp_wnc`, `diot_report_paid_16_imp_r`, `diot_report_paid_16_imp_int_wnc`, `diot_report_paid_16_imp_int_r`, `diot_report_paid_8_n`, `diot_report_paid_8_s`, `diot_report_paid_16`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_mx/views/res_config_settings_views.xml:7`, `addons/l10n_mx/views/res_config_settings_views.xml:10`, `addons/l10n_mx/views/account_views.xml:5`, `addons/l10n_mx/views/account_views.xml:7`, `addons/l10n_mx/views/account_tax_view.xml:5`, `addons/l10n_mx/views/account_tax_view.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_mx/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.config.settings` (addons/l10n_mx/models/res_config_settings.py:6); inherits `account.chart.template` (addons/l10n_mx/models/template_mx.py:6); inherits `account.tax` (addons/l10n_mx/models/account_tax.py:5); inherits `account.account` (addons/l10n_mx/models/account_account.py:4); inherits `account.move.line` (addons/l10n_mx/models/account_move_line.py:4); inherits `res.company` (addons/l10n_mx/models/res_company.py:6)
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

- `addons/l10n_mx/__init__.py`
- `addons/l10n_mx/__manifest__.py`
- `addons/l10n_mx/data/account.account.tag.csv`
- `addons/l10n_mx/data/account_report_diot.xml`
- `addons/l10n_mx/data/l10n_mx_uom.xml`
- `addons/l10n_mx/data/template/account.account-mx.csv`
- `addons/l10n_mx/data/template/account.asset-mx.csv`
- `addons/l10n_mx/data/template/account.depreciation.model-mx.csv`
- `addons/l10n_mx/data/template/account.fiscal.position-mx.csv`
- `addons/l10n_mx/data/template/account.tax-mx.csv`
- `addons/l10n_mx/data/template/account.tax.group-mx.csv`
- `addons/l10n_mx/demo/demo_company.xml`
- `addons/l10n_mx/i18n/es_419.po`
- `addons/l10n_mx/i18n/l10n_mx.pot`
- `addons/l10n_mx/migrations/2.1/post-migrate.py`
- `addons/l10n_mx/migrations/2.2/end-migrate.py`
- `addons/l10n_mx/migrations/2.4/post-migrate.py`
- `addons/l10n_mx/models/__init__.py`
- `addons/l10n_mx/models/account_account.py`
- `addons/l10n_mx/models/account_move_line.py`
- `addons/l10n_mx/models/account_tax.py`
- `addons/l10n_mx/models/res_company.py`
- `addons/l10n_mx/models/res_config_settings.py`
- `addons/l10n_mx/models/template_mx.py`
- `addons/l10n_mx/tests/__init__.py`
- `addons/l10n_mx/tests/common.py`
- `addons/l10n_mx/tests/test_account_account.py`
- `addons/l10n_mx/tests/test_account_move.py`
- `addons/l10n_mx/views/account_tax_view.xml`
- `addons/l10n_mx/views/account_views.xml`
- `addons/l10n_mx/views/res_config_settings_views.xml`
