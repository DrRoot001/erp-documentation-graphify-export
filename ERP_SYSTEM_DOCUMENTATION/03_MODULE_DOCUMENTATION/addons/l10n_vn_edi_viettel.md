# Module: l10n_vn_edi_viettel

- **Module ID:** MOD-342
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_vn_edi_viettel`
- **Manifest:** `addons/l10n_vn_edi_viettel/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-invoicing using SInvoice by Viettel

**Manifest description:**

Vietnam - E-invoicing
=====================
Using SInvoice by Viettel

**Scope evidence:** The module contains 25 files, including 16 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_vn`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_vn_edi_viettel/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 84 methods, 1 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_vn_edi_viettel/models/res_partner.py:6`, `addons/l10n_vn_edi_viettel/models/res_config_settings.py:6`, `addons/l10n_vn_edi_viettel/models/account_journal.py:6`, `addons/l10n_vn_edi_viettel/models/account_move.py:13`, `addons/l10n_vn_edi_viettel/models/account_move_send.py:8`, `addons/l10n_vn_edi_viettel/models/sinvoice.py:10`, `addons/l10n_vn_edi_viettel/models/res_company.py:9`, `addons/l10n_vn_edi_viettel/wizard/account_move_reversal.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/l10n_vn_edi_viettel/wizard/account_move_reversal_view.xml:4`, `addons/l10n_vn_edi_viettel/views/res_config_settings_views.xml:3`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:3`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:39`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:52`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:68`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:80`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:4`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:16`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:34`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:49`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:64`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_vn_edi_viettel/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel/tests/test_edi.py`, `addons/l10n_vn_edi_viettel/tests/__init__.py`, `addons/l10n_vn_edi_viettel/tests/test_sinvoice.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `view_account_move_reversal_inherit_l10n_vn_edi`, `res_config_settings_view_form_inherit_l10n_vn_edi`, `view_invoice_form_inherit_l10n_vn_edi`, `view_account_invoice_filter_inherit_l10n_vn_edi`, `view_invoice_tree_inherit_l10n_vn_edi`, `l10n_vn_edi_send_invoice_payment_status`, `l10n_vn_edi_fetch_tax_code`, `view_l10n_vn_edi_viettel_sinvoice_symbol_search`, `view_l10n_vn_edi_viettel_sinvoice_symbol_list`, `view_l10n_vn_edi_viettel_sinvoice_symbol_form`, `action_sinvoice_symbol`, `SInvoice`, `l10n_vn_edi_sinvoice_symbols`, `account_journal_form_inherit_l10n_vn_edi_viettel`
- Menus: 2; representative evidence: `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:64`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:66`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 20; representative evidence: `addons/l10n_vn_edi_viettel/wizard/account_move_reversal_view.xml:6`, `addons/l10n_vn_edi_viettel/wizard/account_move_reversal_view.xml:8`, `addons/l10n_vn_edi_viettel/views/res_config_settings_views.xml:5`, `addons/l10n_vn_edi_viettel/views/res_config_settings_views.xml:7`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:5`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:7`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:41`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:43`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:54`, `addons/l10n_vn_edi_viettel/views/account_move_views.xml:56`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:6`, `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_vn_edi_viettel/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_vn_edi_viettel/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/l10n_vn_edi_viettel/models/res_partner.py:6); inherits `res.config.settings` (addons/l10n_vn_edi_viettel/models/res_config_settings.py:6); inherits `account.journal` (addons/l10n_vn_edi_viettel/models/account_journal.py:6); inherits `account.move` (addons/l10n_vn_edi_viettel/models/account_move.py:13); inherits `account.move.send` (addons/l10n_vn_edi_viettel/models/account_move_send.py:8); `l10n_vn_edi_viettel.sinvoice.symbol` (addons/l10n_vn_edi_viettel/models/sinvoice.py:10); inherits `res.company` (addons/l10n_vn_edi_viettel/models/res_company.py:9); inherits `account.move.reversal` (addons/l10n_vn_edi_viettel/wizard/account_move_reversal.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_vn`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_vn_edi_viettel/__init__.py`
- `addons/l10n_vn_edi_viettel/__manifest__.py`
- `addons/l10n_vn_edi_viettel/data/neutralize.sql`
- `addons/l10n_vn_edi_viettel/i18n/l10n_vn_edi_viettel.pot`
- `addons/l10n_vn_edi_viettel/i18n/vi.po`
- `addons/l10n_vn_edi_viettel/models/__init__.py`
- `addons/l10n_vn_edi_viettel/models/account_journal.py`
- `addons/l10n_vn_edi_viettel/models/account_move.py`
- `addons/l10n_vn_edi_viettel/models/account_move_send.py`
- `addons/l10n_vn_edi_viettel/models/res_company.py`
- `addons/l10n_vn_edi_viettel/models/res_config_settings.py`
- `addons/l10n_vn_edi_viettel/models/res_partner.py`
- `addons/l10n_vn_edi_viettel/models/sinvoice.py`
- `addons/l10n_vn_edi_viettel/models/sinvoice_service.py`
- `addons/l10n_vn_edi_viettel/security/ir.access.csv`
- `addons/l10n_vn_edi_viettel/tests/__init__.py`
- `addons/l10n_vn_edi_viettel/tests/test_edi.py`
- `addons/l10n_vn_edi_viettel/tests/test_sinvoice.py`
- `addons/l10n_vn_edi_viettel/views/account_journal_views.xml`
- `addons/l10n_vn_edi_viettel/views/account_move_views.xml`
- `addons/l10n_vn_edi_viettel/views/res_config_settings_views.xml`
- `addons/l10n_vn_edi_viettel/views/sinvoice_views.xml`
- `addons/l10n_vn_edi_viettel/wizard/__init__.py`
- `addons/l10n_vn_edi_viettel/wizard/account_move_reversal.py`
- `addons/l10n_vn_edi_viettel/wizard/account_move_reversal_view.xml`
