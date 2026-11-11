# Module: l10n_ec

- **Module ID:** MOD-168
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ec`
- **Manifest:** `addons/l10n_ec/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Functional
----------

This module adds accounting features for Ecuadorian localization, which
represent the minimum requirements to operate a business in Ecuador in compliance
with local regulation bodies such as the ecuadorian tax authority -SRI- and the
Superintendency of Companies -Super Intendencia de Compañías-

Follow the next configuration steps:
1. Go to your company and configure your country as Ecuador
2. Install the invoicing or accounting module, everything will be handled automatically

Highlights:
* Ecuadorian chart of accounts will be automatically installed, based on example provided by Super Intendencia de Compañías
* List of taxes (including withholds) will also be installed, you can switch off the ones your company doesn't use
* Fiscal position, document types, list of local banks, list of local states, etc, will also be installed

Technical
---------
Master Data:
* Chart of Accounts, based on recomendation by Super Cías
* Ecuadorian Taxes, Tax Tags, and Tax Groups
* Ecuadorian Fiscal Positions
* Document types (there are about 41 purchase documents types in Ecuador)
* Identification types
* Ecuador banks
* Partners: Consumidor Final, SRI, IESS, and also basic VAT validation

**Scope evidence:** The module contains 39 files, including 18 Python, 9 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `account_debit_note`, `l10n_latam_invoice_document`, `account`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 9
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ec/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 23 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_ec/demo/account_demo.py:5`, `addons/l10n_ec/models/res_partner.py:33`, `addons/l10n_ec/models/template_ec.py:6`, `addons/l10n_ec/models/account_journal.py:4`, `addons/l10n_ec/models/account_tax.py:7`, `addons/l10n_ec/models/l10n_ec_sri_payment.py:7`, `addons/l10n_ec/models/l10n_latam_document_type.py:8`, `addons/l10n_ec/models/account_move.py:129`, `addons/l10n_ec/models/account_tax_group.py:27`, `addons/l10n_ec/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 0 JavaScript/TypeScript files; static XML analysis found 662 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ec/demo/demo_company.xml:3`, `addons/l10n_ec/demo/demo_company.xml:16`, `addons/l10n_ec/data/account_tax_report_data.xml:3`, `addons/l10n_ec/data/account_tax_report_data.xml:10`, `addons/l10n_ec/data/account_tax_report_data.xml:17`, `addons/l10n_ec/data/account_tax_report_data.xml:22`, `addons/l10n_ec/data/account_tax_report_data.xml:26`, `addons/l10n_ec/data/account_tax_report_data.xml:31`, `addons/l10n_ec/data/account_tax_report_data.xml:38`, `addons/l10n_ec/data/account_tax_report_data.xml:42`, `addons/l10n_ec/data/account_tax_report_data.xml:49`, `addons/l10n_ec/data/account_tax_report_data.xml:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ec/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ec/tests/__init__.py`, `addons/l10n_ec/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `base.partner_demo_company_ec`, `base.demo_company_ec`, `tax_report_104`, `tax_report_104_balance`, `tax_report_line_parent_line_report_1`, `tax_report_line_parent_line_report_2`, `tax_report_line_104_401`, `tax_report_line_104_401_tag`, `tax_report_line_104_411`, `tax_report_line_104_411_tag`, `tax_report_line_104_421`, `tax_report_line_104_421_tag`, `tax_report_line_parent_line_report_6`, `tax_report_line_104_402`, `tax_report_line_104_402_tag`, `tax_report_line_104_412`, `tax_report_line_104_412_tag`, `tax_report_line_104_422`, `tax_report_line_104_422_tag`, `tax_report_line_parent_line_report_7`
- Menus: 2; representative evidence: `addons/l10n_ec/views/root_sri_menu.xml:3`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:43`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 16; representative evidence: `addons/l10n_ec/views/l10n_ec_sri_payment.xml:6`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:8`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:23`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:25`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:37`, `addons/l10n_ec/views/l10n_ec_sri_payment.xml:38`, `addons/l10n_ec/views/res_partner_view.xml:5`, `addons/l10n_ec/views/res_partner_view.xml:7`, `addons/l10n_ec/views/account_tax_view.xml:5`, `addons/l10n_ec/views/account_tax_view.xml:7`, `addons/l10n_ec/views/account_journal_view.xml:5`, `addons/l10n_ec/views/account_journal_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ec/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ec/demo/account_demo.py:5); inherits `res.partner` (addons/l10n_ec/models/res_partner.py:33); inherits `account.chart.template` (addons/l10n_ec/models/template_ec.py:6); inherits `account.journal` (addons/l10n_ec/models/account_journal.py:4); inherits `account.tax` (addons/l10n_ec/models/account_tax.py:7); `l10n_ec.sri.payment` (addons/l10n_ec/models/l10n_ec_sri_payment.py:7); inherits `l10n_latam.document.type` (addons/l10n_ec/models/l10n_latam_document_type.py:8); inherits `account.move` (addons/l10n_ec/models/account_move.py:129); inherits `account.tax.group` (addons/l10n_ec/models/account_tax_group.py:27); inherits `res.company` (addons/l10n_ec/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `account_debit_note`, `l10n_latam_invoice_document`, `account`
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

- `addons/l10n_ec/__init__.py`
- `addons/l10n_ec/__manifest__.py`
- `addons/l10n_ec/data/account_tax_report_data.xml`
- `addons/l10n_ec/data/l10n_ec.sri.payment.csv`
- `addons/l10n_ec/data/l10n_latam.document.type.csv`
- `addons/l10n_ec/data/res_partner_data.xml`
- `addons/l10n_ec/data/template/account.account-ec.csv`
- `addons/l10n_ec/data/template/account.depreciation.model-ec.csv`
- `addons/l10n_ec/data/template/account.fiscal.position-ec.csv`
- `addons/l10n_ec/data/template/account.tax-ec.csv`
- `addons/l10n_ec/data/template/account.tax.group-ec.csv`
- `addons/l10n_ec/demo/__init__.py`
- `addons/l10n_ec/demo/account_demo.py`
- `addons/l10n_ec/demo/demo_company.xml`
- `addons/l10n_ec/i18n/es_419.po`
- `addons/l10n_ec/i18n/l10n_ec.pot`
- `addons/l10n_ec/models/__init__.py`
- `addons/l10n_ec/models/account_journal.py`
- `addons/l10n_ec/models/account_move.py`
- `addons/l10n_ec/models/account_tax.py`
- `addons/l10n_ec/models/account_tax_group.py`
- `addons/l10n_ec/models/l10n_ec_sri_payment.py`
- `addons/l10n_ec/models/l10n_latam_document_type.py`
- `addons/l10n_ec/models/res_company.py`
- `addons/l10n_ec/models/res_partner.py`
- `addons/l10n_ec/models/template_ec.py`
- `addons/l10n_ec/security/ir.access.csv`
- `addons/l10n_ec/static/img/logo_iess.png`
- `addons/l10n_ec/static/img/logo_sri.png`
- `addons/l10n_ec/tests/__init__.py`
- `addons/l10n_ec/tests/test_account_move.py`
- `addons/l10n_ec/tools/__init__.py`
- `addons/l10n_ec/tools/partner_identifiers.py`
- `addons/l10n_ec/views/account_journal_view.xml`
- `addons/l10n_ec/views/account_tax_view.xml`
- `addons/l10n_ec/views/l10n_ec_sri_payment.xml`
- `addons/l10n_ec/views/l10n_latam_document_type_view.xml`
- `addons/l10n_ec/views/res_partner_view.xml`
- `addons/l10n_ec/views/root_sri_menu.xml`
