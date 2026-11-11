# Module: l10n_be

- **Module ID:** MOD-128
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_be`
- **Manifest:** `addons/l10n_be/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Belgium in Odoo.
==============================================================================

After installing this module, the Configuration wizard for accounting is launched.
    * We have the account templates which can be helpful to generate Charts of Accounts.
    * On that particular wizard, you will be asked to pass the name of the company,
      the chart template to follow, the no. of digits to generate, the code for your
      account and bank account, currency to create journals.

Thus, the pure copy of Chart Template is generated.

Wizards provided by this module:
--------------------------------
    * Partner VAT Intra: Enlist the partners with their related VAT and invoiced
      amounts. Prepares an XML file format.

        **Path to access:** Invoicing/Reporting/Legal Reports/Belgium Statements/Partner VAT Intra
    * Periodical VAT Declaration: Prepares an XML file for Vat Declaration of
      the Main company of the User currently Logged in.

        **Path to access:** Invoicing/Reporting/Legal Reports/Belgium Statements/Periodical VAT Declaration
    * Annual Listing Of VAT-Subjected Customers: Prepares an XML file for Vat
      Declaration of the Main company of the User currently Logged in Based on
      Fiscal year.

        **Path to access:** Invoicing/Reporting/Legal Reports/Belgium Statements/Annual Listing Of VAT-Subjected Customers

**Scope evidence:** The module contains 27 files, including 12 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 19 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_be/demo/account_demo.py:5`, `addons/l10n_be/models/template_be_comp.py:7`, `addons/l10n_be/models/account_journal.py:6`, `addons/l10n_be/models/account_tax.py:4`, `addons/l10n_be/models/template_be_asso.py:7`, `addons/l10n_be/models/account_move.py:17`, `addons/l10n_be/models/template_be.py:7`, `addons/l10n_be/models/res_company.py:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 104 record/template/menu identifiers.
- **Evidence:** `addons/l10n_be/demo/demo_company.xml:3`, `addons/l10n_be/demo/demo_company.xml:15`, `addons/l10n_be/demo/demo_company.xml:20`, `addons/l10n_be/data/account_tax_report_data.xml:3`, `addons/l10n_be/data/account_tax_report_data.xml:13`, `addons/l10n_be/data/account_tax_report_data.xml:22`, `addons/l10n_be/data/account_tax_report_data.xml:29`, `addons/l10n_be/data/account_tax_report_data.xml:36`, `addons/l10n_be/data/account_tax_report_data.xml:43`, `addons/l10n_be/data/account_tax_report_data.xml:50`, `addons/l10n_be/data/account_tax_report_data.xml:57`, `addons/l10n_be/data/account_tax_report_data.xml:64`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base.partner_demo_company_be`, `base.demo_company_be`, `base.demo_bank_be`, `tax_report_vat`, `tax_report_vat_balance`, `tax_report_title_operations`, `tax_report_title_operations_sortie`, `tax_report_line_00`, `tax_report_line_00_tag`, `tax_report_line_01`, `tax_report_line_01_tag`, `tax_report_line_02`, `tax_report_line_02_tag`, `tax_report_line_03`, `tax_report_line_03_tag`, `tax_report_line_44`, `tax_report_line_44_tag`, `tax_report_line_45`, `tax_report_line_45_tag`, `tax_report_title_operations_sortie_46`
- Menus: 1; representative evidence: `addons/l10n_be/data/menuitem_data.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_be/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `account.chart.template` (addons/l10n_be/demo/account_demo.py:5); inherits `account.chart.template` (addons/l10n_be/models/template_be_comp.py:7); inherits `account.journal` (addons/l10n_be/models/account_journal.py:6); inherits `account.tax` (addons/l10n_be/models/account_tax.py:4); inherits `account.chart.template` (addons/l10n_be/models/template_be_asso.py:7); inherits `account.move` (addons/l10n_be/models/account_move.py:17); inherits `account.chart.template` (addons/l10n_be/models/template_be.py:7); inherits `res.company` (addons/l10n_be/models/res_company.py:18)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_ubl_cii`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_be/__init__.py`
- `addons/l10n_be/__manifest__.py`
- `addons/l10n_be/data/account_tax_report_data.xml`
- `addons/l10n_be/data/l10n_be_sequence_data.xml`
- `addons/l10n_be/data/menuitem_data.xml`
- `addons/l10n_be/data/template/account.account-be.csv`
- `addons/l10n_be/data/template/account.account-be_asso.csv`
- `addons/l10n_be/data/template/account.account-be_comp.csv`
- `addons/l10n_be/data/template/account.depreciation.model-be.csv`
- `addons/l10n_be/data/template/account.fiscal.position-be.csv`
- `addons/l10n_be/data/template/account.tax-be.csv`
- `addons/l10n_be/data/template/account.tax.group-be.csv`
- `addons/l10n_be/demo/__init__.py`
- `addons/l10n_be/demo/account_demo.py`
- `addons/l10n_be/demo/demo_company.xml`
- `addons/l10n_be/i18n/de.po`
- `addons/l10n_be/i18n/fr.po`
- `addons/l10n_be/i18n/l10n_be.pot`
- `addons/l10n_be/i18n/nl.po`
- `addons/l10n_be/models/__init__.py`
- `addons/l10n_be/models/account_journal.py`
- `addons/l10n_be/models/account_move.py`
- `addons/l10n_be/models/account_tax.py`
- `addons/l10n_be/models/res_company.py`
- `addons/l10n_be/models/template_be.py`
- `addons/l10n_be/models/template_be_asso.py`
- `addons/l10n_be/models/template_be_comp.py`
