# Module: l10n_hu_edi

- **Module ID:** MOD-220
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_hu_edi`
- **Manifest:** `addons/l10n_hu_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

* Electronically report invoices to the NAV (Hungarian Tax Agency) when issuing physical (paper) invoices.
* Electronically receive vendor bills from the NAV.
* Perform the Tax Audit Export (Adóhatósági Ellenőrzési Adatszolgáltatás) in NAV 3.0 format.
* NAV Documentation: https://onlineszamla.nav.gov.hu/files/container/download/2025.10.09.%20EN_Online%20Invoice%20System%203.0%20Interface%20Specification%20.pdf

**Scope evidence:** The module contains 98 files, including 29 Python, 57 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account_debit_note`, `l10n_hu`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 0
- XML/data/view/template files: 57
- Browser asset files: 1
- Security files: 1
- Test files: 10
- Scheduled/automation evidence files: 4
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_hu_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 158 methods, 1 constraint handlers, 0 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/l10n_hu_edi/models/template_hu.py:5`, `addons/l10n_hu_edi/models/res_partner.py:6`, `addons/l10n_hu_edi/models/uom_uom.py:6`, `addons/l10n_hu_edi/models/res_config_settings.py:6`, `addons/l10n_hu_edi/models/product.py:6`, `addons/l10n_hu_edi/models/account_tax.py:47`, `addons/l10n_hu_edi/models/account_move.py:22`, `addons/l10n_hu_edi/models/account_move_send.py:8`, `addons/l10n_hu_edi/models/res_company.py:13`, `addons/l10n_hu_edi/wizard/account_move_debit.py:4`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.py:10`, `addons/l10n_hu_edi/wizard/account_move_reversal.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 57 XML files and 1 JavaScript/TypeScript files; static XML analysis found 49 record/template/menu identifiers.
- **Evidence:** `addons/l10n_hu_edi/demo/demo_partner.xml:3`, `addons/l10n_hu_edi/demo/demo_partner.xml:7`, `addons/l10n_hu_edi/demo/demo_partner.xml:21`, `addons/l10n_hu_edi/demo/demo_partner.xml:30`, `addons/l10n_hu_edi/demo/demo_partner.xml:44`, `addons/l10n_hu_edi/demo/demo_partner.xml:52`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:4`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:32`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:40`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:41`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.xml:4`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_hu_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_hu_edi/__manifest__.py`, `addons/l10n_hu_edi/models/account_move.py`, `addons/l10n_hu_edi/models/account_move_send.py`, `addons/l10n_hu_edi/data/ir_cron.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_hu_edi/tests/test_invoice_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/l10n_hu_edi/tests/test_invoice_report.py`, `addons/l10n_hu_edi/tests/test_invoice_xml.py`, `addons/l10n_hu_edi/tests/test_flows_live.py`, `addons/l10n_hu_edi/tests/common.py`, `addons/l10n_hu_edi/tests/test_credit_debit_notes.py`, `addons/l10n_hu_edi/tests/test_account_move_sync_tax_lines.py`, `addons/l10n_hu_edi/tests/test_bill_xml_upload.py`, `addons/l10n_hu_edi/tests/__init__.py`, `addons/l10n_hu_edi/tests/test_flows_mocked.py`, `addons/l10n_hu_edi/tests/test_res_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 57; representative identifiers: `base.partner_demo_company_hu`, `res_partner_hu_01`, `res_partner_hu_address_01`, `res_partner_hu_02`, `res_partner_hu_address_02`, `res_partner_hu_03`, `l10n_hu_edi_tax_audit_export_form`, `action_l10n_hu_edi_tax_audit_export_form`, `Hungary`, `Tax audit export - Adóhatósági Ellenőrzési Adatszolgáltatás`, `l10n_hu_edi_cancellation_form`, `l10n_hu_edi_receive_bills_wizard_form`, `ir_cron_update_status`, `nav_online_invoice_xml_3_0`, `nav_online_invoice_xml_3_0_simple_address`, `nav_online_invoice_xml_3_0_tax_number`, `nav_online_invoice_xml_3_0_vat_rate`, `nav_online_invoice_xml_3_0_line`, `request_header`, `token_exchange_request`
- Menus: 2; representative evidence: `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:40`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:41`
- Templates: 27; representative evidence: `addons/l10n_hu_edi/data/template_invoice.xml:3`, `addons/l10n_hu_edi/data/template_invoice.xml:103`, `addons/l10n_hu_edi/data/template_invoice.xml:112`, `addons/l10n_hu_edi/data/template_invoice.xml:127`, `addons/l10n_hu_edi/data/template_invoice.xml:147`, `addons/l10n_hu_edi/data/template_requests.xml:4`, `addons/l10n_hu_edi/data/template_requests.xml:29`, `addons/l10n_hu_edi/data/template_requests.xml:35`, `addons/l10n_hu_edi/data/template_requests.xml:50`, `addons/l10n_hu_edi/data/template_requests.xml:58`, `addons/l10n_hu_edi/data/template_requests.xml:69`, `addons/l10n_hu_edi/data/template_requests.xml:83`
- View/action field declarations: 26; representative evidence: `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:6`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:7`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:34`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml:35`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.xml:6`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.xml:7`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard_views.xml:6`, `addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard_views.xml:7`, `addons/l10n_hu_edi/views/uom_uom_views.xml:6`, `addons/l10n_hu_edi/views/uom_uom_views.xml:8`, `addons/l10n_hu_edi/views/res_config_settings_views.xml:5`, `addons/l10n_hu_edi/views/res_config_settings_views.xml:7`
- Browser assets: 1; representative files: `addons/l10n_hu_edi/static/src/views/sync_with_nav_btn/sync_with_nav_btn.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_hu_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_hu_edi/__manifest__.py`, `addons/l10n_hu_edi/models/account_move.py`, `addons/l10n_hu_edi/models/account_move_send.py`, `addons/l10n_hu_edi/data/ir_cron.xml`
- **Report entry points:** `addons/l10n_hu_edi/tests/test_invoice_report.py`

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `account.chart.template` (addons/l10n_hu_edi/models/template_hu.py:5); inherits `res.partner` (addons/l10n_hu_edi/models/res_partner.py:6); inherits `uom.uom` (addons/l10n_hu_edi/models/uom_uom.py:6); inherits `res.config.settings` (addons/l10n_hu_edi/models/res_config_settings.py:6); inherits `product.template` (addons/l10n_hu_edi/models/product.py:6); inherits `account.tax` (addons/l10n_hu_edi/models/account_tax.py:47); inherits `account.move` (addons/l10n_hu_edi/models/account_move.py:22); inherits `account.move.send` (addons/l10n_hu_edi/models/account_move_send.py:8); inherits `res.company` (addons/l10n_hu_edi/models/res_company.py:13); inherits `account.debit.note` (addons/l10n_hu_edi/wizard/account_move_debit.py:4); `l10n_hu_edi.cancellation` (addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.py:10); inherits `account.move.reversal` (addons/l10n_hu_edi/wizard/account_move_reversal.py:4); `l10n_hu_edi.tax_audit_export` (addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.py:12); `l10n_hu_edi.receive.bills.wizard` (addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_debit_note`, `l10n_hu`
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

- `addons/l10n_hu_edi/__init__.py`
- `addons/l10n_hu_edi/__manifest__.py`
- `addons/l10n_hu_edi/data/ir_cron.xml`
- `addons/l10n_hu_edi/data/neutralize.sql`
- `addons/l10n_hu_edi/data/template/account.tax-hu.csv`
- `addons/l10n_hu_edi/data/template_invoice.xml`
- `addons/l10n_hu_edi/data/template_requests.xml`
- `addons/l10n_hu_edi/data/uom.uom.csv`
- `addons/l10n_hu_edi/demo/demo_partner.xml`
- `addons/l10n_hu_edi/i18n/hu.po`
- `addons/l10n_hu_edi/i18n/l10n_hu_edi.pot`
- `addons/l10n_hu_edi/models/__init__.py`
- `addons/l10n_hu_edi/models/account_move.py`
- `addons/l10n_hu_edi/models/account_move_send.py`
- `addons/l10n_hu_edi/models/account_tax.py`
- `addons/l10n_hu_edi/models/l10n_hu_edi_connection.py`
- `addons/l10n_hu_edi/models/product.py`
- `addons/l10n_hu_edi/models/res_company.py`
- `addons/l10n_hu_edi/models/res_config_settings.py`
- `addons/l10n_hu_edi/models/res_partner.py`
- `addons/l10n_hu_edi/models/template_hu.py`
- `addons/l10n_hu_edi/models/uom_uom.py`
- `addons/l10n_hu_edi/security/ir.access.csv`
- `addons/l10n_hu_edi/static/img/gipsz_jakab.jpg`
- `addons/l10n_hu_edi/static/img/hun_flag.jpg`
- `addons/l10n_hu_edi/static/img/logo-mol-colorful.88751645.svg`
- `addons/l10n_hu_edi/static/img/magyaros_karoly.jpg`
- `addons/l10n_hu_edi/static/img/tvk.png`
- `addons/l10n_hu_edi/static/src/views/sync_with_nav_btn/sync_with_nav_btn.js`
- `addons/l10n_hu_edi/static/src/views/sync_with_nav_btn/sync_with_nav_btn.xml`
- `addons/l10n_hu_edi/tests/__init__.py`
- `addons/l10n_hu_edi/tests/common.py`
- `addons/l10n_hu_edi/tests/invoice_xmls/batch_modifications.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/credit_note.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/credit_note_original_bill.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/credit_note_receive.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/debit_note.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/debit_note_original_bill.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_advance.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_complex_eur.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_complex_huf.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_final.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_simple.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_simple_discount.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/invoice_tax_price_include.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/normal_invoice.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/query_invoice_data_response.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/query_invoice_data_response_gzip.xml`
- `addons/l10n_hu_edi/tests/invoice_xmls/simplified_invoice.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/BATCH_MOD_2026_0002_1.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/BATCH_MOD_2026_0002_2.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/INV_2026_00003.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/INV_2026_00004.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/manageAnnulment_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/manageAnnulment_response.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/manageInvoice_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/manageInvoice_response.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryInvoiceData_batch_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryInvoiceData_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryInvoiceDigest_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryInvoiceDigest_response.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionList_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionList_response.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response_annulment_done.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response_annulment_pending.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response_error.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response_original.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/queryTransactionStatus_response_warning.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/tokenExchange_request.xml`
- `addons/l10n_hu_edi/tests/mocked_requests/tokenExchange_response.xml`
- `addons/l10n_hu_edi/tests/test_account_move_sync_tax_lines.py`
- `addons/l10n_hu_edi/tests/test_bill_xml_upload.py`
- `addons/l10n_hu_edi/tests/test_credit_debit_notes.py`
- `addons/l10n_hu_edi/tests/test_flows_live.py`
- `addons/l10n_hu_edi/tests/test_flows_mocked.py`
- `addons/l10n_hu_edi/tests/test_invoice_report.py`
- `addons/l10n_hu_edi/tests/test_invoice_xml.py`
- `addons/l10n_hu_edi/tests/test_res_partner.py`
- `addons/l10n_hu_edi/views/account_move_views.xml`
- `addons/l10n_hu_edi/views/account_tax_views.xml`
- `addons/l10n_hu_edi/views/product_template_views.xml`
- `addons/l10n_hu_edi/views/report_invoice.xml`
- `addons/l10n_hu_edi/views/report_templates.xml`
- `addons/l10n_hu_edi/views/res_company_views.xml`
- `addons/l10n_hu_edi/views/res_config_settings_views.xml`
- `addons/l10n_hu_edi/views/res_partner_views.xml`
- `addons/l10n_hu_edi/views/uom_uom_views.xml`
- `addons/l10n_hu_edi/wizard/__init__.py`
- `addons/l10n_hu_edi/wizard/account_move_debit.py`
- `addons/l10n_hu_edi/wizard/account_move_reversal.py`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.py`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_cancellation.xml`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard.py`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_receive_bills_wizard_views.xml`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.py`
- `addons/l10n_hu_edi/wizard/l10n_hu_edi_tax_audit_export.xml`
