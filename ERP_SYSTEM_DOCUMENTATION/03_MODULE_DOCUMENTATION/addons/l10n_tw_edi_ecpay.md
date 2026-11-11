# Module: l10n_tw_edi_ecpay

- **Module ID:** MOD-328
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_tw_edi_ecpay`
- **Manifest:** `addons/l10n_tw_edi_ecpay/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-invoicing using ECpay

**Manifest description:**

Taiwan - E-invoicing
=====================
This module allows the user to send their invoices to the Ecpay system.

**Scope evidence:** The module contains 29 files, including 19 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_tw`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 2
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_tw_edi_ecpay/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 73 methods, 1 constraint handlers, 1 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/l10n_tw_edi_ecpay/models/res_partner.py:6`, `addons/l10n_tw_edi_ecpay/models/res_config_settings.py:6`, `addons/l10n_tw_edi_ecpay/models/account_tax.py:7`, `addons/l10n_tw_edi_ecpay/models/account_move.py:15`, `addons/l10n_tw_edi_ecpay/models/account_move_line.py:4`, `addons/l10n_tw_edi_ecpay/models/account_move_send.py:8`, `addons/l10n_tw_edi_ecpay/models/res_company.py:6`, `addons/l10n_tw_edi_ecpay/wizard/account_move_reversal.py:6`, `addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_print.py:8`, `addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_cancel.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/l10n_tw_edi_ecpay/controllers/main.py:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_print_view.xml:3`, `addons/l10n_tw_edi_ecpay/views/account_move_view.xml:4`, `addons/l10n_tw_edi_ecpay/views/account_move_view.xml:42`, `addons/l10n_tw_edi_ecpay/views/account_move_reversal_view.xml:4`, `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_cancel_view.xml:3`, `addons/l10n_tw_edi_ecpay/views/res_config_setting_view.xml:4`, `addons/l10n_tw_edi_ecpay/views/account_tax.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_tw_edi_ecpay/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_tw_edi_ecpay/views/account_move_view.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_tw_edi_ecpay/tests/test_edi.py`, `addons/l10n_tw_edi_ecpay/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `l10n_tw_edi_invoice_print_form`, `view_move_form_inherit_ecpay`, `action_print_ecpay_invoice`, `view_account_move_reversal_inherit_ecpay`, `l10n_tw_edi_invoice_cancel_form`, `res_config_settings_view_form`, `ec_view_tax_form_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_print_view.xml:5`, `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_print_view.xml:6`, `addons/l10n_tw_edi_ecpay/views/account_move_view.xml:6`, `addons/l10n_tw_edi_ecpay/views/account_move_view.xml:8`, `addons/l10n_tw_edi_ecpay/views/account_move_reversal_view.xml:6`, `addons/l10n_tw_edi_ecpay/views/account_move_reversal_view.xml:8`, `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_cancel_view.xml:5`, `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_cancel_view.xml:6`, `addons/l10n_tw_edi_ecpay/views/res_config_setting_view.xml:6`, `addons/l10n_tw_edi_ecpay/views/res_config_setting_view.xml:8`, `addons/l10n_tw_edi_ecpay/views/account_tax.xml:6`, `addons/l10n_tw_edi_ecpay/views/account_tax.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_tw_edi_ecpay/__manifest__.py`
- **HTTP entry points:** `addons/l10n_tw_edi_ecpay/controllers/main.py:11`
- **Scheduled entry points:** `addons/l10n_tw_edi_ecpay/views/account_move_view.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `res.partner` (addons/l10n_tw_edi_ecpay/models/res_partner.py:6); inherits `res.config.settings` (addons/l10n_tw_edi_ecpay/models/res_config_settings.py:6); inherits `account.tax` (addons/l10n_tw_edi_ecpay/models/account_tax.py:7); inherits `account.move` (addons/l10n_tw_edi_ecpay/models/account_move.py:15); inherits `account.move.line` (addons/l10n_tw_edi_ecpay/models/account_move_line.py:4); inherits `account.move.send` (addons/l10n_tw_edi_ecpay/models/account_move_send.py:8); inherits `res.company` (addons/l10n_tw_edi_ecpay/models/res_company.py:6); inherits `account.move.reversal` (addons/l10n_tw_edi_ecpay/wizard/account_move_reversal.py:6); `l10n_tw_edi.invoice.print` (addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_print.py:8); `l10n_tw_edi.invoice.cancel` (addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_cancel.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/l10n_tw_edi_ecpay/controllers/main.py:11`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_tw`
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

- `addons/l10n_tw_edi_ecpay/__init__.py`
- `addons/l10n_tw_edi_ecpay/__manifest__.py`
- `addons/l10n_tw_edi_ecpay/controllers/__init__.py`
- `addons/l10n_tw_edi_ecpay/controllers/main.py`
- `addons/l10n_tw_edi_ecpay/data/neutralize.sql`
- `addons/l10n_tw_edi_ecpay/i18n/l10n_tw_edi_ecpay.pot`
- `addons/l10n_tw_edi_ecpay/i18n/zh_TW.po`
- `addons/l10n_tw_edi_ecpay/models/__init__.py`
- `addons/l10n_tw_edi_ecpay/models/account_move.py`
- `addons/l10n_tw_edi_ecpay/models/account_move_line.py`
- `addons/l10n_tw_edi_ecpay/models/account_move_send.py`
- `addons/l10n_tw_edi_ecpay/models/account_tax.py`
- `addons/l10n_tw_edi_ecpay/models/res_company.py`
- `addons/l10n_tw_edi_ecpay/models/res_config_settings.py`
- `addons/l10n_tw_edi_ecpay/models/res_partner.py`
- `addons/l10n_tw_edi_ecpay/security/ir.access.csv`
- `addons/l10n_tw_edi_ecpay/tests/__init__.py`
- `addons/l10n_tw_edi_ecpay/tests/test_edi.py`
- `addons/l10n_tw_edi_ecpay/utils.py`
- `addons/l10n_tw_edi_ecpay/views/account_move_reversal_view.xml`
- `addons/l10n_tw_edi_ecpay/views/account_move_view.xml`
- `addons/l10n_tw_edi_ecpay/views/account_tax.xml`
- `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_cancel_view.xml`
- `addons/l10n_tw_edi_ecpay/views/l10n_tw_edi_invoice_print_view.xml`
- `addons/l10n_tw_edi_ecpay/views/res_config_setting_view.xml`
- `addons/l10n_tw_edi_ecpay/wizard/__init__.py`
- `addons/l10n_tw_edi_ecpay/wizard/account_move_reversal.py`
- `addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_cancel.py`
- `addons/l10n_tw_edi_ecpay/wizard/l10n_tw_edi_invoice_print.py`
