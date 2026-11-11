# Module: l10n_hr_edi

- **Module ID:** MOD-217
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_hr_edi`
- **Manifest:** `addons/l10n_hr_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Reporting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

e-invoicing for Croatia

**Scope evidence:** The module contains 52 files, including 26 Python, 20 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_hr`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 16
- Controller/API files: 0
- XML/data/view/template files: 20
- Browser asset files: 0
- Security files: 1
- Test files: 6
- Scheduled/automation evidence files: 3
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_hr_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 16 model declarations, 109 methods, 3 constraint handlers, 0 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/l10n_hr_edi/models/res_partner.py:7`, `addons/l10n_hr_edi/models/product_template.py:4`, `addons/l10n_hr_edi/models/product_template.py:13`, `addons/l10n_hr_edi/models/account_edi_xml_ubl_hr.py:10`, `addons/l10n_hr_edi/models/res_config_settings.py:4`, `addons/l10n_hr_edi/models/account_journal.py:4`, `addons/l10n_hr_edi/models/account_tax.py:4`, `addons/l10n_hr_edi/models/account_tax.py:10`, `addons/l10n_hr_edi/models/account_chart_template.py:6`, `addons/l10n_hr_edi/models/sequence_mixin.py:28`, `addons/l10n_hr_edi/models/account_move.py:22`, `addons/l10n_hr_edi/models/account_move_line.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 20 XML files and 0 JavaScript/TypeScript files; static XML analysis found 32 record/template/menu identifiers.
- **Evidence:** `addons/l10n_hr_edi/demo/demo_company.xml:3`, `addons/l10n_hr_edi/demo/demo_company.xml:10`, `addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard_views.xml:3`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:5`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:13`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:21`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:29`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:37`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:45`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:53`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:61`, `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml:69`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_hr_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_hr_edi/models/account_move_send.py`, `addons/l10n_hr_edi/models/res_company.py`, `addons/l10n_hr_edi/data/cron.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/l10n_hr_edi/tests/test_payment_unreported.py`, `addons/l10n_hr_edi/tests/test_mer_api.py`, `addons/l10n_hr_edi/tests/test_hr_edi_common.py`, `addons/l10n_hr_edi/tests/test_flows.py`, `addons/l10n_hr_edi/tests/__init__.py`, `addons/l10n_hr_edi/tests/test_ubl_hr.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 20; representative identifiers: `base.demo_company_hr`, `base.partner_demo_customer_hr`, `mojeracun_reject_wizard_form`, `vat_type_pdv25`, `vat_type_pdv13`, `vat_type_pdv5`, `vat_type_z`, `vat_type_k`, `vat_type_g`, `vat_type_ae`, `vat_type_e`, `vat_type_povnak`, `vat_type_pp`, `vat_type_ppmv`, `vat_type_o`, `vat_type_n`, `ir_cron_mer_get_new_documents`, `ir_cron_mer_update_document_status`, `ir_cron_mer_archive_signed_xmls`, `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_hr_edi/views/report_invoice_views.xml:4`, `addons/l10n_hr_edi/views/report_invoice_views.xml:34`
- View/action field declarations: 24; representative evidence: `addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard_views.xml:5`, `addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard_views.xml:7`, `addons/l10n_hr_edi/views/res_config_settings_views.xml:5`, `addons/l10n_hr_edi/views/res_config_settings_views.xml:7`, `addons/l10n_hr_edi/views/account_move_views.xml:6`, `addons/l10n_hr_edi/views/account_move_views.xml:8`, `addons/l10n_hr_edi/views/account_move_views.xml:135`, `addons/l10n_hr_edi/views/account_move_views.xml:137`, `addons/l10n_hr_edi/views/account_move_views.xml:195`, `addons/l10n_hr_edi/views/account_move_views.xml:197`, `addons/l10n_hr_edi/views/l10n_hr_kpd_category_views.xml:5`, `addons/l10n_hr_edi/views/l10n_hr_kpd_category_views.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_hr_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_hr_edi/models/account_move_send.py`, `addons/l10n_hr_edi/models/res_company.py`, `addons/l10n_hr_edi/data/cron.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 16
- Representative model evidence: inherits `res.partner` (addons/l10n_hr_edi/models/res_partner.py:7); inherits `product.template` (addons/l10n_hr_edi/models/product_template.py:4); `l10n_hr.kpd.category` (addons/l10n_hr_edi/models/product_template.py:13); `account.edi.xml.ubl_hr` (addons/l10n_hr_edi/models/account_edi_xml_ubl_hr.py:10); inherits `res.config.settings` (addons/l10n_hr_edi/models/res_config_settings.py:4); inherits `account.journal` (addons/l10n_hr_edi/models/account_journal.py:4); inherits `account.tax` (addons/l10n_hr_edi/models/account_tax.py:4); `l10n.hr.tax.category` (addons/l10n_hr_edi/models/account_tax.py:10); inherits `account.chart.template` (addons/l10n_hr_edi/models/account_chart_template.py:6); inherits `sequence.mixin` (addons/l10n_hr_edi/models/sequence_mixin.py:28); inherits `account.move` (addons/l10n_hr_edi/models/account_move.py:22); inherits `account.move.line` (addons/l10n_hr_edi/models/account_move_line.py:4); inherits `account.move.send` (addons/l10n_hr_edi/models/account_move_send.py:12); `l10n_hr_edi.addendum` (addons/l10n_hr_edi/models/l10n_hr_edi_addendum.py:4); inherits `res.company` (addons/l10n_hr_edi/models/res_company.py:21); `l10n_hr_edi.mojeracun_reject_wizard` (addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_hr`, `account_edi_ubl_cii`
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

- `addons/l10n_hr_edi/__init__.py`
- `addons/l10n_hr_edi/__manifest__.py`
- `addons/l10n_hr_edi/data/cron.xml`
- `addons/l10n_hr_edi/data/l10n_hr.kpd.category.csv`
- `addons/l10n_hr_edi/data/l10n_hr_tax_category.xml`
- `addons/l10n_hr_edi/data/neutralize.sql`
- `addons/l10n_hr_edi/data/template/account.tax-hr.csv`
- `addons/l10n_hr_edi/demo/demo_company.xml`
- `addons/l10n_hr_edi/i18n/hr.po`
- `addons/l10n_hr_edi/i18n/l10n_hr_edi.pot`
- `addons/l10n_hr_edi/models/__init__.py`
- `addons/l10n_hr_edi/models/account_chart_template.py`
- `addons/l10n_hr_edi/models/account_edi_xml_ubl_hr.py`
- `addons/l10n_hr_edi/models/account_journal.py`
- `addons/l10n_hr_edi/models/account_move.py`
- `addons/l10n_hr_edi/models/account_move_line.py`
- `addons/l10n_hr_edi/models/account_move_send.py`
- `addons/l10n_hr_edi/models/account_tax.py`
- `addons/l10n_hr_edi/models/l10n_hr_edi_addendum.py`
- `addons/l10n_hr_edi/models/product_template.py`
- `addons/l10n_hr_edi/models/res_company.py`
- `addons/l10n_hr_edi/models/res_config_settings.py`
- `addons/l10n_hr_edi/models/res_partner.py`
- `addons/l10n_hr_edi/models/sequence_mixin.py`
- `addons/l10n_hr_edi/security/ir.access.csv`
- `addons/l10n_hr_edi/tests/__init__.py`
- `addons/l10n_hr_edi/tests/flows/in_invoice.xml`
- `addons/l10n_hr_edi/tests/flows/out_invoice.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice_cash_basis.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice_exemption_e.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice_exemption_k.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice_multiple.xml`
- `addons/l10n_hr_edi/tests/test_files/test_invoice_refund.xml`
- `addons/l10n_hr_edi/tests/test_flows.py`
- `addons/l10n_hr_edi/tests/test_hr_edi_common.py`
- `addons/l10n_hr_edi/tests/test_mer_api.py`
- `addons/l10n_hr_edi/tests/test_payment_unreported.py`
- `addons/l10n_hr_edi/tests/test_ubl_hr.py`
- `addons/l10n_hr_edi/tools/__init__.py`
- `addons/l10n_hr_edi/tools/api.py`
- `addons/l10n_hr_edi/views/account_journal_views.xml`
- `addons/l10n_hr_edi/views/account_move_views.xml`
- `addons/l10n_hr_edi/views/account_tax_views.xml`
- `addons/l10n_hr_edi/views/l10n_hr_kpd_category_views.xml`
- `addons/l10n_hr_edi/views/product_views.xml`
- `addons/l10n_hr_edi/views/report_invoice_views.xml`
- `addons/l10n_hr_edi/views/res_config_settings_views.xml`
- `addons/l10n_hr_edi/views/res_partner_views.xml`
- `addons/l10n_hr_edi/wizard/__init__.py`
- `addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard.py`
- `addons/l10n_hr_edi/wizard/l10n_hr_edi_mojeracun_reject_wizard_views.xml`
