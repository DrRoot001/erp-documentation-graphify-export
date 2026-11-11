# Module: l10n_my_edi

- **Module ID:** MOD-279
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_my_edi`
- **Manifest:** `addons/l10n_my_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** E-invoicing using MyInvois

**Manifest description:**

This modules allows the user to send their invoices to the MyInvois system.

**Scope evidence:** The module contains 59 files, including 27 Python, 27 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_my`, `l10n_my_ubl_pint`, `account_edi_proxy_client`.

## 2. Module structure

- Model/business logic files: 15
- Controller/API files: 2
- XML/data/view/template files: 27
- Browser asset files: 0
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 6
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_my_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 15 model declarations, 225 methods, 1 constraint handlers, 1 onchange handlers, and 19 dependency declarations.
- **Evidence:** `addons/l10n_my_edi/models/res_partner.py:6`, `addons/l10n_my_edi/models/account_edi_proxy_user.py:11`, `addons/l10n_my_edi/models/product_template.py:80`, `addons/l10n_my_edi/models/res_config_settings.py:6`, `addons/l10n_my_edi/models/account_tax.py:5`, `addons/l10n_my_edi/models/account_move.py:6`, `addons/l10n_my_edi/models/account_journal_dashboard.py:4`, `addons/l10n_my_edi/models/myinvois_document.py:27`, `addons/l10n_my_edi/models/account_move_line.py:7`, `addons/l10n_my_edi/models/account_move_send.py:5`, `addons/l10n_my_edi/models/account_edi_xml_ubl_my.py:44`, `addons/l10n_my_edi/models/l10n_my_edi_industry_classification.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_my_edi/controllers/portal.py`, `addons/l10n_my_edi/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 27 XML files and 0 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.xml:3`, `addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.xml:3`, `addons/l10n_my_edi/data/ir_cron.xml:4`, `addons/l10n_my_edi/data/res_partner.xml:5`, `addons/l10n_my_edi/views/product_template_view.xml:4`, `addons/l10n_my_edi/views/report_invoice.xml:3`, `addons/l10n_my_edi/views/report_invoice.xml:25`, `addons/l10n_my_edi/views/l10n_my_edi_industrial_classification_views.xml:5`, `addons/l10n_my_edi/views/account_move_view.xml:3`, `addons/l10n_my_edi/views/account_move_view.xml:59`, `addons/l10n_my_edi/views/account_move_view.xml:75`, `addons/l10n_my_edi/views/res_company_view.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_my_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_my_edi/__manifest__.py`, `addons/l10n_my_edi/models/myinvois_document.py`, `addons/l10n_my_edi/data/ir_cron.xml`, `addons/l10n_my_edi/views/account_move_view.xml`, `addons/l10n_my_edi/views/myinvois_document_views.xml`, `addons/l10n_my_edi/tests/test_submissions.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_my_edi/models/myinvois_document.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/l10n_my_edi/tests/test_file_generation_common.py`, `addons/l10n_my_edi/tests/test_branch.py`, `addons/l10n_my_edi/tests/test_submissions.py`, `addons/l10n_my_edi/tests/test_consolidated_invoices.py`, `addons/l10n_my_edi/tests/__init__.py`, `addons/l10n_my_edi/tests/test_file_generation.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 27; representative identifiers: `myinvois_document_status_update_form`, `myinvois_consolidate_invoice_wizard_form`, `ir_cron_myinvois_document_sync`, `general_public`, `product_template_form_view`, `report_invoice_document`, `report_invoice`, `view_classification_list`, `view_move_form_inherit_l10n_my_myinvois`, `view_invoice_list_inherit_l10n_my_myinvois`, `invoice_send_to_myinvois`, `view_company_form_inherit_l10n_my_myinvois`, `account_journal_dashboard_kanban_view_inherit_l10n_my_myinvois`, `view_partner_form_inherit_l10n_my_myinvois`, `portal_my_details_fields`, `view_tax_form_inherit_l10n_my_myinvois`, `myinvois_document_form_view`, `myinvois_document_list_view`, `myinvois_document_search_view`, `action_generate_myinvois_document_file`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/l10n_my_edi/views/report_invoice.xml:3`, `addons/l10n_my_edi/views/report_invoice.xml:25`, `addons/l10n_my_edi/views/account_portal_templates.xml:2`
- View/action field declarations: 28; representative evidence: `addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.xml:5`, `addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.xml:6`, `addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.xml:5`, `addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.xml:6`, `addons/l10n_my_edi/views/product_template_view.xml:6`, `addons/l10n_my_edi/views/product_template_view.xml:8`, `addons/l10n_my_edi/views/l10n_my_edi_industrial_classification_views.xml:7`, `addons/l10n_my_edi/views/l10n_my_edi_industrial_classification_views.xml:8`, `addons/l10n_my_edi/views/account_move_view.xml:5`, `addons/l10n_my_edi/views/account_move_view.xml:7`, `addons/l10n_my_edi/views/account_move_view.xml:61`, `addons/l10n_my_edi/views/account_move_view.xml:63`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_my_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_my_edi/__manifest__.py`, `addons/l10n_my_edi/models/myinvois_document.py`, `addons/l10n_my_edi/data/ir_cron.xml`, `addons/l10n_my_edi/views/account_move_view.xml`, `addons/l10n_my_edi/views/myinvois_document_views.xml`, `addons/l10n_my_edi/tests/test_submissions.py`
- **Report entry points:** `addons/l10n_my_edi/models/myinvois_document.py`

## 7. Database interactions

- Model declarations: 15
- Representative model evidence: inherits `res.partner` (addons/l10n_my_edi/models/res_partner.py:6); inherits `account_edi_proxy_client.user` (addons/l10n_my_edi/models/account_edi_proxy_user.py:11); inherits `product.template` (addons/l10n_my_edi/models/product_template.py:80); inherits `res.config.settings` (addons/l10n_my_edi/models/res_config_settings.py:6); inherits `account.tax` (addons/l10n_my_edi/models/account_tax.py:5); inherits `account.move` (addons/l10n_my_edi/models/account_move.py:6); inherits `account.journal` (addons/l10n_my_edi/models/account_journal_dashboard.py:4); `myinvois.document` (addons/l10n_my_edi/models/myinvois_document.py:27); inherits `account.move.line` (addons/l10n_my_edi/models/account_move_line.py:7); inherits `account.move.send` (addons/l10n_my_edi/models/account_move_send.py:5); `account.edi.xml.ubl_myinvois_my` (addons/l10n_my_edi/models/account_edi_xml_ubl_my.py:44); `l10n_my_edi.industry_classification` (addons/l10n_my_edi/models/l10n_my_edi_industry_classification.py:5); inherits `res.company` (addons/l10n_my_edi/models/res_company.py:6); `myinvois.consolidate.invoice.wizard` (addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.py:10); `myinvois.document.status.update.wizard` (addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_my`, `l10n_my_ubl_pint`, `account_edi_proxy_client`
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

- `addons/l10n_my_edi/__init__.py`
- `addons/l10n_my_edi/__manifest__.py`
- `addons/l10n_my_edi/controllers/__init__.py`
- `addons/l10n_my_edi/controllers/portal.py`
- `addons/l10n_my_edi/data/ir_cron.xml`
- `addons/l10n_my_edi/data/l10n_my_edi.industry_classification.csv`
- `addons/l10n_my_edi/data/neutralize.sql`
- `addons/l10n_my_edi/data/res_partner.xml`
- `addons/l10n_my_edi/i18n/l10n_my_edi.pot`
- `addons/l10n_my_edi/i18n/ms.po`
- `addons/l10n_my_edi/models/__init__.py`
- `addons/l10n_my_edi/models/account_edi_proxy_user.py`
- `addons/l10n_my_edi/models/account_edi_xml_ubl_my.py`
- `addons/l10n_my_edi/models/account_journal_dashboard.py`
- `addons/l10n_my_edi/models/account_move.py`
- `addons/l10n_my_edi/models/account_move_line.py`
- `addons/l10n_my_edi/models/account_move_send.py`
- `addons/l10n_my_edi/models/account_tax.py`
- `addons/l10n_my_edi/models/l10n_my_edi_industry_classification.py`
- `addons/l10n_my_edi/models/myinvois_document.py`
- `addons/l10n_my_edi/models/product_template.py`
- `addons/l10n_my_edi/models/res_company.py`
- `addons/l10n_my_edi/models/res_config_settings.py`
- `addons/l10n_my_edi/models/res_partner.py`
- `addons/l10n_my_edi/security/ir.access.csv`
- `addons/l10n_my_edi/tests/__init__.py`
- `addons/l10n_my_edi/tests/expected_xmls/bill_import.xml`
- `addons/l10n_my_edi/tests/expected_xmls/credit_note.xml`
- `addons/l10n_my_edi/tests/expected_xmls/credit_note_company_currency.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_foreigner.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_import.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_multicurrency.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_optional_fields.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_self_billing.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_tax_exempt.xml`
- `addons/l10n_my_edi/tests/expected_xmls/invoice_with_so.xml`
- `addons/l10n_my_edi/tests/expected_xmls/refund_note_company_currency.xml`
- `addons/l10n_my_edi/tests/test_branch.py`
- `addons/l10n_my_edi/tests/test_consolidated_invoices.py`
- `addons/l10n_my_edi/tests/test_file_generation.py`
- `addons/l10n_my_edi/tests/test_file_generation_common.py`
- `addons/l10n_my_edi/tests/test_submissions.py`
- `addons/l10n_my_edi/views/account_journal_dashboard_view.xml`
- `addons/l10n_my_edi/views/account_move_view.xml`
- `addons/l10n_my_edi/views/account_portal_templates.xml`
- `addons/l10n_my_edi/views/account_tax_view.xml`
- `addons/l10n_my_edi/views/l10n_my_edi_industrial_classification_views.xml`
- `addons/l10n_my_edi/views/myinvois_document_views.xml`
- `addons/l10n_my_edi/views/product_template_view.xml`
- `addons/l10n_my_edi/views/report_invoice.xml`
- `addons/l10n_my_edi/views/res_company_view.xml`
- `addons/l10n_my_edi/views/res_config_settings_view.xml`
- `addons/l10n_my_edi/views/res_partner_view.xml`
- `addons/l10n_my_edi/wizard/__init__.py`
- `addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.py`
- `addons/l10n_my_edi/wizard/myinvois_consolidate_invoice_wizard.xml`
- `addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.py`
- `addons/l10n_my_edi/wizard/myinvois_document_status_update_wizard.xml`
