# Module: l10n_uy

- **Module ID:** MOD-338
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_uy`
- **Manifest:** `addons/l10n_uy/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

General Chart of Accounts.
==========================

This module adds accounting functionalities for the Uruguayan localization, representing the minimum required configuration for a company to operate in Uruguay under the regulations and guidelines provided by the DGI (Dirección General Impositiva).

Among the functionalities are:

* Uruguayan Generic Chart of Account
* Pre-configured VAT Taxes and Tax Groups.
* Legal document types in Uruguay.
* Valid contact identification types in Uruguay.
* Configuration and activation of Uruguayan Currencies  (UYU, UYI - Unidad Indexada Uruguaya).
* Frequently used default contacts already configured: DGI, Consumidor Final Uruguayo.

Configuration
-------------

Demo data for testing:

* Uruguayan company named "UY Company" with the Uruguayan chart of accounts already installed, pre configured taxes, document types and identification types.
* Uruguayan contacts for testing:

   * IEB Internacional
   * Consumidor Final Anónimo Uruguayo.

**Scope evidence:** The module contains 33 files, including 16 Python, 9 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_latam_invoice_document`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 32 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_uy/demo/account_demo.py:11`, `addons/l10n_uy/models/res_partner.py:10`, `addons/l10n_uy/models/account_tax.py:5`, `addons/l10n_uy/models/l10n_latam_document_type.py:7`, `addons/l10n_uy/models/template_uy.py:6`, `addons/l10n_uy/models/account_move.py:16`, `addons/l10n_uy/models/res_company.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 0 JavaScript/TypeScript files; static XML analysis found 62 record/template/menu identifiers.
- **Evidence:** `addons/l10n_uy/demo/demo_company.xml:3`, `addons/l10n_uy/demo/demo_company.xml:16`, `addons/l10n_uy/demo/res_currency_rate_demo.xml:4`, `addons/l10n_uy/demo/res_partner_demo.xml:5`, `addons/l10n_uy/demo/account_supplier_refund_demo.xml:5`, `addons/l10n_uy/demo/account_supplier_refund_demo.xml:17`, `addons/l10n_uy/demo/account_supplier_refund_demo.xml:29`, `addons/l10n_uy/demo/account_customer_refund_demo.xml:5`, `addons/l10n_uy/demo/account_customer_refund_demo.xml:15`, `addons/l10n_uy/demo/account_customer_refund_demo.xml:26`, `addons/l10n_uy/demo/account_customer_refund_demo.xml:37`, `addons/l10n_uy/data/account_tax_report_data.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_uy/tests/test_check_vat.py`, `addons/l10n_uy/tests/__init__.py`, `addons/l10n_uy/tests/test_doc_types.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `base.partner_demo_company_uy`, `base.demo_company_uy`, `rateUSD`, `partner_dgi`, `demo_sup_refund_invoice_3`, `demo_sup_refund_invoice_2`, `demo_sup_refund_invoice_1`, `demo_refund_invoice_1`, `demo_refund_invoice_2`, `demo_refund_invoice_3`, `demo_refund_invoice_4`, `tax_report`, `tax_report_balance`, `account_tax_report_base_impb`, `account_tax_report_base_impb_cmprs`, `account_tax_report_base_impb_cmprs_22`, `account_tax_report_base_impb_cmprs_22_tag`, `account_tax_report_base_impb_cmprs_10`, `account_tax_report_base_impb_cmprs_10_tag`, `account_tax_report_base_impb_cmprs_0`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_uy/views/account_tax_views.xml:6`, `addons/l10n_uy/views/account_tax_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_uy/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `account.chart.template` (addons/l10n_uy/demo/account_demo.py:11); inherits `res.partner` (addons/l10n_uy/models/res_partner.py:10); inherits `account.tax` (addons/l10n_uy/models/account_tax.py:5); inherits `l10n_latam.document.type` (addons/l10n_uy/models/l10n_latam_document_type.py:7); inherits `account.chart.template` (addons/l10n_uy/models/template_uy.py:6); inherits `account.move` (addons/l10n_uy/models/account_move.py:16); inherits `res.company` (addons/l10n_uy/models/res_company.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `l10n_latam_invoice_document`
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

- `addons/l10n_uy/__init__.py`
- `addons/l10n_uy/__manifest__.py`
- `addons/l10n_uy/data/account_tax_report_data.xml`
- `addons/l10n_uy/data/l10n_latam.document.type.csv`
- `addons/l10n_uy/data/res_currency_data.xml`
- `addons/l10n_uy/data/res_partner_data.xml`
- `addons/l10n_uy/data/template/account.account-uy.csv`
- `addons/l10n_uy/data/template/account.depreciation.model-uy.csv`
- `addons/l10n_uy/data/template/account.fiscal.position-uy.csv`
- `addons/l10n_uy/data/template/account.tax-uy.csv`
- `addons/l10n_uy/data/template/account.tax.group-uy.csv`
- `addons/l10n_uy/demo/__init__.py`
- `addons/l10n_uy/demo/account_customer_refund_demo.xml`
- `addons/l10n_uy/demo/account_demo.py`
- `addons/l10n_uy/demo/account_supplier_refund_demo.xml`
- `addons/l10n_uy/demo/demo_company.xml`
- `addons/l10n_uy/demo/res_currency_rate_demo.xml`
- `addons/l10n_uy/demo/res_partner_demo.xml`
- `addons/l10n_uy/i18n/es_419.po`
- `addons/l10n_uy/i18n/l10n_uy.pot`
- `addons/l10n_uy/models/__init__.py`
- `addons/l10n_uy/models/account_move.py`
- `addons/l10n_uy/models/account_tax.py`
- `addons/l10n_uy/models/l10n_latam_document_type.py`
- `addons/l10n_uy/models/res_company.py`
- `addons/l10n_uy/models/res_partner.py`
- `addons/l10n_uy/models/template_uy.py`
- `addons/l10n_uy/tests/__init__.py`
- `addons/l10n_uy/tests/test_check_vat.py`
- `addons/l10n_uy/tests/test_doc_types.py`
- `addons/l10n_uy/tools/__init__.py`
- `addons/l10n_uy/tools/partner_identifiers.py`
- `addons/l10n_uy/views/account_tax_views.xml`
