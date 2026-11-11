# Module: l10n_ro_edi

- **Module ID:** MOD-305
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ro_edi`
- **Manifest:** `addons/l10n_ro_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-Invoice implementation for Romania

**Manifest description:**

E-invoice implementation for Romania

**Scope evidence:** The module contains 43 files, including 22 Python, 15 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_ubl_cii`, `l10n_ro`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 2
- XML/data/view/template files: 15
- Browser asset files: 1
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ro_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 87 methods, 1 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/l10n_ro_edi/models/res_partner.py:7`, `addons/l10n_ro_edi/models/res_config_settings.py:4`, `addons/l10n_ro_edi/models/cpv_code.py:4`, `addons/l10n_ro_edi/models/product.py:4`, `addons/l10n_ro_edi/models/ciusro_document.py:4`, `addons/l10n_ro_edi/models/account_move.py:20`, `addons/l10n_ro_edi/models/account_edi_xml_ubl_ciusro.py:26`, `addons/l10n_ro_edi/models/account_move_send.py:4`, `addons/l10n_ro_edi/models/res_company.py:13`, `addons/l10n_ro_edi/wizard/account_move_send_wizard.py:4`, `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/l10n_ro_edi/controllers/main.py:18`, `addons/l10n_ro_edi/controllers/main.py:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 1 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.xml:4`, `addons/l10n_ro_edi/data/ir_cron.xml:4`, `addons/l10n_ro_edi/data/ir_cron.xml:14`, `addons/l10n_ro_edi/views/res_config_settings_views.xml:3`, `addons/l10n_ro_edi/views/account_move_views.xml:4`, `addons/l10n_ro_edi/views/account_move_views.xml:50`, `addons/l10n_ro_edi/views/account_move_views.xml:61`, `addons/l10n_ro_edi/views/account_move_views.xml:72`, `addons/l10n_ro_edi/views/account_move_views.xml:83`, `addons/l10n_ro_edi/views/account_move_views.xml:106`, `addons/l10n_ro_edi/views/product_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ro_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_ro_edi/__manifest__.py`, `addons/l10n_ro_edi/models/res_company.py`, `addons/l10n_ro_edi/data/ir_cron.xml`, `addons/l10n_ro_edi/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_ro_edi/tests/test_ro_edi.py`, `addons/l10n_ro_edi/tests/test_xml_ubl_ro.py`, `addons/l10n_ro_edi/tests/common.py`, `addons/l10n_ro_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `account_move_fetch_invoices_wizard_form`, `ir_cron_l10n_ro_edi_refresh_access_token`, `ir_cron_l10n_ro_edi_synchronize_invoices`, `res_config_settings_form_inherit_l10n_ro_edi`, `account_move_form_inherit_l10n_ro_edi`, `out_invoice_tree_inherit_l10n_ro_edi`, `out_credit_note_tree_inherit_l10n_ro_edi`, `in_invoice_tree_inherit_l10n_ro_edi`, `l10n_ro_edi_view_account_invoice_filter`, `l10n_ro_edi_action_fetch_ciusro_status`, `product_template_form_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 16; representative evidence: `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.xml:6`, `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.xml:7`, `addons/l10n_ro_edi/views/res_config_settings_views.xml:5`, `addons/l10n_ro_edi/views/res_config_settings_views.xml:7`, `addons/l10n_ro_edi/views/account_move_views.xml:6`, `addons/l10n_ro_edi/views/account_move_views.xml:9`, `addons/l10n_ro_edi/views/account_move_views.xml:52`, `addons/l10n_ro_edi/views/account_move_views.xml:54`, `addons/l10n_ro_edi/views/account_move_views.xml:63`, `addons/l10n_ro_edi/views/account_move_views.xml:65`, `addons/l10n_ro_edi/views/account_move_views.xml:74`, `addons/l10n_ro_edi/views/account_move_views.xml:76`
- Browser assets: 1; representative files: `addons/l10n_ro_edi/static/src/components/fetch_invoices.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ro_edi/__manifest__.py`
- **HTTP entry points:** `addons/l10n_ro_edi/controllers/main.py:18`, `addons/l10n_ro_edi/controllers/main.py:34`
- **Scheduled entry points:** `addons/l10n_ro_edi/__manifest__.py`, `addons/l10n_ro_edi/models/res_company.py`, `addons/l10n_ro_edi/data/ir_cron.xml`, `addons/l10n_ro_edi/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `res.partner` (addons/l10n_ro_edi/models/res_partner.py:7); inherits `res.config.settings` (addons/l10n_ro_edi/models/res_config_settings.py:4); `l10n_ro.cpv.code` (addons/l10n_ro_edi/models/cpv_code.py:4); inherits `product.template` (addons/l10n_ro_edi/models/product.py:4); `l10n_ro_edi.document` (addons/l10n_ro_edi/models/ciusro_document.py:4); inherits `account.move` (addons/l10n_ro_edi/models/account_move.py:20); `account.edi.xml.ubl_ro` (addons/l10n_ro_edi/models/account_edi_xml_ubl_ciusro.py:26); inherits `account.move.send` (addons/l10n_ro_edi/models/account_move_send.py:4); inherits `res.company` (addons/l10n_ro_edi/models/res_company.py:13); inherits `account.move.send.wizard` (addons/l10n_ro_edi/wizard/account_move_send_wizard.py:4); `l10n_ro_edi.account_move_fetch_invoices.wizard` (addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/l10n_ro_edi/controllers/main.py:18`, `addons/l10n_ro_edi/controllers/main.py:34`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_ubl_cii`, `l10n_ro`
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

- `addons/l10n_ro_edi/__init__.py`
- `addons/l10n_ro_edi/__manifest__.py`
- `addons/l10n_ro_edi/controllers/__init__.py`
- `addons/l10n_ro_edi/controllers/main.py`
- `addons/l10n_ro_edi/data/ir_cron.xml`
- `addons/l10n_ro_edi/data/l10n_ro.cpv.code.csv`
- `addons/l10n_ro_edi/data/neutralize.sql`
- `addons/l10n_ro_edi/i18n/l10n_ro_edi.pot`
- `addons/l10n_ro_edi/i18n/ro.po`
- `addons/l10n_ro_edi/models/__init__.py`
- `addons/l10n_ro_edi/models/account_edi_xml_ubl_ciusro.py`
- `addons/l10n_ro_edi/models/account_move.py`
- `addons/l10n_ro_edi/models/account_move_send.py`
- `addons/l10n_ro_edi/models/ciusro_document.py`
- `addons/l10n_ro_edi/models/cpv_code.py`
- `addons/l10n_ro_edi/models/product.py`
- `addons/l10n_ro_edi/models/res_company.py`
- `addons/l10n_ro_edi/models/res_config_settings.py`
- `addons/l10n_ro_edi/models/res_partner.py`
- `addons/l10n_ro_edi/models/utils.py`
- `addons/l10n_ro_edi/security/ir.access.csv`
- `addons/l10n_ro_edi/static/src/components/fetch_invoices.js`
- `addons/l10n_ro_edi/static/src/components/fetch_invoices.xml`
- `addons/l10n_ro_edi/tests/__init__.py`
- `addons/l10n_ro_edi/tests/common.py`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_in_invoice.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_characters_limit.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_cpv_code.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_defaults.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_different_currency.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_no_prefix_company_registry.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_invoice_no_prefix_vat.xml`
- `addons/l10n_ro_edi/tests/test_files/from_odoo/ciusro_out_refund.xml`
- `addons/l10n_ro_edi/tests/test_ro_edi.py`
- `addons/l10n_ro_edi/tests/test_xml_ubl_ro.py`
- `addons/l10n_ro_edi/views/account_move_views.xml`
- `addons/l10n_ro_edi/views/product_views.xml`
- `addons/l10n_ro_edi/views/res_config_settings_views.xml`
- `addons/l10n_ro_edi/wizard/__init__.py`
- `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.py`
- `addons/l10n_ro_edi/wizard/account_move_fetch_invoices_wizard.xml`
- `addons/l10n_ro_edi/wizard/account_move_send_wizard.py`
