# Module: l10n_eg_edi_eta

- **Module ID:** MOD-172
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_eg_edi_eta`
- **Manifest:** `addons/l10n_eg_edi_eta/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `account`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Egypt Tax Authority Invoice Integration

**Manifest description:**

Egypt Tax Authority Invoice Integration
==============================================================================
Integrates with the ETA portal to automatically send and sign the Invoices to the Tax Authority.

**Scope evidence:** The module contains 43 files, including 24 Python, 11 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_eg`.

## 2. Module structure

- Model/business logic files: 16
- Controller/API files: 0
- XML/data/view/template files: 11
- Browser asset files: 1
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_eg_edi_eta/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 16 model declarations, 90 methods, 0 constraint handlers, 1 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/l10n_eg_edi_eta/models/res_partner.py:4`, `addons/l10n_eg_edi_eta/models/res_currency_rate.py:5`, `addons/l10n_eg_edi_eta/models/uom_uom.py:4`, `addons/l10n_eg_edi_eta/models/uom_uom.py:12`, `addons/l10n_eg_edi_eta/models/product_template.py:5`, `addons/l10n_eg_edi_eta/models/product_template.py:49`, `addons/l10n_eg_edi_eta/models/res_config_settings.py:4`, `addons/l10n_eg_edi_eta/models/eta_thumb_drive.py:13`, `addons/l10n_eg_edi_eta/models/account_journal.py:4`, `addons/l10n_eg_edi_eta/models/eta_submission.py:13`, `addons/l10n_eg_edi_eta/models/eta_activity_type.py:4`, `addons/l10n_eg_edi_eta/models/account_move.py:24`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 1 JavaScript/TypeScript files; static XML analysis found 22 record/template/menu identifiers.
- **Evidence:** `addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.xml:4`, `addons/l10n_eg_edi_eta/data/res_country_data.xml:3`, `addons/l10n_eg_edi_eta/data/res_country_data.xml:27`, `addons/l10n_eg_edi_eta/views/uom_uom_view.xml:3`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:3`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:18`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:24`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:25`, `addons/l10n_eg_edi_eta/views/report_invoice.xml:3`, `addons/l10n_eg_edi_eta/views/account_move_view.xml:3`, `addons/l10n_eg_edi_eta/views/account_move_view.xml:44`, `addons/l10n_eg_edi_eta/views/account_move_view.xml:66`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_eg_edi_eta/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_eg_edi_eta/views/account_move_view.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_eg_edi_eta/tests/test_edi_json.py`, `addons/l10n_eg_edi_eta/tests/common.py`, `addons/l10n_eg_edi_eta/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `l10n_eg_edi_cancel_wizard_form`, `eg_partner_address_form`, `base.eg`, `uom_uom_view_form`, `view_l10n_eg_edi_thumb_drive_tree`, `action_eta_thumb_drive_tree`, `ETA`, `menu_action_eta_thumb_drive_tree`, `egyptian_invoice`, `view_move_form_inherit`, `l10n_eg_edi_view_out_invoice_tree_inherit`, `l10n_eg_edi_view_out_credit_note_tree_inherit`, `l10n_eg_edi_view_account_invoice_filter`, `action_l10n_eg_get_invoice_pdf`, `action_l10n_eg_sign_invoices`, `view_company_form_inherit_l10n_eg_edi`, `product_template_only_form_view_inherit_l10n_eg_eta_edi`, `product_normal_form_view_inherit_l10n_eg_eta_edi`, `view_account_journal_form_inherit_l10n_eg_edi`, `res_config_settings_view_form`
- Menus: 2; representative evidence: `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:24`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:25`
- Templates: 1; representative evidence: `addons/l10n_eg_edi_eta/views/report_invoice.xml:3`
- View/action field declarations: 32; representative evidence: `addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.xml:6`, `addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.xml:7`, `addons/l10n_eg_edi_eta/data/res_country_data.xml:5`, `addons/l10n_eg_edi_eta/data/res_country_data.xml:7`, `addons/l10n_eg_edi_eta/views/uom_uom_view.xml:5`, `addons/l10n_eg_edi_eta/views/uom_uom_view.xml:7`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:5`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:6`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:20`, `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml:21`, `addons/l10n_eg_edi_eta/views/account_move_view.xml:5`, `addons/l10n_eg_edi_eta/views/account_move_view.xml:8`
- Browser assets: 1; representative files: `addons/l10n_eg_edi_eta/static/src/client_action/sign_invoice.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_eg_edi_eta/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_eg_edi_eta/views/account_move_view.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 16
- Representative model evidence: inherits `res.partner` (addons/l10n_eg_edi_eta/models/res_partner.py:4); inherits `res.currency.rate` (addons/l10n_eg_edi_eta/models/res_currency_rate.py:5); `l10n_eg_edi.uom.code` (addons/l10n_eg_edi_eta/models/uom_uom.py:4); inherits `uom.uom` (addons/l10n_eg_edi_eta/models/uom_uom.py:12); inherits `product.template` (addons/l10n_eg_edi_eta/models/product_template.py:5); inherits `product.product` (addons/l10n_eg_edi_eta/models/product_template.py:49); inherits `res.config.settings` (addons/l10n_eg_edi_eta/models/res_config_settings.py:4); `l10n_eg_edi.thumb.drive` (addons/l10n_eg_edi_eta/models/eta_thumb_drive.py:13); inherits `account.journal` (addons/l10n_eg_edi_eta/models/account_journal.py:4); `l10n_eg_edi.eta.submission` (addons/l10n_eg_edi_eta/models/eta_submission.py:13); `l10n_eg_edi.activity.type` (addons/l10n_eg_edi_eta/models/eta_activity_type.py:4); inherits `account.move` (addons/l10n_eg_edi_eta/models/account_move.py:24); inherits `account.move.send` (addons/l10n_eg_edi_eta/models/account_move_send.py:4); inherits `ir.attachment` (addons/l10n_eg_edi_eta/models/ir_attachment.py:5); inherits `res.company` (addons/l10n_eg_edi_eta/models/res_company.py:4); `l10n_eg_edi.cancel.wizard` (addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_eg`
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

- `addons/l10n_eg_edi_eta/__init__.py`
- `addons/l10n_eg_edi_eta/__manifest__.py`
- `addons/l10n_eg_edi_eta/data/l10n_eg_edi.activity.type.csv`
- `addons/l10n_eg_edi_eta/data/l10n_eg_edi.uom.code.csv`
- `addons/l10n_eg_edi_eta/data/neutralize.sql`
- `addons/l10n_eg_edi_eta/data/res_country_data.xml`
- `addons/l10n_eg_edi_eta/data/uom.uom.csv`
- `addons/l10n_eg_edi_eta/i18n/ar.po`
- `addons/l10n_eg_edi_eta/i18n/l10n_eg_edi_eta.pot`
- `addons/l10n_eg_edi_eta/lib/eta_client.py`
- `addons/l10n_eg_edi_eta/models/__init__.py`
- `addons/l10n_eg_edi_eta/models/account_journal.py`
- `addons/l10n_eg_edi_eta/models/account_move.py`
- `addons/l10n_eg_edi_eta/models/account_move_send.py`
- `addons/l10n_eg_edi_eta/models/eta_activity_type.py`
- `addons/l10n_eg_edi_eta/models/eta_submission.py`
- `addons/l10n_eg_edi_eta/models/eta_thumb_drive.py`
- `addons/l10n_eg_edi_eta/models/ir_attachment.py`
- `addons/l10n_eg_edi_eta/models/product_template.py`
- `addons/l10n_eg_edi_eta/models/res_company.py`
- `addons/l10n_eg_edi_eta/models/res_config_settings.py`
- `addons/l10n_eg_edi_eta/models/res_currency_rate.py`
- `addons/l10n_eg_edi_eta/models/res_partner.py`
- `addons/l10n_eg_edi_eta/models/uom_uom.py`
- `addons/l10n_eg_edi_eta/security/ir.access.csv`
- `addons/l10n_eg_edi_eta/static/src/client_action/sign_invoice.js`
- `addons/l10n_eg_edi_eta/tests/__init__.py`
- `addons/l10n_eg_edi_eta/tests/common.py`
- `addons/l10n_eg_edi_eta/tests/test_edi_json.py`
- `addons/l10n_eg_edi_eta/tools/__init__.py`
- `addons/l10n_eg_edi_eta/tools/eta_serialize.py`
- `addons/l10n_eg_edi_eta/views/account_journal_view.xml`
- `addons/l10n_eg_edi_eta/views/account_move_view.xml`
- `addons/l10n_eg_edi_eta/views/eta_thumb_drive.xml`
- `addons/l10n_eg_edi_eta/views/l10n_eg_edi_activity_type_view.xml`
- `addons/l10n_eg_edi_eta/views/product_template_views.xml`
- `addons/l10n_eg_edi_eta/views/report_invoice.xml`
- `addons/l10n_eg_edi_eta/views/res_company_view.xml`
- `addons/l10n_eg_edi_eta/views/res_config_settings_view.xml`
- `addons/l10n_eg_edi_eta/views/uom_uom_view.xml`
- `addons/l10n_eg_edi_eta/wizards/__init__.py`
- `addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.py`
- `addons/l10n_eg_edi_eta/wizards/l10n_eg_edi_cancel_wizard.xml`
