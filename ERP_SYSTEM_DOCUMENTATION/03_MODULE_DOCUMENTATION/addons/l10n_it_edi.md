# Module: l10n_it_edi

- **Module ID:** MOD-241
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_it_edi`
- **Manifest:** `addons/l10n_it_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

E-invoice implementation

**Scope evidence:** The module contains 119 files, including 38 Python, 68 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_it`, `account_edi_proxy_client`, `account_debit_note`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 2
- XML/data/view/template files: 68
- Browser asset files: 2
- Security files: 1
- Test files: 14
- Scheduled/automation evidence files: 5
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_it_edi/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 313 methods, 8 constraint handlers, 3 onchange handlers, and 19 dependency declarations.
- **Evidence:** `addons/l10n_it_edi/demo/account_demo.py:5`, `addons/l10n_it_edi/models/res_partner.py:10`, `addons/l10n_it_edi/models/account_edi_proxy_user.py:11`, `addons/l10n_it_edi/models/res_config_settings.py:6`, `addons/l10n_it_edi/models/account_payment_method_line.py:36`, `addons/l10n_it_edi/models/ddt.py:7`, `addons/l10n_it_edi/models/account_journal.py:4`, `addons/l10n_it_edi/models/account_tax.py:73`, `addons/l10n_it_edi/models/l10n_it_document_type.py:5`, `addons/l10n_it_edi/models/account_chart_template.py:5`, `addons/l10n_it_edi/models/account_move.py:62`, `addons/l10n_it_edi/models/account_move_send.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_it_edi/controllers/portal.py`, `addons/l10n_it_edi/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 68 XML files and 2 JavaScript/TypeScript files; static XML analysis found 33 record/template/menu identifiers.
- **Evidence:** `addons/l10n_it_edi/data/ir_cron.xml:3`, `addons/l10n_it_edi/data/invoice_it_simplified_template.xml:4`, `addons/l10n_it_edi/data/invoice_it_simplified_template.xml:20`, `addons/l10n_it_edi/data/account_invoice_demo.xml:5`, `addons/l10n_it_edi/data/account_invoice_demo.xml:15`, `addons/l10n_it_edi/data/account_invoice_demo.xml:19`, `addons/l10n_it_edi/data/account_invoice_demo.xml:31`, `addons/l10n_it_edi/data/account_invoice_demo.xml:39`, `addons/l10n_it_edi/data/account_invoice_demo.xml:50`, `addons/l10n_it_edi/data/account_invoice_demo.xml:61`, `addons/l10n_it_edi/data/account_invoice_demo.xml:66`, `addons/l10n_it_edi/data/invoice_it_template.xml:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_it_edi/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_it_edi/__manifest__.py`, `addons/l10n_it_edi/models/account_move.py`, `addons/l10n_it_edi/data/ir_cron.xml`, `addons/l10n_it_edi/tests/test_edi_import.py`, `addons/l10n_it_edi/tests/test_account_move_send.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 14 test files are present.
- **Evidence:** `addons/l10n_it_edi/tests/test_account_move_payment_method.py`, `addons/l10n_it_edi/tests/test_withholding.py`, `addons/l10n_it_edi/tests/test_edi_export.py`, `addons/l10n_it_edi/tests/test_edi_pa.py`, `addons/l10n_it_edi/tests/test_edi_reverse_charge.py`, `addons/l10n_it_edi/tests/common.py`, `addons/l10n_it_edi/tests/test_account_move_document_type.py`, `addons/l10n_it_edi/tests/test_edi_import.py`, `addons/l10n_it_edi/tests/test_edi_address.py`, `addons/l10n_it_edi/tests/__init__.py`, `addons/l10n_it_edi/tests/test_res_partner.py`, `addons/l10n_it_edi/tests/test_it_document_type.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 68; representative identifiers: `ir_cron_l10n_it_edi_download_and_update`, `account_invoice_line_it_simplified_FatturaPA`, `account_invoice_it_simplified_FatturaPA_export`, `base.demo_company_it`, `base.partner_demo_company_it`, `partner_demo_it`, `demo_l10n_it_edi_bank`, `demo_l10n_it_edi_partner_a`, `demo_l10n_it_edi_partner_pa`, `demo_l10n_it_edi_key`, `demo_l10n_it_edi_proxy_user`, `account_invoice_line_it_FatturaPA`, `account_invoice_it_FatturaPA_export`, `account_invoice_it_FatturaPA_sede`, `account_invoice_FatturaPA_origin_document`, `view_account_journal_form_l10n_it`, `res_config_settings_view_form`, `report_invoice_document`, `document_tax_totals_inherit_stamp_duty`, `Show l10n_it fields`
- Menus: 1; representative evidence: `addons/l10n_it_edi/views/l10n_it_view.xml:227`
- Templates: 9; representative evidence: `addons/l10n_it_edi/data/invoice_it_simplified_template.xml:4`, `addons/l10n_it_edi/data/invoice_it_simplified_template.xml:20`, `addons/l10n_it_edi/data/invoice_it_template.xml:5`, `addons/l10n_it_edi/data/invoice_it_template.xml:47`, `addons/l10n_it_edi/data/invoice_it_template.xml:247`, `addons/l10n_it_edi/data/invoice_it_template.xml:257`, `addons/l10n_it_edi/views/report_invoice.xml:3`, `addons/l10n_it_edi/views/report_invoice.xml:66`, `addons/l10n_it_edi/views/portal_address_templates.xml:4`
- View/action field declarations: 28; representative evidence: `addons/l10n_it_edi/views/account_payment_method.xml:6`, `addons/l10n_it_edi/views/account_payment_method.xml:8`, `addons/l10n_it_edi/views/res_config_settings_views.xml:6`, `addons/l10n_it_edi/views/res_config_settings_views.xml:8`, `addons/l10n_it_edi/views/l10n_it_document_type.xml:7`, `addons/l10n_it_edi/views/l10n_it_document_type.xml:8`, `addons/l10n_it_edi/views/l10n_it_document_type.xml:18`, `addons/l10n_it_edi/views/l10n_it_document_type.xml:19`, `addons/l10n_it_edi/views/account_tax_view.xml:6`, `addons/l10n_it_edi/views/account_tax_view.xml:9`, `addons/l10n_it_edi/views/l10n_it_view.xml:7`, `addons/l10n_it_edi/views/l10n_it_view.xml:9`
- Browser assets: 2; representative files: `addons/l10n_it_edi/static/src/interactions/address.js`, `addons/l10n_it_edi/static/tests/tours/l10n_it_edi_address_codice_fiscale.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_it_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_it_edi/__manifest__.py`, `addons/l10n_it_edi/models/account_move.py`, `addons/l10n_it_edi/data/ir_cron.xml`, `addons/l10n_it_edi/tests/test_edi_import.py`, `addons/l10n_it_edi/tests/test_account_move_send.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `account.chart.template` (addons/l10n_it_edi/demo/account_demo.py:5); inherits `res.partner` (addons/l10n_it_edi/models/res_partner.py:10); inherits `account_edi_proxy_client.user` (addons/l10n_it_edi/models/account_edi_proxy_user.py:11); inherits `res.config.settings` (addons/l10n_it_edi/models/res_config_settings.py:6); inherits `account.payment.method.line` (addons/l10n_it_edi/models/account_payment_method_line.py:36); `l10n_it.ddt` (addons/l10n_it_edi/models/ddt.py:7); inherits `account.journal` (addons/l10n_it_edi/models/account_journal.py:4); inherits `account.tax` (addons/l10n_it_edi/models/account_tax.py:73); `l10n_it.document.type` (addons/l10n_it_edi/models/l10n_it_document_type.py:5); inherits `account.chart.template` (addons/l10n_it_edi/models/account_chart_template.py:5); inherits `account.move` (addons/l10n_it_edi/models/account_move.py:62); inherits `account.move.send` (addons/l10n_it_edi/models/account_move_send.py:7); inherits `res.company` (addons/l10n_it_edi/models/res_company.py:28); inherits `account.payment.register` (addons/l10n_it_edi/wizard/account_payment_register.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_it`, `account_edi_proxy_client`, `account_debit_note`
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

- `addons/l10n_it_edi/__init__.py`
- `addons/l10n_it_edi/__manifest__.py`
- `addons/l10n_it_edi/controllers/__init__.py`
- `addons/l10n_it_edi/controllers/portal.py`
- `addons/l10n_it_edi/data/account.account.tag.csv`
- `addons/l10n_it_edi/data/account_invoice_demo.xml`
- `addons/l10n_it_edi/data/invoice_it_simplified_template.xml`
- `addons/l10n_it_edi/data/invoice_it_template.xml`
- `addons/l10n_it_edi/data/ir_cron.xml`
- `addons/l10n_it_edi/data/l10n_it.document.type.csv`
- `addons/l10n_it_edi/data/neutralize.sql`
- `addons/l10n_it_edi/data/pkey.key`
- `addons/l10n_it_edi/data/template/account.tax-it.csv`
- `addons/l10n_it_edi/demo/__init__.py`
- `addons/l10n_it_edi/demo/account_demo.py`
- `addons/l10n_it_edi/i18n/it.po`
- `addons/l10n_it_edi/i18n/l10n_it_edi.pot`
- `addons/l10n_it_edi/migrations/0.5/post-moving-account-taxes.py`
- `addons/l10n_it_edi/models/__init__.py`
- `addons/l10n_it_edi/models/account_chart_template.py`
- `addons/l10n_it_edi/models/account_edi_proxy_user.py`
- `addons/l10n_it_edi/models/account_journal.py`
- `addons/l10n_it_edi/models/account_move.py`
- `addons/l10n_it_edi/models/account_move_send.py`
- `addons/l10n_it_edi/models/account_payment_method_line.py`
- `addons/l10n_it_edi/models/account_tax.py`
- `addons/l10n_it_edi/models/ddt.py`
- `addons/l10n_it_edi/models/l10n_it_document_type.py`
- `addons/l10n_it_edi/models/res_company.py`
- `addons/l10n_it_edi/models/res_config_settings.py`
- `addons/l10n_it_edi/models/res_partner.py`
- `addons/l10n_it_edi/security/ir.access.csv`
- `addons/l10n_it_edi/static/src/interactions/address.js`
- `addons/l10n_it_edi/static/tests/tours/l10n_it_edi_address_codice_fiscale.js`
- `addons/l10n_it_edi/tests/__init__.py`
- `addons/l10n_it_edi/tests/common.py`
- `addons/l10n_it_edi/tests/export_xmls/bill_reverse_charge.xml`
- `addons/l10n_it_edi/tests/export_xmls/bill_reverse_charge_2.xml`
- `addons/l10n_it_edi/tests/export_xmls/bill_reverse_charge_san_marino.xml`
- `addons/l10n_it_edi/tests/export_xmls/credit_note_export_document_type.xml`
- `addons/l10n_it_edi/tests/export_xmls/credit_note_negative_price.xml`
- `addons/l10n_it_edi/tests/export_xmls/credit_note_refund_no_reconcile.xml`
- `addons/l10n_it_edi/tests/export_xmls/credit_note_reverse_charge.xml`
- `addons/l10n_it_edi/tests/export_xmls/enasarco_tax_invoice.xml`
- `addons/l10n_it_edi/tests/export_xmls/export_foreign_currency_global_discount.xml`
- `addons/l10n_it_edi/tests/export_xmls/export_foreign_currency_global_simple_discount.xml`
- `addons/l10n_it_edi/tests/export_xmls/export_foreign_currency_simple_discount.xml`
- `addons/l10n_it_edi/tests/export_xmls/inps_tax_invoice.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_below_400_codice_simplified.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_decimal_precision_product.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_exclude_postdated_moves.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_external_reverse_charge.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_fully_discounted.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_internal_reverse_charge.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_lowercase_fields.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_negative_price.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_non_latin_and_latin.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_partially_discounted.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_price_included_taxes.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_total_400_VAT_simplified.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_vat_not_equals_codice.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_with_attachment.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_with_multiple_product_description_fields.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_with_oss_tax.xml`
- `addons/l10n_it_edi/tests/export_xmls/invoice_with_rounding_line.xml`
- `addons/l10n_it_edi/tests/export_xmls/it_edi_debit_note.xml`
- `addons/l10n_it_edi/tests/export_xmls/pension_fund_tax_invoice.xml`
- `addons/l10n_it_edi/tests/export_xmls/prezzio_unitario_converted_company_currency.xml`
- `addons/l10n_it_edi/tests/export_xmls/split_payment.xml`
- `addons/l10n_it_edi/tests/export_xmls/split_payment_cn.xml`
- `addons/l10n_it_edi/tests/export_xmls/test_export_invoice_with_two_downpayments.xml`
- `addons/l10n_it_edi/tests/export_xmls/withholding_23_ret20.xml`
- `addons/l10n_it_edi/tests/export_xmls/withholding_23_ret50.xml`
- `addons/l10n_it_edi/tests/export_xmls/withholding_tax_invoice.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_enasa.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_pfun2.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_pfun3.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_pfund.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_ret20.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_ret50.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT00470550013_withh.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567888_FPR01.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567889_FPR03.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_DISC1.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPMAP.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR01.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR01.xml.p7m`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR02.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR03.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR04.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567890_FPR05.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567891_FPR01.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01234567892_FPR01.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01654010345_10099.xml`
- `addons/l10n_it_edi/tests/import_xmls/IT01654010345_10099.xml.p7m`
- `addons/l10n_it_edi/tests/import_xmls/IT09633951000_NpFwF.xml.p7m`
- `addons/l10n_it_edi/tests/test_account_move_document_type.py`
- `addons/l10n_it_edi/tests/test_account_move_payment_method.py`
- `addons/l10n_it_edi/tests/test_account_move_send.py`
- `addons/l10n_it_edi/tests/test_download_docs.py`
- `addons/l10n_it_edi/tests/test_edi_address.py`
- `addons/l10n_it_edi/tests/test_edi_export.py`
- `addons/l10n_it_edi/tests/test_edi_import.py`
- `addons/l10n_it_edi/tests/test_edi_pa.py`
- `addons/l10n_it_edi/tests/test_edi_reverse_charge.py`
- `addons/l10n_it_edi/tests/test_it_document_type.py`
- `addons/l10n_it_edi/tests/test_res_partner.py`
- `addons/l10n_it_edi/tests/test_withholding.py`
- `addons/l10n_it_edi/tools/__init__.py`
- `addons/l10n_it_edi/tools/remove_signature.py`
- `addons/l10n_it_edi/views/account_payment_method.xml`
- `addons/l10n_it_edi/views/account_tax_view.xml`
- `addons/l10n_it_edi/views/l10n_it_document_type.xml`
- `addons/l10n_it_edi/views/l10n_it_view.xml`
- `addons/l10n_it_edi/views/portal_address_templates.xml`
- `addons/l10n_it_edi/views/report_invoice.xml`
- `addons/l10n_it_edi/views/res_config_settings_views.xml`
- `addons/l10n_it_edi/wizard/__init__.py`
- `addons/l10n_it_edi/wizard/account_payment_register.py`
