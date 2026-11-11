# Module: account_edi_ubl_cii

- **Module ID:** MOD-006
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_edi_ubl_cii`
- **Manifest:** `addons/account_edi_ubl_cii/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Electronic invoicing module
===========================

Allows to export and import formats: E-FFF, UBL Bis 3, EHF3, NLCIUS, Factur-X (CII), XRechnung (UBL).
When generating the PDF on the invoice, the PDF will be embedded inside the xml for all UBL formats. This allows the
receiver to retrieve the PDF with only the xml file. Note that **EHF3 is fully implemented by UBL Bis 3** (`reference
<https://anskaffelser.dev/postaward/g3/spec/current/billing-3.0/norway/#_implementation>`_).

Note that E-FFF, NLCIUS and XRechnung (UBL) are only available for Belgian, Dutch and German companies,
respectively. UBL Bis 3 is only available for companies which country is present in the `EAS list
<https://docs.peppol.eu/poacc/billing/3.0/codelist/eas/>`_.

**Scope evidence:** The module contains 323 files, including 73 Python, 198 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 23
- Controller/API files: 0
- XML/data/view/template files: 198
- Browser asset files: 0
- Security files: 0
- Test files: 36
- Scheduled/automation evidence files: 1
- Reporting evidence files: 7

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 23 model declarations, 1028 methods, 0 constraint handlers, 1 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/account_edi_ubl_cii/models/res_partner.py:15`, `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_20.py:20`, `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_efff.py:8`, `addons/account_edi_ubl_cii/models/uom_uom.py:4`, `addons/account_edi_ubl_cii/models/account_edi_xml_cii_facturx.py:28`, `addons/account_edi_ubl_cii/models/account_edi_ubl_cen_en16931.py:6`, `addons/account_edi_ubl_cii/models/ir_actions_report.py:6`, `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_nlcius.py:6`, `addons/account_edi_ubl_cii/models/account_tax.py:4`, `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_21.py:4`, `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_sg.py:5`, `addons/account_edi_ubl_cii/models/account_edi_ubl_pint.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 198 XML files and 0 JavaScript/TypeScript files; static XML analysis found 45 record/template/menu identifiers.
- **Evidence:** `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:92`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:3`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:25`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:55`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:88`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:4`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:104`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:132`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:149`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:346`, `addons/account_edi_ubl_cii/data/ir_config_parameter_data.xml:4`, `addons/account_edi_ubl_cii/data/uom_data.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account_edi_ubl_cii/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 7 files contain report-action/template indicators.
- **Evidence:** `addons/account_edi_ubl_cii/models/ir_actions_report.py`, `addons/account_edi_ubl_cii/models/account_edi_common.py`, `addons/account_edi_ubl_cii/models/account_edi_ubl.py`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml`, `addons/account_edi_ubl_cii/tests/common.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_auto_generate_pdf.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 36 test files are present.
- **Evidence:** `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_group_lines_by_tax.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_retrieve_analytic_distribution.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_retrieve_product.py`, `addons/account_edi_ubl_cii/tests/test_cii_export_facturx_fr.py`, `addons/account_edi_ubl_cii/tests/test_ubl_export_bis3_debit_note.py`, `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr.py`, `addons/account_edi_ubl_cii/tests/test_ubl_export_bis3_invoice_be_down_payment.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_retrieve_vehicle.py`, `addons/account_edi_ubl_cii/tests/test_autopost_bills.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_group_lines_by_tax.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_retrieve_tax.py`, `addons/account_edi_ubl_cii/tests/test_cii_facturx_fr_decode_invoice_line.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 198; representative identifiers: `action_report_account_invoices_generated_by_odoo`, `account_invoices_generated_by_odoo`, `report_invoice_document`, `layout_invoices_generated_by_odoo`, `external_layout_with_context`, `account_invoice_line_facturx_export_22`, `account_invoice_partner_facturx_export_22`, `account_invoice_address_facturx_export_22`, `account_invoice_facturx_export_22`, `account_invoice_pdfa_3_facturx_metadata`, `disable_pdf_in_xml`, `uom.product_uom_unit`, `uom.product_uom_dozen`, `uom.product_uom_kgm`, `uom.product_uom_gram`, `uom.product_uom_day`, `uom.product_uom_hour`, `uom.product_uom_minute`, `uom.product_uom_ton`, `uom.product_uom_meter`
- Menus: 0; representative evidence: Not found in module
- Templates: 9; representative evidence: `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:3`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:25`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:55`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:88`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:4`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:104`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:132`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:149`, `addons/account_edi_ubl_cii/data/cii_22_templates.xml:346`
- View/action field declarations: 7; representative evidence: `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml:94`, `addons/account_edi_ubl_cii/views/uom_uom_views.xml:5`, `addons/account_edi_ubl_cii/views/uom_uom_views.xml:7`, `addons/account_edi_ubl_cii/views/account_tax_views.xml:5`, `addons/account_edi_ubl_cii/views/account_tax_views.xml:7`, `addons/account_edi_ubl_cii/views/res_partner_views.xml:4`, `addons/account_edi_ubl_cii/views/res_partner_views.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_edi_ubl_cii/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/account_edi_ubl_cii/views/account_move_views.xml`
- **Report entry points:** `addons/account_edi_ubl_cii/models/ir_actions_report.py`, `addons/account_edi_ubl_cii/models/account_edi_common.py`, `addons/account_edi_ubl_cii/models/account_edi_ubl.py`, `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml`, `addons/account_edi_ubl_cii/tests/common.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be.py`, `addons/account_edi_ubl_cii/tests/test_ubl_import_bis3_invoice_be_auto_generate_pdf.py`

## 7. Database interactions

- Model declarations: 23
- Representative model evidence: inherits `res.partner` (addons/account_edi_ubl_cii/models/res_partner.py:15); `account.edi.xml.ubl_20` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_20.py:20); `account.edi.xml.ubl_efff` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_efff.py:8); inherits `uom.uom` (addons/account_edi_ubl_cii/models/uom_uom.py:4); `account.edi.xml.cii` (addons/account_edi_ubl_cii/models/account_edi_xml_cii_facturx.py:28); `account.edi.ubl_cen_en16931` (addons/account_edi_ubl_cii/models/account_edi_ubl_cen_en16931.py:6); inherits `ir.actions.report` (addons/account_edi_ubl_cii/models/ir_actions_report.py:6); `account.edi.xml.ubl_nl` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_nlcius.py:6); inherits `account.tax` (addons/account_edi_ubl_cii/models/account_tax.py:4); `account.edi.xml.ubl_21` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_21.py:4); `account.edi.xml.ubl_sg` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_sg.py:5); `account.edi.ubl_pint` (addons/account_edi_ubl_cii/models/account_edi_ubl_pint.py:7); `account.edi.ubl_pint_eu` (addons/account_edi_ubl_cii/models/account_edi_ubl_pint_eu.py:6); inherits `account.move` (addons/account_edi_ubl_cii/models/account_move.py:13); `account.edi.common` (addons/account_edi_ubl_cii/models/account_edi_common.py:185); `account.edi.xml.ubl_de` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_xrechnung.py:5); inherits `account.move.send` (addons/account_edi_ubl_cii/models/account_move_send.py:16); `account.edi.xml.ubl_bis3` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_bis3.py:13); `account.edi.ubl` (addons/account_edi_ubl_cii/models/account_edi_ubl.py:34); `account.edi.cii` (addons/account_edi_ubl_cii/models/account_edi_cii.py:18); `account.edi.xml.ubl_a_nz` (addons/account_edi_ubl_cii/models/account_edi_xml_ubl_a_nz.py:6); inherits `res.company` (addons/account_edi_ubl_cii/models/res_company.py:4); inherits `account.move.send.wizard` (addons/account_edi_ubl_cii/wizard/account_move_send_wizard.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
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

- `addons/account_edi_ubl_cii/__init__.py`
- `addons/account_edi_ubl_cii/__manifest__.py`
- `addons/account_edi_ubl_cii/data/cii_22_templates.xml`
- `addons/account_edi_ubl_cii/data/ir_config_parameter_data.xml`
- `addons/account_edi_ubl_cii/data/uom_data.xml`
- `addons/account_edi_ubl_cii/i18n/account_edi_ubl_cii.pot`
- `addons/account_edi_ubl_cii/i18n/ar.po`
- `addons/account_edi_ubl_cii/i18n/az.po`
- `addons/account_edi_ubl_cii/i18n/bg.po`
- `addons/account_edi_ubl_cii/i18n/bs.po`
- `addons/account_edi_ubl_cii/i18n/ca.po`
- `addons/account_edi_ubl_cii/i18n/cs.po`
- `addons/account_edi_ubl_cii/i18n/da.po`
- `addons/account_edi_ubl_cii/i18n/de.po`
- `addons/account_edi_ubl_cii/i18n/el.po`
- `addons/account_edi_ubl_cii/i18n/es.po`
- `addons/account_edi_ubl_cii/i18n/es_419.po`
- `addons/account_edi_ubl_cii/i18n/et.po`
- `addons/account_edi_ubl_cii/i18n/fa.po`
- `addons/account_edi_ubl_cii/i18n/fi.po`
- `addons/account_edi_ubl_cii/i18n/fr.po`
- `addons/account_edi_ubl_cii/i18n/fr_BE.po`
- `addons/account_edi_ubl_cii/i18n/he.po`
- `addons/account_edi_ubl_cii/i18n/hi.po`
- `addons/account_edi_ubl_cii/i18n/hr.po`
- `addons/account_edi_ubl_cii/i18n/hu.po`
- `addons/account_edi_ubl_cii/i18n/id.po`
- `addons/account_edi_ubl_cii/i18n/it.po`
- `addons/account_edi_ubl_cii/i18n/ja.po`
- `addons/account_edi_ubl_cii/i18n/kab.po`
- `addons/account_edi_ubl_cii/i18n/ko.po`
- `addons/account_edi_ubl_cii/i18n/ku.po`
- `addons/account_edi_ubl_cii/i18n/lo.po`
- `addons/account_edi_ubl_cii/i18n/lt.po`
- `addons/account_edi_ubl_cii/i18n/lv.po`
- `addons/account_edi_ubl_cii/i18n/mn.po`
- `addons/account_edi_ubl_cii/i18n/my.po`
- `addons/account_edi_ubl_cii/i18n/nb.po`
- `addons/account_edi_ubl_cii/i18n/nl.po`
- `addons/account_edi_ubl_cii/i18n/pl.po`
- `addons/account_edi_ubl_cii/i18n/pt.po`
- `addons/account_edi_ubl_cii/i18n/pt_BR.po`
- `addons/account_edi_ubl_cii/i18n/ro.po`
- `addons/account_edi_ubl_cii/i18n/ru.po`
- `addons/account_edi_ubl_cii/i18n/sk.po`
- `addons/account_edi_ubl_cii/i18n/sl.po`
- `addons/account_edi_ubl_cii/i18n/sr@latin.po`
- `addons/account_edi_ubl_cii/i18n/sv.po`
- `addons/account_edi_ubl_cii/i18n/th.po`
- `addons/account_edi_ubl_cii/i18n/tr.po`
- `addons/account_edi_ubl_cii/i18n/uk.po`
- `addons/account_edi_ubl_cii/i18n/uz.po`
- `addons/account_edi_ubl_cii/i18n/vi.po`
- `addons/account_edi_ubl_cii/i18n/zh_CN.po`
- `addons/account_edi_ubl_cii/i18n/zh_TW.po`
- `addons/account_edi_ubl_cii/models/__init__.py`
- `addons/account_edi_ubl_cii/models/account_edi_cii.py`
- `addons/account_edi_ubl_cii/models/account_edi_common.py`
- `addons/account_edi_ubl_cii/models/account_edi_ubl.py`
- `addons/account_edi_ubl_cii/models/account_edi_ubl_cen_en16931.py`
- `addons/account_edi_ubl_cii/models/account_edi_ubl_pint.py`
- `addons/account_edi_ubl_cii/models/account_edi_ubl_pint_eu.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_cii_facturx.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_20.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_21.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_a_nz.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_bis3.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_efff.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_nlcius.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_sg.py`
- `addons/account_edi_ubl_cii/models/account_edi_xml_ubl_xrechnung.py`
- `addons/account_edi_ubl_cii/models/account_move.py`
- `addons/account_edi_ubl_cii/models/account_move_send.py`
- `addons/account_edi_ubl_cii/models/account_tax.py`
- `addons/account_edi_ubl_cii/models/ir_actions_report.py`
- `addons/account_edi_ubl_cii/models/res_company.py`
- `addons/account_edi_ubl_cii/models/res_partner.py`
- `addons/account_edi_ubl_cii/models/uom_uom.py`
- `addons/account_edi_ubl_cii/report/account_edi_ubl_cii_report_templates.xml`
- `addons/account_edi_ubl_cii/static/src/scss/account_edi_ubl_cii.scss`
- `addons/account_edi_ubl_cii/tests/__init__.py`
- `addons/account_edi_ubl_cii/tests/common.py`
- `addons/account_edi_ubl_cii/tests/test_addresses.py`
- `addons/account_edi_ubl_cii/tests/test_autopost_bills.py`
- `addons/account_edi_ubl_cii/tests/test_cii_export_facturx_fr.py`
- `addons/account_edi_ubl_cii/tests/test_cii_facturx_fr_decode_invoice_line.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_cash_rounding.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_group_lines_by_tax.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_retrieve_account.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_retrieve_analytic_distribution.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_retrieve_partner.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_retrieve_product.py`
- `addons/account_edi_ubl_cii/tests/test_cii_import_facturx_fr_retrieve_tax.py`
- `addons/account_edi_ubl_cii/tests/test_download_docs.py`
- `addons/account_edi_ubl_cii/tests/test_files/bis3_bill_group_by_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/bis3_bill_vehicle_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/debit_note/be/test_export_debit_note.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/debit_note/ignore_schema.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_BR_CO_10_line_extension_amount_sum_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_BR_E_08_line_extension_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_BR_S_08_tax_subtotal_taxable_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_PEPPOL_EN16931_R120_line_extension_amount_huge_number_of_decimals.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_allowance_charge_custom_tax_recycling_contribution.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_allowance_charge_fixed_tax_recycling_contribution.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_cash_rounding_add_invoice_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_cash_rounding_biggest_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_custom_tax_emptying_turned_as_extra_invoice_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_be_invoice_address.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_be_only_eas_endpoint.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_be_vat.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_be_vat_and_company_registry.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_be_vat_and_ref.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_lu_company_registry.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_lu_only_vat.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_nl_vat_eas_kvk_company_registry.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_nl_vat_eas_oin_company_registry.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_nl_vat_kvk_eas.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_customer_party_identifiers_partner_nl_vat_oin_eas.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_early_pay_discount_multiple_taxes.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_early_pay_discount_with_0_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_early_pay_discount_with_discount_on_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_early_pay_discount_with_recycling_contribution_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_export_sections_as_invoice_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_export_sections_with_price_included_taxes.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_fixed_tax_emptying_return_turned_as_extra_invoice_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_fixed_tax_emptying_turned_as_extra_invoice_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_item_description_name.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_manual_tax_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_multiple_fixed_tax_emptying_turned_as_extra_invoice_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_negative_discount_upsell.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_negative_price_unit.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_payee_financial_account.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_payment_mandate_active.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_payment_mandate_expired.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_price_amount_rounding_precision_with_price_included_taxes.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_price_amount_rounding_precision_with_price_included_taxes_plus_free_product.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_price_unit_more_decimals.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_product_commodity_code_cpv.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_product_commodity_code_intrastat.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_product_commodity_code_unspsc.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_send_and_print_additional_documents.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_sent_to_luxembourg_dig.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_sent_to_partner_with_gln.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_currency_code_tax_totals_foreign_currency.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_exempt.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_out_of_scope.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_subtotal_exempt_amount_round_globally.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_subtotal_exempt_amount_round_per_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_tax_withholding.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_with_discount_and_fixed_tax_emptying_return.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_with_fixed_tax_on_negative_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_with_global_discount_line_sale_order.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_invoice_with_vehicle_license_plate.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/be/test_sale_order_down_payment_first_invoice.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice/ignore_schema.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/be/test_credit_note_self_billing_payment_mandate_active.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/be/test_credit_note_self_billing_payment_mandate_expired.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/be/test_credit_note_selfbilling.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/be/test_invoice_selfbilling.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/be/test_invoice_selfbilling_reverse_charge.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/bis3/invoice_selfbilling/ignore_schema.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_allowance_charge_fixed_tax_included_recycling_contribution.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_allowance_charge_fixed_tax_recycling_contribution.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_cash_rounding_add_invoice_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_cash_rounding_biggest_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_deferred_dates.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_deferred_dates_on_some_lines.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_deferred_dates_on_some_lines_with_delivery_date.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_delivery_date_and_address.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_document_header.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_early_pay_discount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_end_following_month_payment_term.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_financial_account_bank.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_financial_account_iban.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_global_location_number.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_immediate_payment_term.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_in_foreign_currency.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_multiple_taxes.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_negative_price_unit.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_partner_info.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_partner_siret.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_price_amount_rounding_precision.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_price_amount_rounding_precision_with_price_included_taxes.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_product_description_name.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_product_uom_and_discounts.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_tax_included.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_tax_withholding.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_with_chorus_pro_fields.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_with_fixed_tax_on_negative_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/export/facturx/invoice/fr/test_invoice_without_chorus_pro_fields.xml`
- `addons/account_edi_ubl_cii/tests/test_files/facturx_out_invoice.xml`
- `addons/account_edi_ubl_cii/tests/test_files/facturx_out_invoice_abnormal.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_bill_endpoint_in_party_tax_scheme.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_bill_multiple_payment_means.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_bill_vat_in_party_identification.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_cash_rounding_add_invoice_line.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_cash_rounding_biggest_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_credit_note_optional_fields.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_discount_per_line_price_on_big_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_document_charge_tax_alignment.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_embedded_pdf.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_auto_generate_pdf.pdf`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_auto_generate_pdf.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_discount_on_price_zero.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_fixed_tax_fuzzy.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_group_lines_by_tax.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_group_lines_correct_tax_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_line_quantity_decimals.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_invoice_optional_fields.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_lot_of_decimals_in_quantities.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_partner_creation.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_partner_creation_ch.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_partner_creation_email.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_partner_vat_in_other_country.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_payable_rounding_amount_not_being_cash_rounding.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_import_without_embedded_attachment.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_invoice_two_tax_subtotals_because_of_multi_currency.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_account_invoice_predictive.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_credit_note_payment_due_date.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_empty_description.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_full_price_node_and_invoiced_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_full_price_node_no_invoiced_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_price_allowance_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_price_allowance_base_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_price_allowance_base_amount_and_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_price_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_zero_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_line_extension_amount_zero_quantity_zero_price_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_name.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_name_and_description.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_negative_lines_and_total.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_negative_with_base_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_price_amount_base_quantity.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_zero_line_extension_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_zero_line_extension_amount_with_quantity_allowance_charge.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_invoice_line_zero_line_extension_amount_zero_quantity_with_price_amount.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_partner_retrieval_bank_account_number.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_partner_retrieval_own_bank_account_number.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_barcode.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_by_supplier_info.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_by_supplier_info_as_first_preference.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_default_code.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_description.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_invoice_predictive.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_name.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_product_uom_category_mismatch.xml`
- `addons/account_edi_ubl_cii/tests/test_files/import/bis3/invoice/be/test_partial_import_tax_charge_to_fixed_tax.xml`
- Additional source files not expanded in this page: 73; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
