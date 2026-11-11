# Module: l10n_ar

- **Module ID:** MOD-120
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ar`
- **Manifest:** `addons/l10n_ar/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Functional
----------

This module add accounting features for the Argentinean localization, which represent the minimal configuration needed for a company  to operate in Argentina and under the ARCA (Administración Federal de Ingresos Públicos) regulations and guidelines.

Follow the next configuration steps for Production:

1. Go to your company and configure your VAT number and ARCA Responsibility Type
2. Go to Accounting / Settings and set the Chart of Account that you will like to use.
3. Create your Sale journals taking into account ARCA POS info.

Demo data for testing:

* 3 companies were created, one for each ARCA responsibility type with the respective Chart of Account installed. Choose the company that fix you in order to make tests:

  * (AR) Responsable Inscripto
  * (AR) Exento
  * (AR) Monotributo

* Journal sales configured to Pre printed and Expo invoices in all companies
* Invoices and other documents examples already validated in “(AR) Responsable Inscripto” company
* Partners example for the different responsibility types:

  * ADHOC (IVA Responsable Inscripto)
  * Servicios Globales (IVA Sujeto Exento)
  * Gritti (Monotributo)
  * Montana Sur. IVA Liberado in Zona Franca
  * Barcelona food (Cliente del Exterior)
  * Odoo (Proveedor del Exterior)

Highlights:

* Chart of account will not be automatically installed, each CoA Template depends on the ARCA Responsibility of the company, you will need to install the CoA for your needs.
* No sales journals will be generated when installing a CoA, you will need to configure your journals manually.
* The Document type will be properly pre selected when creating an invoice depending on the fiscal responsibility of the issuer and receiver of the document and the related journal.
* A CBU account type has been added and also CBU Validation


Technical
---------

This module adds both models and fields that will be eventually used for the electronic invoice module. Here is a summary of the main features:

Master Data:

* Chart of Account: one for each ARCA responsibility that is related to a legal entity:

  * Responsable Inscripto (RI)
  * Exento (EX)
  * Monotributo (Mono)

* Argentinean Taxes and Account Tax Groups (VAT taxes with the existing aliquots and other types)
* ARCA Responsibility Types
* Fiscal Positions (in order to map taxes)
* Legal Documents Types in Argentina
* Identification Types valid in Argentina.
* Country ARCA codes and Country VAT codes for legal entities, natural persons and others
* Currency ARCA codes
* Unit of measures ARCA codes
* Partners: Consumidor Final and ARCA

**Scope evidence:** The module contains 90 files, including 35 Python, 32 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_latam_invoice_document`, `account`.

## 2. Module structure

- Model/business logic files: 22
- Controller/API files: 2
- XML/data/view/template files: 32
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ar/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 22 model declarations, 142 methods, 5 constraint handlers, 5 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/l10n_ar/demo/account_demo.py:8`, `addons/l10n_ar/models/res_partner.py:21`, `addons/l10n_ar/models/l10n_ar_arca_activity.py:5`, `addons/l10n_ar/models/uom_uom.py:5`, `addons/l10n_ar/models/res_config_settings.py:5`, `addons/l10n_ar/models/res_currency.py:5`, `addons/l10n_ar/models/template_ar_ri.py:6`, `addons/l10n_ar/models/account_journal.py:7`, `addons/l10n_ar/models/account_account.py:5`, `addons/l10n_ar/models/account_fiscal_position.py:5`, `addons/l10n_ar/models/template_ar_ex.py:6`, `addons/l10n_ar/models/template_ar_base.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/l10n_ar/controllers/portal.py`, `addons/l10n_ar/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 32 XML files and 0 JavaScript/TypeScript files; static XML analysis found 161 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:7`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:24`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:38`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:51`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:64`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:81`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:93`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:106`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:139`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:150`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:159`, `addons/l10n_ar/demo/account_supplier_invoice_demo.xml:182`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ar/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_ar/views/report_invoice.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_ar/tests/common.py`, `addons/l10n_ar/tests/test_manual.py`, `addons/l10n_ar/tests/__init__.py`, `addons/l10n_ar/tests/test_res_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 32; representative identifiers: `demo_sup_invoice_1`, `demo_sup_invoice_2`, `demo_sup_invoice_3`, `demo_sup_invoice_4`, `demo_sup_invoice_5`, `demo_sup_invoice_6`, `demo_sup_invoice_7`, `demo_sup_invoice_8`, `demo_sup_invoice_9`, `demo_sup_invoice_10`, `demo_sup_invoice_11`, `demo_sup_invoice_12`, `demo_liquido_producto_1`, `demo_despacho_1`, `demo_sup_invoice_1`, `demo_sup_invoice_2`, `demo_sup_invoice_3`, `demo_sup_invoice_4`, `demo_sup_invoice_5`, `demo_sup_invoice_6`
- Menus: 7; representative evidence: `addons/l10n_ar/report/invoice_report_view.xml:28`, `addons/l10n_ar/report/invoice_report_view.xml:41`, `addons/l10n_ar/data/account_chart_template_data2.xml:3`, `addons/l10n_ar/views/l10n_ar_arca_activity_view.xml:34`, `addons/l10n_ar/views/l10n_ar_afip_responsibility_type_view.xml:35`, `addons/l10n_ar/views/l10n_latam_document_type_view.xml:49`, `addons/l10n_ar/views/afip_menuitem.xml:4`
- Templates: 5; representative evidence: `addons/l10n_ar/views/report_invoice.xml:5`, `addons/l10n_ar/views/report_invoice.xml:76`, `addons/l10n_ar/views/report_invoice.xml:309`, `addons/l10n_ar/views/report_invoice.xml:317`, `addons/l10n_ar/views/portal_address_templates.xml:4`
- View/action field declarations: 56; representative evidence: `addons/l10n_ar/report/invoice_report_view.xml:6`, `addons/l10n_ar/report/invoice_report_view.xml:8`, `addons/l10n_ar/report/invoice_report_view.xml:23`, `addons/l10n_ar/report/invoice_report_view.xml:24`, `addons/l10n_ar/report/invoice_report_view.xml:36`, `addons/l10n_ar/report/invoice_report_view.xml:37`, `addons/l10n_ar/views/uom_uom_view.xml:6`, `addons/l10n_ar/views/uom_uom_view.xml:8`, `addons/l10n_ar/views/uom_uom_view.xml:17`, `addons/l10n_ar/views/uom_uom_view.xml:19`, `addons/l10n_ar/views/l10n_ar_arca_activity_view.xml:5`, `addons/l10n_ar/views/l10n_ar_arca_activity_view.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ar/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_ar/views/report_invoice.xml`

## 7. Database interactions

- Model declarations: 22
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ar/demo/account_demo.py:8); inherits `res.partner` (addons/l10n_ar/models/res_partner.py:21); `l10n_ar.arca.activity` (addons/l10n_ar/models/l10n_ar_arca_activity.py:5); inherits `uom.uom` (addons/l10n_ar/models/uom_uom.py:5); inherits `res.config.settings` (addons/l10n_ar/models/res_config_settings.py:5); inherits `res.currency` (addons/l10n_ar/models/res_currency.py:5); inherits `account.chart.template` (addons/l10n_ar/models/template_ar_ri.py:6); inherits `account.journal` (addons/l10n_ar/models/account_journal.py:7); inherits `account.account` (addons/l10n_ar/models/account_account.py:5); inherits `account.fiscal.position` (addons/l10n_ar/models/account_fiscal_position.py:5); inherits `account.chart.template` (addons/l10n_ar/models/template_ar_ex.py:6); inherits `account.chart.template` (addons/l10n_ar/models/template_ar_base.py:6); inherits `account.chart.template` (addons/l10n_ar/models/account_chart_template.py:7); inherits `res.country` (addons/l10n_ar/models/res_country.py:6); inherits `l10n_latam.document.type` (addons/l10n_ar/models/l10n_latam_document_type.py:5); inherits `account.move` (addons/l10n_ar/models/account_move.py:11); inherits `account.tax.group` (addons/l10n_ar/models/account_tax_group.py:6); inherits `account.move.line` (addons/l10n_ar/models/account_move_line.py:5); inherits `res.partner.bank` (addons/l10n_ar/models/res_partner_bank.py:11); `l10n_ar.afip.responsibility.type` (addons/l10n_ar/models/l10n_ar_afip_responsibility_type.py:6); inherits `res.company` (addons/l10n_ar/models/res_company.py:5); inherits `account.invoice.report` (addons/l10n_ar/report/invoice_report.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_latam_invoice_document`, `account`
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

- `addons/l10n_ar/__init__.py`
- `addons/l10n_ar/__manifest__.py`
- `addons/l10n_ar/controllers/__init__.py`
- `addons/l10n_ar/controllers/portal.py`
- `addons/l10n_ar/data/account.account.tag.csv`
- `addons/l10n_ar/data/account_chart_template_data2.xml`
- `addons/l10n_ar/data/l10n_ar.arca.activity.csv`
- `addons/l10n_ar/data/l10n_ar_afip_responsibility_type_data.xml`
- `addons/l10n_ar/data/l10n_latam.document.type.csv`
- `addons/l10n_ar/data/l10n_latam.document.type.xml`
- `addons/l10n_ar/data/res.country.csv`
- `addons/l10n_ar/data/res.currency.csv`
- `addons/l10n_ar/data/res_partner_data.xml`
- `addons/l10n_ar/data/template/account.account-ar_base.csv`
- `addons/l10n_ar/data/template/account.account-ar_ex.csv`
- `addons/l10n_ar/data/template/account.account-ar_ri.csv`
- `addons/l10n_ar/data/template/account.depreciation.model-ar_base.csv`
- `addons/l10n_ar/data/template/account.fiscal.position-ar_ri.csv`
- `addons/l10n_ar/data/template/account.tax-ar_base.csv`
- `addons/l10n_ar/data/template/account.tax-ar_ex.csv`
- `addons/l10n_ar/data/template/account.tax-ar_ri.csv`
- `addons/l10n_ar/data/template/account.tax.group-ar_base.csv`
- `addons/l10n_ar/data/template/account.tax.group-ar_ex.csv`
- `addons/l10n_ar/data/template/account.tax.group-ar_ri.csv`
- `addons/l10n_ar/data/uom_uom_data.xml`
- `addons/l10n_ar/demo/__init__.py`
- `addons/l10n_ar/demo/account_customer_invoice_demo.xml`
- `addons/l10n_ar/demo/account_customer_refund_demo.xml`
- `addons/l10n_ar/demo/account_demo.py`
- `addons/l10n_ar/demo/account_supplier_invoice_demo.xml`
- `addons/l10n_ar/demo/account_supplier_refund_demo.xml`
- `addons/l10n_ar/demo/account_tax_demo.xml`
- `addons/l10n_ar/demo/adhoc_jjs.jpeg`
- `addons/l10n_ar/demo/adhoc_logo.png`
- `addons/l10n_ar/demo/exento_demo.xml`
- `addons/l10n_ar/demo/gritti_logo.png`
- `addons/l10n_ar/demo/mono_demo.xml`
- `addons/l10n_ar/demo/odoo_logo.jpg`
- `addons/l10n_ar/demo/product_product_demo.xml`
- `addons/l10n_ar/demo/res_partner_demo.xml`
- `addons/l10n_ar/demo/respinsc_demo.xml`
- `addons/l10n_ar/i18n/es_419.po`
- `addons/l10n_ar/i18n/l10n_ar.pot`
- `addons/l10n_ar/models/__init__.py`
- `addons/l10n_ar/models/account_account.py`
- `addons/l10n_ar/models/account_chart_template.py`
- `addons/l10n_ar/models/account_fiscal_position.py`
- `addons/l10n_ar/models/account_journal.py`
- `addons/l10n_ar/models/account_move.py`
- `addons/l10n_ar/models/account_move_line.py`
- `addons/l10n_ar/models/account_tax_group.py`
- `addons/l10n_ar/models/l10n_ar_afip_responsibility_type.py`
- `addons/l10n_ar/models/l10n_ar_arca_activity.py`
- `addons/l10n_ar/models/l10n_latam_document_type.py`
- `addons/l10n_ar/models/res_company.py`
- `addons/l10n_ar/models/res_config_settings.py`
- `addons/l10n_ar/models/res_country.py`
- `addons/l10n_ar/models/res_currency.py`
- `addons/l10n_ar/models/res_partner.py`
- `addons/l10n_ar/models/res_partner_bank.py`
- `addons/l10n_ar/models/template_ar_base.py`
- `addons/l10n_ar/models/template_ar_ex.py`
- `addons/l10n_ar/models/template_ar_ri.py`
- `addons/l10n_ar/models/uom_uom.py`
- `addons/l10n_ar/report/__init__.py`
- `addons/l10n_ar/report/invoice_report.py`
- `addons/l10n_ar/report/invoice_report_view.xml`
- `addons/l10n_ar/security/ir.access.csv`
- `addons/l10n_ar/tests/__init__.py`
- `addons/l10n_ar/tests/common.py`
- `addons/l10n_ar/tests/test_manual.py`
- `addons/l10n_ar/tests/test_res_partner.py`
- `addons/l10n_ar/tools/__init__.py`
- `addons/l10n_ar/tools/partner_identifiers.py`
- `addons/l10n_ar/views/account_account_view.xml`
- `addons/l10n_ar/views/account_fiscal_position_view.xml`
- `addons/l10n_ar/views/account_journal_view.xml`
- `addons/l10n_ar/views/account_move_view.xml`
- `addons/l10n_ar/views/afip_menuitem.xml`
- `addons/l10n_ar/views/l10n_ar_afip_responsibility_type_view.xml`
- `addons/l10n_ar/views/l10n_ar_arca_activity_view.xml`
- `addons/l10n_ar/views/l10n_latam_document_type_view.xml`
- `addons/l10n_ar/views/portal_address_templates.xml`
- `addons/l10n_ar/views/report_invoice.xml`
- `addons/l10n_ar/views/res_company_view.xml`
- `addons/l10n_ar/views/res_config_settings_view.xml`
- `addons/l10n_ar/views/res_country_view.xml`
- `addons/l10n_ar/views/res_currency_view.xml`
- `addons/l10n_ar/views/res_partner_view.xml`
- `addons/l10n_ar/views/uom_uom_view.xml`
