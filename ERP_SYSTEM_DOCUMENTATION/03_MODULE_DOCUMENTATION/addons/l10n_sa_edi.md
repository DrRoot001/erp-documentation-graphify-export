# Module: l10n_sa_edi

- **Module ID:** MOD-311
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sa_edi`
- **Manifest:** `addons/l10n_sa_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-Invoicing, Universal Business Language

**Manifest description:**

E-invoice implementation for Saudi Arabia; Integration with ZATCA

**Scope evidence:** The module contains 63 files, including 32 Python, 23 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account_edi_ubl_cii`, `l10n_sa`, `certificate`.

## 2. Module structure

- Model/business logic files: 19
- Controller/API files: 2
- XML/data/view/template files: 23
- Browser asset files: 1
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_sa_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 19 model declarations, 209 methods, 0 constraint handlers, 0 onchange handlers, and 10 dependency declarations.
- **Evidence:** `addons/l10n_sa_edi/demo/account_demo.py:5`, `addons/l10n_sa_edi/models/res_partner.py:4`, `addons/l10n_sa_edi/models/res_config_settings.py:4`, `addons/l10n_sa_edi/models/account_edi_xml_ubl_21_zatca.py:4`, `addons/l10n_sa_edi/models/account_journal.py:44`, `addons/l10n_sa_edi/models/account_tax.py:25`, `addons/l10n_sa_edi/models/account_chart_template.py:5`, `addons/l10n_sa_edi/models/l10n_sa_edi_document.py:25`, `addons/l10n_sa_edi/models/certificate.py:20`, `addons/l10n_sa_edi/models/account_move.py:10`, `addons/l10n_sa_edi/models/account_move.py:312`, `addons/l10n_sa_edi/models/zatca_mixin.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_sa_edi/controllers/portal.py`, `addons/l10n_sa_edi/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 23 XML files and 1 JavaScript/TypeScript files; static XML analysis found 19 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:4`, `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:23`, `addons/l10n_sa_edi/data/res_country_data.xml:3`, `addons/l10n_sa_edi/data/res_country_data.xml:34`, `addons/l10n_sa_edi/data/ubl_21_zatca.xml:4`, `addons/l10n_sa_edi/data/ubl_21_zatca.xml:92`, `addons/l10n_sa_edi/data/transaction_type_data.xml:3`, `addons/l10n_sa_edi/data/transaction_type_data.xml:7`, `addons/l10n_sa_edi/data/transaction_type_data.xml:11`, `addons/l10n_sa_edi/views/report_templates.xml:3`, `addons/l10n_sa_edi/views/report_invoice.xml:4`, `addons/l10n_sa_edi/views/res_company_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_sa_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_sa_edi/tests/test_invoice.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/l10n_sa_edi/tests/common.py`, `addons/l10n_sa_edi/tests/__init__.py`, `addons/l10n_sa_edi/tests/test_sa_edi_additional_identifiers.py`, `addons/l10n_sa_edi/tests/test_edi_zatca.py`, `addons/l10n_sa_edi/tests/test_account_move_send.py`, `addons/l10n_sa_edi/tests/test_invoice.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 23; representative identifiers: `l10n_sa_edi_otp_wizard_view_form`, `l10n_sa_edi_otp_wizard_act_window`, `sa_partner_address_form`, `base.sa`, `export_sa_zatca_ubl_extensions`, `export_sa_zatca_ubl_signed_properties`, `transaction_type_nominal`, `transaction_type_export`, `transaction_type_summary`, `l10n_sa_edi_company_address_list`, `l10n_sa_edi_report_invoice_document`, `view_company_form`, `view_move_form`, `view_invoice_tree`, `view_account_invoice_filter`, `address_form_fields`, `view_tax_form`, `res_config_settings_view_form`, `view_account_journal_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 5; representative evidence: `addons/l10n_sa_edi/data/ubl_21_zatca.xml:4`, `addons/l10n_sa_edi/data/ubl_21_zatca.xml:92`, `addons/l10n_sa_edi/views/report_templates.xml:3`, `addons/l10n_sa_edi/views/report_invoice.xml:4`, `addons/l10n_sa_edi/views/portal_address_templates.xml:4`
- View/action field declarations: 20; representative evidence: `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:6`, `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:7`, `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:25`, `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml:26`, `addons/l10n_sa_edi/data/res_country_data.xml:5`, `addons/l10n_sa_edi/data/res_country_data.xml:7`, `addons/l10n_sa_edi/views/res_company_views.xml:6`, `addons/l10n_sa_edi/views/res_company_views.xml:8`, `addons/l10n_sa_edi/views/account_move_views.xml:6`, `addons/l10n_sa_edi/views/account_move_views.xml:8`, `addons/l10n_sa_edi/views/account_move_views.xml:55`, `addons/l10n_sa_edi/views/account_move_views.xml:57`
- Browser assets: 1; representative files: `addons/l10n_sa_edi/static/src/interactions/address.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sa_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_sa_edi/tests/test_invoice.py`

## 7. Database interactions

- Model declarations: 19
- Representative model evidence: inherits `account.chart.template` (addons/l10n_sa_edi/demo/account_demo.py:5); inherits `res.partner` (addons/l10n_sa_edi/models/res_partner.py:4); inherits `res.config.settings` (addons/l10n_sa_edi/models/res_config_settings.py:4); `account.edi.xml.ubl_21.zatca` (addons/l10n_sa_edi/models/account_edi_xml_ubl_21_zatca.py:4); inherits `account.journal` (addons/l10n_sa_edi/models/account_journal.py:44); inherits `account.tax` (addons/l10n_sa_edi/models/account_tax.py:25); inherits `account.chart.template` (addons/l10n_sa_edi/models/account_chart_template.py:5); `l10n_sa_edi.document` (addons/l10n_sa_edi/models/l10n_sa_edi_document.py:25); inherits `certificate.certificate` (addons/l10n_sa_edi/models/certificate.py:20); inherits `account.move` (addons/l10n_sa_edi/models/account_move.py:10); inherits `account.move.line` (addons/l10n_sa_edi/models/account_move.py:312); inherits `zatca.mixin` (addons/l10n_sa_edi/models/zatca_mixin.py:4); inherits `account.move.send` (addons/l10n_sa_edi/models/account_move_send.py:11); `zatca.ubl.mixin` (addons/l10n_sa_edi/models/zatca_ubl_mixin.py:30); `l10n_sa_edi.transaction.type` (addons/l10n_sa_edi/models/l10n_sa_edi_transaction_type.py:4); inherits `ir.attachment` (addons/l10n_sa_edi/models/ir_attachment.py:5); `l10n_sa_edi.log` (addons/l10n_sa_edi/models/l10n_sa_edi_log.py:6); inherits `res.company` (addons/l10n_sa_edi/models/res_company.py:6); `l10n_sa_edi.otp.wizard` (addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_edi_ubl_cii`, `l10n_sa`, `certificate`
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

- `addons/l10n_sa_edi/__init__.py`
- `addons/l10n_sa_edi/__manifest__.py`
- `addons/l10n_sa_edi/controllers/__init__.py`
- `addons/l10n_sa_edi/controllers/portal.py`
- `addons/l10n_sa_edi/data/neutralize.sql`
- `addons/l10n_sa_edi/data/pre-hash_invoice.xsl`
- `addons/l10n_sa_edi/data/res_country_data.xml`
- `addons/l10n_sa_edi/data/template/account.tax-sa.csv`
- `addons/l10n_sa_edi/data/transaction_type_data.xml`
- `addons/l10n_sa_edi/data/ubl_21_zatca.xml`
- `addons/l10n_sa_edi/demo/__init__.py`
- `addons/l10n_sa_edi/demo/account_demo.py`
- `addons/l10n_sa_edi/i18n/ar.po`
- `addons/l10n_sa_edi/i18n/l10n_sa_edi.pot`
- `addons/l10n_sa_edi/migrations/0.3/end-migrate.py`
- `addons/l10n_sa_edi/models/__init__.py`
- `addons/l10n_sa_edi/models/account_chart_template.py`
- `addons/l10n_sa_edi/models/account_edi_xml_ubl_21_zatca.py`
- `addons/l10n_sa_edi/models/account_journal.py`
- `addons/l10n_sa_edi/models/account_move.py`
- `addons/l10n_sa_edi/models/account_move_send.py`
- `addons/l10n_sa_edi/models/account_tax.py`
- `addons/l10n_sa_edi/models/certificate.py`
- `addons/l10n_sa_edi/models/ir_attachment.py`
- `addons/l10n_sa_edi/models/l10n_sa_edi_document.py`
- `addons/l10n_sa_edi/models/l10n_sa_edi_log.py`
- `addons/l10n_sa_edi/models/l10n_sa_edi_transaction_type.py`
- `addons/l10n_sa_edi/models/res_company.py`
- `addons/l10n_sa_edi/models/res_config_settings.py`
- `addons/l10n_sa_edi/models/res_partner.py`
- `addons/l10n_sa_edi/models/zatca_mixin.py`
- `addons/l10n_sa_edi/models/zatca_ubl_mixin.py`
- `addons/l10n_sa_edi/security/ir.access.csv`
- `addons/l10n_sa_edi/static/src/interactions/address.js`
- `addons/l10n_sa_edi/static/src/scss/form_view.scss`
- `addons/l10n_sa_edi/tests/__init__.py`
- `addons/l10n_sa_edi/tests/common.py`
- `addons/l10n_sa_edi/tests/compliance/simplified/credit.xml`
- `addons/l10n_sa_edi/tests/compliance/simplified/debit.xml`
- `addons/l10n_sa_edi/tests/compliance/simplified/invoice.xml`
- `addons/l10n_sa_edi/tests/compliance/standard/credit.xml`
- `addons/l10n_sa_edi/tests/compliance/standard/debit.xml`
- `addons/l10n_sa_edi/tests/compliance/standard/invoice.xml`
- `addons/l10n_sa_edi/tests/test_account_move_send.py`
- `addons/l10n_sa_edi/tests/test_edi_zatca.py`
- `addons/l10n_sa_edi/tests/test_files/downpayment_credit_note.xml`
- `addons/l10n_sa_edi/tests/test_files/downpayment_invoice.xml`
- `addons/l10n_sa_edi/tests/test_files/final_credit_note.xml`
- `addons/l10n_sa_edi/tests/test_files/final_invoice.xml`
- `addons/l10n_sa_edi/tests/test_files/invoice_global_discount.xml`
- `addons/l10n_sa_edi/tests/test_invoice.py`
- `addons/l10n_sa_edi/tests/test_sa_edi_additional_identifiers.py`
- `addons/l10n_sa_edi/views/account_journal_views.xml`
- `addons/l10n_sa_edi/views/account_move_views.xml`
- `addons/l10n_sa_edi/views/account_tax_views.xml`
- `addons/l10n_sa_edi/views/portal_address_templates.xml`
- `addons/l10n_sa_edi/views/report_invoice.xml`
- `addons/l10n_sa_edi/views/report_templates.xml`
- `addons/l10n_sa_edi/views/res_company_views.xml`
- `addons/l10n_sa_edi/views/res_config_settings_view.xml`
- `addons/l10n_sa_edi/wizard/__init__.py`
- `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.py`
- `addons/l10n_sa_edi/wizard/l10n_sa_edi_otp_wizard.xml`
