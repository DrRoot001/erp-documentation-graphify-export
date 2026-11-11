# Module: l10n_id

- **Module ID:** MOD-221
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_id`
- **Manifest:** `addons/l10n_id/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the latest Indonesian Odoo localisation necessary to run Odoo accounting for SMEs with:
=================================================================================================
    - generic Indonesian chart of accounts
    - tax structure

**Scope evidence:** The module contains 28 files, including 15 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 5
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_id/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 36 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_id/models/res_bank.py:28`, `addons/l10n_id/models/template_id.py:6`, `addons/l10n_id/models/qris_transaction.py:7`, `addons/l10n_id/models/account_move.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_id/controllers/portal.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/l10n_id/demo/demo_company.xml:3`, `addons/l10n_id/demo/demo_company.xml:16`, `addons/l10n_id/data/ir_cron.xml:3`, `addons/l10n_id/views/res_config_settings_views.xml:4`, `addons/l10n_id/views/res_bank.xml:4`, `addons/l10n_id/views/account_move_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_id/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_id/__manifest__.py`, `addons/l10n_id/models/qris_transaction.py`, `addons/l10n_id/models/account_move.py`, `addons/l10n_id/data/ir_cron.xml`, `addons/l10n_id/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_id/tests/test_qris_transaction.py`, `addons/l10n_id/tests/test_qris.py`, `addons/l10n_id/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_id`, `base.demo_company_id`, `qris_fetch_cron`, `res_config_settings_view_form`, `view_partner_bank_form_inherit_account`, `action_fetch_qris_status`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/l10n_id/views/res_config_settings_views.xml:6`, `addons/l10n_id/views/res_config_settings_views.xml:8`, `addons/l10n_id/views/res_bank.xml:6`, `addons/l10n_id/views/res_bank.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_id/__manifest__.py`
- **HTTP entry points:** `addons/l10n_id/controllers/portal.py:8`
- **Scheduled entry points:** `addons/l10n_id/__manifest__.py`, `addons/l10n_id/models/qris_transaction.py`, `addons/l10n_id/models/account_move.py`, `addons/l10n_id/data/ir_cron.xml`, `addons/l10n_id/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner.bank` (addons/l10n_id/models/res_bank.py:28); inherits `account.chart.template` (addons/l10n_id/models/template_id.py:6); `l10n_id.qris.transaction` (addons/l10n_id/models/qris_transaction.py:7); inherits `account.move` (addons/l10n_id/models/account_move.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_id/controllers/portal.py:8`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_id/__init__.py`
- `addons/l10n_id/__manifest__.py`
- `addons/l10n_id/controllers/__init__.py`
- `addons/l10n_id/controllers/portal.py`
- `addons/l10n_id/data/ir_cron.xml`
- `addons/l10n_id/data/template/account.account-id.csv`
- `addons/l10n_id/data/template/account.depreciation.model-id.csv`
- `addons/l10n_id/data/template/account.fiscal.position-id.csv`
- `addons/l10n_id/data/template/account.tax-id.csv`
- `addons/l10n_id/data/template/account.tax.group-id.csv`
- `addons/l10n_id/demo/demo_company.xml`
- `addons/l10n_id/i18n/id.po`
- `addons/l10n_id/i18n/l10n_id.pot`
- `addons/l10n_id/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_id/migrations/1.2/end-migrate_update_taxes.py`
- `addons/l10n_id/migrations/1.3/end-migrate_update_taxes.py`
- `addons/l10n_id/models/__init__.py`
- `addons/l10n_id/models/account_move.py`
- `addons/l10n_id/models/qris_transaction.py`
- `addons/l10n_id/models/res_bank.py`
- `addons/l10n_id/models/template_id.py`
- `addons/l10n_id/security/ir.access.csv`
- `addons/l10n_id/tests/__init__.py`
- `addons/l10n_id/tests/test_qris.py`
- `addons/l10n_id/tests/test_qris_transaction.py`
- `addons/l10n_id/views/account_move_views.xml`
- `addons/l10n_id/views/res_bank.xml`
- `addons/l10n_id/views/res_config_settings_views.xml`
