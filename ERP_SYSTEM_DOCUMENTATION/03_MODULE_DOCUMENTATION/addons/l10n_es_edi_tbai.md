# Module: l10n_es_edi_tbai

- **Module ID:** MOD-177
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es_edi_tbai`
- **Manifest:** `addons/l10n_es_edi_tbai/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module sends invoices and vendor bills to the "Diputaciones
Forales" of Araba/Álava, Bizkaia and Gipuzkoa.

Invoices and bills get converted to XML and regularly sent to the
Basque government servers which provides them with a unique identifier.
A hash chain ensures the continuous nature of the invoice/bill
sequences. QR codes are added to emitted (sent/printed) invoices,
bills and tickets to allow anyone to check they have been declared.

You need to configure your certificate and the tax agency.

**Scope evidence:** The module contains 60 files, including 24 Python, 29 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_es`, `certificate`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 29
- Browser asset files: 0
- Security files: 1
- Test files: 10
- Scheduled/automation evidence files: 1
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_es_edi_tbai/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 143 methods, 0 constraint handlers, 0 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/l10n_es_edi_tbai/models/l10n_es_edi_tbai_document.py:48`, `addons/l10n_es_edi_tbai/models/res_config_settings.py:7`, `addons/l10n_es_edi_tbai/models/account_tax.py:5`, `addons/l10n_es_edi_tbai/models/certificate.py:6`, `addons/l10n_es_edi_tbai/models/account_move.py:12`, `addons/l10n_es_edi_tbai/models/account_move_line.py:4`, `addons/l10n_es_edi_tbai/models/account_move_send.py:4`, `addons/l10n_es_edi_tbai/models/res_company.py:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 29 XML files and 0 JavaScript/TypeScript files; static XML analysis found 28 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es_edi_tbai/demo/demo_res_partner.xml:3`, `addons/l10n_es_edi_tbai/demo/demo_res_partner.xml:11`, `addons/l10n_es_edi_tbai/demo/demo_company.xml:3`, `addons/l10n_es_edi_tbai/demo/demo_certificate.xml:3`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:4`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:10`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:16`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:55`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:78`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:149`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:197`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_es_edi_tbai/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_es_edi_tbai/views/account_move_view.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_bill_bizkaia.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 10 test files are present.
- **Evidence:** `addons/l10n_es_edi_tbai/tests/test_tbai_recipient_id_types.py`, `addons/l10n_es_edi_tbai/tests/test_edi_xml.py`, `addons/l10n_es_edi_tbai/tests/test_move_reversal.py`, `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_bill_bizkaia.py`, `addons/l10n_es_edi_tbai/tests/common.py`, `addons/l10n_es_edi_tbai/tests/test_edi_tbai_user_errors.py`, `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_invoice_bizkaia.py`, `addons/l10n_es_edi_tbai/tests/__init__.py`, `addons/l10n_es_edi_tbai/tests/test_edi_web_services.py`, `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_invoice.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 29; representative identifiers: `l10n_es_tbai_partner_spanish_filemon`, `l10n_es_tbai_partner_european_lagaffe`, `base.demo_company_es`, `demo_certificate`, `template_invoice_main_post`, `template_invoice_main_cancel`, `template_invoice_bundle`, `template_invoice_sujetos`, `template_invoice_factura`, `template_invoice_desglose`, `template_digital_signature`, `template_LROE_240_main`, `template_LROE_240_inner`, `template_LROE_240_main_recibidas`, `template_LROE_240_inner_recibidas`, `template_LROE_recibidas_common`, `epigrafe_config`, `res_config_settings_view_form`, `l10n_es_tbai_external_layout_standard`, `view_move_form_inherit_l10n_es_edi_tbai`
- Menus: 3; representative evidence: `addons/l10n_es_edi_tbai/views/res_company_views.xml:18`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:37`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:42`
- Templates: 13; representative evidence: `addons/l10n_es_edi_tbai/data/template_invoice.xml:4`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:10`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:16`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:55`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:78`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:149`, `addons/l10n_es_edi_tbai/data/template_invoice.xml:197`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:6`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:29`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:58`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:81`, `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml:106`
- View/action field declarations: 12; representative evidence: `addons/l10n_es_edi_tbai/views/res_config_settings_views.xml:5`, `addons/l10n_es_edi_tbai/views/res_config_settings_views.xml:7`, `addons/l10n_es_edi_tbai/views/account_move_view.xml:6`, `addons/l10n_es_edi_tbai/views/account_move_view.xml:8`, `addons/l10n_es_edi_tbai/views/res_company_views.xml:5`, `addons/l10n_es_edi_tbai/views/res_company_views.xml:7`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:7`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:9`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:18`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:19`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:28`, `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml:30`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es_edi_tbai/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_es_edi_tbai/views/account_move_view.xml`
- **Report entry points:** `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_bill_bizkaia.py`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: `l10n_es_edi_tbai.document` (addons/l10n_es_edi_tbai/models/l10n_es_edi_tbai_document.py:48); inherits `res.config.settings` (addons/l10n_es_edi_tbai/models/res_config_settings.py:7); inherits `account.tax` (addons/l10n_es_edi_tbai/models/account_tax.py:5); inherits `certificate.certificate` (addons/l10n_es_edi_tbai/models/certificate.py:6); inherits `account.move` (addons/l10n_es_edi_tbai/models/account_move.py:12); inherits `account.move.line` (addons/l10n_es_edi_tbai/models/account_move_line.py:4); inherits `account.move.send` (addons/l10n_es_edi_tbai/models/account_move_send.py:4); inherits `res.company` (addons/l10n_es_edi_tbai/models/res_company.py:45)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_es`, `certificate`
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

- `addons/l10n_es_edi_tbai/__init__.py`
- `addons/l10n_es_edi_tbai/__manifest__.py`
- `addons/l10n_es_edi_tbai/const.py`
- `addons/l10n_es_edi_tbai/data/ir_config_parameter.xml`
- `addons/l10n_es_edi_tbai/data/neutralize.sql`
- `addons/l10n_es_edi_tbai/data/template_LROE_bizkaia.xml`
- `addons/l10n_es_edi_tbai/data/template_invoice.xml`
- `addons/l10n_es_edi_tbai/demo/certificates/Bizkaia-IZDesa2025.p12`
- `addons/l10n_es_edi_tbai/demo/certificates/araba_1234.p12`
- `addons/l10n_es_edi_tbai/demo/certificates/gipuzkoa_Iz3np32024.p12`
- `addons/l10n_es_edi_tbai/demo/demo_certificate.xml`
- `addons/l10n_es_edi_tbai/demo/demo_company.xml`
- `addons/l10n_es_edi_tbai/demo/demo_res_partner.xml`
- `addons/l10n_es_edi_tbai/i18n/es.po`
- `addons/l10n_es_edi_tbai/i18n/l10n_es_edi_tbai.pot`
- `addons/l10n_es_edi_tbai/models/__init__.py`
- `addons/l10n_es_edi_tbai/models/account_move.py`
- `addons/l10n_es_edi_tbai/models/account_move_line.py`
- `addons/l10n_es_edi_tbai/models/account_move_send.py`
- `addons/l10n_es_edi_tbai/models/account_tax.py`
- `addons/l10n_es_edi_tbai/models/certificate.py`
- `addons/l10n_es_edi_tbai/models/l10n_es_edi_tbai_agencies.py`
- `addons/l10n_es_edi_tbai/models/l10n_es_edi_tbai_document.py`
- `addons/l10n_es_edi_tbai/models/res_company.py`
- `addons/l10n_es_edi_tbai/models/res_config_settings.py`
- `addons/l10n_es_edi_tbai/models/xml_utils.py`
- `addons/l10n_es_edi_tbai/security/ir.access.csv`
- `addons/l10n_es_edi_tbai/tests/__init__.py`
- `addons/l10n_es_edi_tbai/tests/common.py`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_cancel.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_fecha_operacion.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post_in.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post_in_140.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post_in_ic.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post_in_nd.xml`
- `addons/l10n_es_edi_tbai/tests/document_xmls/xml_post_refund.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/cancel_bill_failure_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/cancel_bill_success_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/cancel_invoice_failure_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/cancel_invoice_success_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/cancel_invoice_success_gi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/post_bill_success_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/post_invoice_failure_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/post_invoice_success_bi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/post_invoice_success_gi.xml`
- `addons/l10n_es_edi_tbai/tests/response_xmls/post_or_cancel_invoice_failure_gi.xml`
- `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_bill_bizkaia.py`
- `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_invoice.py`
- `addons/l10n_es_edi_tbai/tests/test_edi_tbai_send_invoice_bizkaia.py`
- `addons/l10n_es_edi_tbai/tests/test_edi_tbai_user_errors.py`
- `addons/l10n_es_edi_tbai/tests/test_edi_web_services.py`
- `addons/l10n_es_edi_tbai/tests/test_edi_xml.py`
- `addons/l10n_es_edi_tbai/tests/test_move_reversal.py`
- `addons/l10n_es_edi_tbai/tests/test_tbai_recipient_id_types.py`
- `addons/l10n_es_edi_tbai/views/account_move_view.xml`
- `addons/l10n_es_edi_tbai/views/l10n_es_edi_tbai_certificate_views.xml`
- `addons/l10n_es_edi_tbai/views/report_invoice.xml`
- `addons/l10n_es_edi_tbai/views/res_company_views.xml`
- `addons/l10n_es_edi_tbai/views/res_config_settings_views.xml`
