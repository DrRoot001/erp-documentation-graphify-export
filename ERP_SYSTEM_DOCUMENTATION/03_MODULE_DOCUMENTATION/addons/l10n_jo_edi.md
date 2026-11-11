# Module: l10n_jo_edi

- **Module ID:** MOD-246
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_jo_edi`
- **Manifest:** `addons/l10n_jo_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Electronic Invoicing for Jordan UBL 2.1

**Manifest description:**

Allows the users to integrate with JoFotara.

**Scope evidence:** The module contains 33 files, including 15 Python, 14 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_ubl_cii`, `l10n_jo`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 14
- Browser asset files: 1
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 96 methods, 0 constraint handlers, 0 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/l10n_jo_edi/models/res_config_settings.py:4`, `addons/l10n_jo_edi/models/account_tax.py:4`, `addons/l10n_jo_edi/models/account_edi_xml_ubl_21_jo.py:20`, `addons/l10n_jo_edi/models/account_move.py:9`, `addons/l10n_jo_edi/models/account_move_send.py:15`, `addons/l10n_jo_edi/models/ir_attachment.py:5`, `addons/l10n_jo_edi/models/res_company.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 1 JavaScript/TypeScript files; static XML analysis found 17 record/template/menu identifiers.
- **Evidence:** `addons/l10n_jo_edi/demo/demo_company.xml:4`, `addons/l10n_jo_edi/views/report_templates.xml:4`, `addons/l10n_jo_edi/views/report_templates.xml:9`, `addons/l10n_jo_edi/views/report_templates.xml:14`, `addons/l10n_jo_edi/views/report_templates.xml:19`, `addons/l10n_jo_edi/views/report_templates.xml:24`, `addons/l10n_jo_edi/views/report_templates.xml:29`, `addons/l10n_jo_edi/views/report_templates.xml:34`, `addons/l10n_jo_edi/views/report_templates.xml:39`, `addons/l10n_jo_edi/views/res_config_settings_views.xml:4`, `addons/l10n_jo_edi/views/report_invoice.xml:3`, `addons/l10n_jo_edi/views/report_invoice.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_jo_edi/tests/jo_edi_common.py`, `addons/l10n_jo_edi/tests/test_jo_edi_invoice_codes.py`, `addons/l10n_jo_edi/tests/test_jo_edi_types.py`, `addons/l10n_jo_edi/tests/test_jo_edi_precision.py`, `addons/l10n_jo_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `base.demo_company_jo`, `l10n_jo_edi_external_layout_standard`, `l10n_jo_edi_external_layout_wave`, `l10n_jo_edi_external_layout_bubble`, `l10n_jo_edi_external_layout_folder`, `l10n_jo_edi_external_layout_center`, `l10n_jo_edi_external_layout_dual`, `l10n_jo_edi_external_layout_lines`, `l10n_jo_edi_external_layout_compact`, `res_config_settings_view_form`, `report_invoice_document_jo_header`, `report_invoice_document`, `report_invoice`, `view_move_form`, `view_out_invoice_tree`, `view_out_credit_note_tree`, `view_account_invoice_filter`
- Menus: 0; representative evidence: Not found in module
- Templates: 11; representative evidence: `addons/l10n_jo_edi/views/report_templates.xml:4`, `addons/l10n_jo_edi/views/report_templates.xml:9`, `addons/l10n_jo_edi/views/report_templates.xml:14`, `addons/l10n_jo_edi/views/report_templates.xml:19`, `addons/l10n_jo_edi/views/report_templates.xml:24`, `addons/l10n_jo_edi/views/report_templates.xml:29`, `addons/l10n_jo_edi/views/report_templates.xml:34`, `addons/l10n_jo_edi/views/report_templates.xml:39`, `addons/l10n_jo_edi/views/report_invoice.xml:3`, `addons/l10n_jo_edi/views/report_invoice.xml:14`, `addons/l10n_jo_edi/views/report_invoice.xml:27`
- View/action field declarations: 10; representative evidence: `addons/l10n_jo_edi/views/res_config_settings_views.xml:6`, `addons/l10n_jo_edi/views/res_config_settings_views.xml:8`, `addons/l10n_jo_edi/views/account_move_views.xml:6`, `addons/l10n_jo_edi/views/account_move_views.xml:8`, `addons/l10n_jo_edi/views/account_move_views.xml:36`, `addons/l10n_jo_edi/views/account_move_views.xml:38`, `addons/l10n_jo_edi/views/account_move_views.xml:49`, `addons/l10n_jo_edi/views/account_move_views.xml:51`, `addons/l10n_jo_edi/views/account_move_views.xml:62`, `addons/l10n_jo_edi/views/account_move_views.xml:64`
- Browser assets: 1; representative files: `addons/l10n_jo_edi/static/src/jo_edi_error_dialog/jo_edi_error_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_jo_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.config.settings` (addons/l10n_jo_edi/models/res_config_settings.py:4); inherits `account.tax` (addons/l10n_jo_edi/models/account_tax.py:4); `account.edi.xml.ubl_21.jo` (addons/l10n_jo_edi/models/account_edi_xml_ubl_21_jo.py:20); inherits `account.move` (addons/l10n_jo_edi/models/account_move.py:9); inherits `account.move.send` (addons/l10n_jo_edi/models/account_move_send.py:15); inherits `ir.attachment` (addons/l10n_jo_edi/models/ir_attachment.py:5); inherits `res.company` (addons/l10n_jo_edi/models/res_company.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_ubl_cii`, `l10n_jo`
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

- `addons/l10n_jo_edi/__init__.py`
- `addons/l10n_jo_edi/__manifest__.py`
- `addons/l10n_jo_edi/data/neutralize.sql`
- `addons/l10n_jo_edi/demo/demo_company.xml`
- `addons/l10n_jo_edi/i18n/ar.po`
- `addons/l10n_jo_edi/i18n/l10n_jo_edi.pot`
- `addons/l10n_jo_edi/models/__init__.py`
- `addons/l10n_jo_edi/models/account_edi_xml_ubl_21_jo.py`
- `addons/l10n_jo_edi/models/account_move.py`
- `addons/l10n_jo_edi/models/account_move_send.py`
- `addons/l10n_jo_edi/models/account_tax.py`
- `addons/l10n_jo_edi/models/ir_attachment.py`
- `addons/l10n_jo_edi/models/res_company.py`
- `addons/l10n_jo_edi/models/res_config_settings.py`
- `addons/l10n_jo_edi/static/src/jo_edi_error_dialog/jo_edi_error_dialog.js`
- `addons/l10n_jo_edi/static/src/jo_edi_error_dialog/jo_edi_error_dialog.xml`
- `addons/l10n_jo_edi/tests/__init__.py`
- `addons/l10n_jo_edi/tests/jo_edi_common.py`
- `addons/l10n_jo_edi/tests/test_files/type_1.xml`
- `addons/l10n_jo_edi/tests/test_files/type_2.xml`
- `addons/l10n_jo_edi/tests/test_files/type_3.xml`
- `addons/l10n_jo_edi/tests/test_files/type_4.xml`
- `addons/l10n_jo_edi/tests/test_files/type_5.xml`
- `addons/l10n_jo_edi/tests/test_files/type_6.xml`
- `addons/l10n_jo_edi/tests/test_files/type_7.xml`
- `addons/l10n_jo_edi/tests/test_files/type_8.xml`
- `addons/l10n_jo_edi/tests/test_jo_edi_invoice_codes.py`
- `addons/l10n_jo_edi/tests/test_jo_edi_precision.py`
- `addons/l10n_jo_edi/tests/test_jo_edi_types.py`
- `addons/l10n_jo_edi/views/account_move_views.xml`
- `addons/l10n_jo_edi/views/report_invoice.xml`
- `addons/l10n_jo_edi/views/report_templates.xml`
- `addons/l10n_jo_edi/views/res_config_settings_views.xml`
