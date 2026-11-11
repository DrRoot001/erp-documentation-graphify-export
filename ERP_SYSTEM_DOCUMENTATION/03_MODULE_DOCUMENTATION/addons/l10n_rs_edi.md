# Module: l10n_rs_edi

- **Module ID:** MOD-308
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_rs_edi`
- **Manifest:** `addons/l10n_rs_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-Invoice implementation for Serbia

**Manifest description:**

eFaktura E-invoice implementation for Serbia

**Scope evidence:** The module contains 21 files, including 13 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_ubl_cii`, `l10n_rs`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 5
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

- **Description:** 7 model declarations, 24 methods, 2 constraint handlers, 1 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_rs_edi/models/res_partner.py:5`, `addons/l10n_rs_edi/models/res_config_settings.py:4`, `addons/l10n_rs_edi/models/account_move.py:12`, `addons/l10n_rs_edi/models/account_edi_xml_ubl_21_rs.py:5`, `addons/l10n_rs_edi/models/account_move_send.py:4`, `addons/l10n_rs_edi/models/res_company.py:4`, `addons/l10n_rs_edi/wizard/account_move_send_wizard.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/l10n_rs_edi/views/res_config_settings_views.xml:3`, `addons/l10n_rs_edi/views/account_move.xml:4`, `addons/l10n_rs_edi/views/res_partner_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_rs_edi/tests/test_xml_ubl_rs.py`, `addons/l10n_rs_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `res_config_settings_view_form`, `view_move_form`, `res_partner_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_rs_edi/views/res_config_settings_views.xml:5`, `addons/l10n_rs_edi/views/res_config_settings_views.xml:7`, `addons/l10n_rs_edi/views/account_move.xml:6`, `addons/l10n_rs_edi/views/account_move.xml:8`, `addons/l10n_rs_edi/views/res_partner_views.xml:5`, `addons/l10n_rs_edi/views/res_partner_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_rs_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.partner` (addons/l10n_rs_edi/models/res_partner.py:5); inherits `res.config.settings` (addons/l10n_rs_edi/models/res_config_settings.py:4); inherits `account.move` (addons/l10n_rs_edi/models/account_move.py:12); `account.edi.xml.ubl.rs` (addons/l10n_rs_edi/models/account_edi_xml_ubl_21_rs.py:5); inherits `account.move.send` (addons/l10n_rs_edi/models/account_move_send.py:4); inherits `res.company` (addons/l10n_rs_edi/models/res_company.py:4); inherits `account.move.send.wizard` (addons/l10n_rs_edi/wizard/account_move_send_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_ubl_cii`, `l10n_rs`
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

- `addons/l10n_rs_edi/__init__.py`
- `addons/l10n_rs_edi/__manifest__.py`
- `addons/l10n_rs_edi/data/neutralize.sql`
- `addons/l10n_rs_edi/i18n/l10n_rs_edi.pot`
- `addons/l10n_rs_edi/i18n/sr@latin.po`
- `addons/l10n_rs_edi/models/__init__.py`
- `addons/l10n_rs_edi/models/account_edi_xml_ubl_21_rs.py`
- `addons/l10n_rs_edi/models/account_move.py`
- `addons/l10n_rs_edi/models/account_move_send.py`
- `addons/l10n_rs_edi/models/res_company.py`
- `addons/l10n_rs_edi/models/res_config_settings.py`
- `addons/l10n_rs_edi/models/res_partner.py`
- `addons/l10n_rs_edi/tests/__init__.py`
- `addons/l10n_rs_edi/tests/test_files/export_credit_note.xml`
- `addons/l10n_rs_edi/tests/test_files/export_invoice.xml`
- `addons/l10n_rs_edi/tests/test_xml_ubl_rs.py`
- `addons/l10n_rs_edi/views/account_move.xml`
- `addons/l10n_rs_edi/views/res_config_settings_views.xml`
- `addons/l10n_rs_edi/views/res_partner_views.xml`
- `addons/l10n_rs_edi/wizard/__init__.py`
- `addons/l10n_rs_edi/wizard/account_move_send_wizard.py`
