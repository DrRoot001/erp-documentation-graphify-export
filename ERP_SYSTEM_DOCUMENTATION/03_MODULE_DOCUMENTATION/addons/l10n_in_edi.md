# Module: l10n_in_edi

- **Module ID:** MOD-229
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_edi`
- **Manifest:** `addons/l10n_in_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Indian - E-invoicing
====================
To submit invoicing through API to the government.
We use "Tera Software Limited" as GSP
Step 1: First you need to create an API username and password in the E-invoice portal.
Step 2: Switch to company related to that GST number
Step 3: Set that username and password in Odoo (Goto: Invoicing/Accounting -> Configuration -> Settings -> Customer Invoices or find "E-invoice" in search bar)
Step 4: Repeat steps 1,2,3 for all GSTIN you have in odoo. If you have a multi-company with the same GST number then perform step 1 for the first company only.
For the creation of API username and password please ref this document: <https://service.odoo.co.in/einvoice_create_api_user>

**Scope evidence:** The module contains 25 files, including 15 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_in_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 43 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_in_edi/models/res_partner.py:6`, `addons/l10n_in_edi/models/res_config_settings.py:5`, `addons/l10n_in_edi/models/account_journal.py:5`, `addons/l10n_in_edi/models/account_move.py:25`, `addons/l10n_in_edi/models/account_move_line.py:4`, `addons/l10n_in_edi/models/account_move_send.py:4`, `addons/l10n_in_edi/models/ir_attachment.py:5`, `addons/l10n_in_edi/models/res_company.py:9`, `addons/l10n_in_edi/wizard/l10n_in_edi_cancel.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_edi/demo/demo_company.xml:4`, `addons/l10n_in_edi/wizard/l10n_in_edi_cancel_views.xml:4`, `addons/l10n_in_edi/views/res_config_settings_views.xml:3`, `addons/l10n_in_edi/views/edi_pdf_report.xml:3`, `addons/l10n_in_edi/views/account_move_views.xml:3`, `addons/l10n_in_edi/views/account_move_views.xml:46`, `addons/l10n_in_edi/views/account_move_views.xml:61`, `addons/l10n_in_edi/views/account_move_views.xml:76`, `addons/l10n_in_edi/views/account_journal_dashboard_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_in_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_in_edi/tests/test_edi_json.py`, `addons/l10n_in_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.demo_company_in`, `view_ewaybill_cancel_form`, `res_config_settings_view_form_inherit_l10n_in_edi`, `l10n_in_einvoice_report_invoice_document_inherit`, `invoice_form_inherit_l10n_in_edi`, `view_out_invoice_tree_inherit_l10n_in_edi`, `view_out_credit_note_tree_inherit_l10n_in_edi`, `l10n_in_edi_inherit_account_move_search_view`, `account_journal_dashboard_kanban_view_in`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_in_edi/views/edi_pdf_report.xml:3`
- View/action field declarations: 14; representative evidence: `addons/l10n_in_edi/wizard/l10n_in_edi_cancel_views.xml:6`, `addons/l10n_in_edi/wizard/l10n_in_edi_cancel_views.xml:7`, `addons/l10n_in_edi/views/res_config_settings_views.xml:5`, `addons/l10n_in_edi/views/res_config_settings_views.xml:7`, `addons/l10n_in_edi/views/account_move_views.xml:5`, `addons/l10n_in_edi/views/account_move_views.xml:7`, `addons/l10n_in_edi/views/account_move_views.xml:48`, `addons/l10n_in_edi/views/account_move_views.xml:50`, `addons/l10n_in_edi/views/account_move_views.xml:63`, `addons/l10n_in_edi/views/account_move_views.xml:65`, `addons/l10n_in_edi/views/account_move_views.xml:78`, `addons/l10n_in_edi/views/account_move_views.xml:80`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.partner` (addons/l10n_in_edi/models/res_partner.py:6); inherits `res.config.settings` (addons/l10n_in_edi/models/res_config_settings.py:5); inherits `account.journal` (addons/l10n_in_edi/models/account_journal.py:5); inherits `account.move` (addons/l10n_in_edi/models/account_move.py:25); inherits `account.move.line` (addons/l10n_in_edi/models/account_move_line.py:4); inherits `account.move.send` (addons/l10n_in_edi/models/account_move_send.py:4); inherits `ir.attachment` (addons/l10n_in_edi/models/ir_attachment.py:5); inherits `res.company` (addons/l10n_in_edi/models/res_company.py:9); `l10n_in_edi.cancel` (addons/l10n_in_edi/wizard/l10n_in_edi_cancel.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in`
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

- `addons/l10n_in_edi/__init__.py`
- `addons/l10n_in_edi/__manifest__.py`
- `addons/l10n_in_edi/data/neutralize.sql`
- `addons/l10n_in_edi/demo/demo_company.xml`
- `addons/l10n_in_edi/i18n/hi.po`
- `addons/l10n_in_edi/i18n/l10n_in_edi.pot`
- `addons/l10n_in_edi/models/__init__.py`
- `addons/l10n_in_edi/models/account_journal.py`
- `addons/l10n_in_edi/models/account_move.py`
- `addons/l10n_in_edi/models/account_move_line.py`
- `addons/l10n_in_edi/models/account_move_send.py`
- `addons/l10n_in_edi/models/ir_attachment.py`
- `addons/l10n_in_edi/models/res_company.py`
- `addons/l10n_in_edi/models/res_config_settings.py`
- `addons/l10n_in_edi/models/res_partner.py`
- `addons/l10n_in_edi/security/ir.access.csv`
- `addons/l10n_in_edi/tests/__init__.py`
- `addons/l10n_in_edi/tests/test_edi_json.py`
- `addons/l10n_in_edi/views/account_journal_dashboard_views.xml`
- `addons/l10n_in_edi/views/account_move_views.xml`
- `addons/l10n_in_edi/views/edi_pdf_report.xml`
- `addons/l10n_in_edi/views/res_config_settings_views.xml`
- `addons/l10n_in_edi/wizard/__init__.py`
- `addons/l10n_in_edi/wizard/l10n_in_edi_cancel.py`
- `addons/l10n_in_edi/wizard/l10n_in_edi_cancel_views.xml`
