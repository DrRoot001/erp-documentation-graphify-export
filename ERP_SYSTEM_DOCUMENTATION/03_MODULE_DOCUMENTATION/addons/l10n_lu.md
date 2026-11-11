# Module: l10n_lu

- **Module ID:** MOD-264
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_lu`
- **Manifest:** `addons/l10n_lu/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Luxembourg.
======================================================================

    * the Luxembourg Official Chart of Accounts (law of June 2009 + 2015 chart and Taxes),
    * the Tax Code Chart for Luxembourg
    * the main taxes used in Luxembourg
    * default fiscal position for local, intracom, extracom

Notes:
    * the 2015 chart of taxes is implemented to a large extent,
      see the first sheet of tax.xls for details of coverage
    * to update the chart of tax template, update tax.xls and run tax2csv.py

**Scope evidence:** The module contains 21 files, including 6 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 6
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

- **Description:** 1 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_lu/models/template_lu.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 307 record/template/menu identifiers.
- **Evidence:** `addons/l10n_lu/demo/demo_company.xml:3`, `addons/l10n_lu/demo/demo_company.xml:16`, `addons/l10n_lu/demo/demo_company.xml:21`, `addons/l10n_lu/data/l10n_lu_chart_data.xml:3`, `addons/l10n_lu/data/tax_report/sections_34.xml:3`, `addons/l10n_lu/data/tax_report/sections_34.xml:12`, `addons/l10n_lu/data/tax_report/sections_34.xml:21`, `addons/l10n_lu/data/tax_report/sections_34.xml:28`, `addons/l10n_lu/data/tax_report/sections_34.xml:36`, `addons/l10n_lu/data/tax_report/sections_34.xml:43`, `addons/l10n_lu/data/tax_report/sections_34.xml:50`, `addons/l10n_lu/data/tax_report/sections_34.xml:57`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_lu`, `base.demo_company_lu`, `base.demo_bank_lu`, `Luxembourg`, `l10n_lu_tax_report_sections_3_4`, `tax_report_sections_3_4_balance`, `account_tax_report_line_3_assessment_deducible_tax`, `account_tax_report_line_3a_total_input_tax`, `account_tax_report_line_3a_1_invoiced_by_other_taxable_person`, `account_tax_report_line_3a_1_invoiced_by_other_taxable_person_tag`, `account_tax_report_line_3a_2_due_respect_intra_comm_goods`, `account_tax_report_line_3a_2_due_respect_intra_comm_goods_tag`, `account_tax_report_line_3a_3_due_paid_respect_importation_goods`, `account_tax_report_line_3a_3_due_paid_respect_importation_goods_tag`, `account_tax_report_line_3a_4_due_respect_application_goods`, `account_tax_report_line_3a_4_due_respect_application_goods_tag`, `account_tax_report_line_3a_5_due_under_reverse_charge`, `account_tax_report_line_3a_5_due_under_reverse_charge_tag`, `account_tax_report_line_3a_6_paid_joint_several_guarantee`, `account_tax_report_line_3a_6_paid_joint_several_guarantee_tag`
- Menus: 1; representative evidence: `addons/l10n_lu/data/l10n_lu_chart_data.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_lu/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_lu/models/template_lu.py:6)
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

- `addons/l10n_lu/__init__.py`
- `addons/l10n_lu/__manifest__.py`
- `addons/l10n_lu/data/account.account.tag.csv`
- `addons/l10n_lu/data/l10n_lu_chart_data.xml`
- `addons/l10n_lu/data/tax_report/section_1.xml`
- `addons/l10n_lu/data/tax_report/section_2.xml`
- `addons/l10n_lu/data/tax_report/sections_34.xml`
- `addons/l10n_lu/data/tax_report/tax_report.xml`
- `addons/l10n_lu/data/template/account.account-lu.csv`
- `addons/l10n_lu/data/template/account.fiscal.position-lu.csv`
- `addons/l10n_lu/data/template/account.tax-lu.csv`
- `addons/l10n_lu/data/template/account.tax.group-lu.csv`
- `addons/l10n_lu/demo/demo_company.xml`
- `addons/l10n_lu/i18n/de.po`
- `addons/l10n_lu/i18n/fr.po`
- `addons/l10n_lu/i18n/l10n_lu.pot`
- `addons/l10n_lu/i18n/lb.po`
- `addons/l10n_lu/migrations/2.1/end-migrate_update_taxes.py`
- `addons/l10n_lu/migrations/2.2/end-migrate_update_taxes.py`
- `addons/l10n_lu/models/__init__.py`
- `addons/l10n_lu/models/template_lu.py`
