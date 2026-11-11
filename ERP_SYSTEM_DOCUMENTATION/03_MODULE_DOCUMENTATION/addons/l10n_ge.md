# Module: l10n_ge

- **Module ID:** MOD-202
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ge`
- **Manifest:** `addons/l10n_ge/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Georgian accounting localization package

**Manifest description:**

This module provides the basic accounting configuration required to use Odoo Accounting in Georgia, including:
==================================================================================================================
* Georgian chart of accounts
* Tax groups and taxes
* Fiscal Positions
* Georgian VAT report

The module is designed to provide a standard accounting setup for companies operating in Georgia and can be extended further based on specific business or legal requirements.

**Scope evidence:** The module contains 13 files, including 4 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 3
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
- **Evidence:** `addons/l10n_ge/models/template_ge.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 116 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ge/demo/demo_company.xml:3`, `addons/l10n_ge/demo/demo_company.xml:15`, `addons/l10n_ge/demo/res_partner_demo.xml:4`, `addons/l10n_ge/demo/res_partner_demo.xml:14`, `addons/l10n_ge/data/account_tax_report_data.xml:3`, `addons/l10n_ge/data/account_tax_report_data.xml:10`, `addons/l10n_ge/data/account_tax_report_data.xml:14`, `addons/l10n_ge/data/account_tax_report_data.xml:20`, `addons/l10n_ge/data/account_tax_report_data.xml:25`, `addons/l10n_ge/data/account_tax_report_data.xml:31`, `addons/l10n_ge/data/account_tax_report_data.xml:36`, `addons/l10n_ge/data/account_tax_report_data.xml:43`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_ge`, `base.demo_company_ge`, `res_partner_ge_individual_customer`, `res_partner_ge_business_customer`, `tax_report_ge`, `tax_report_base`, `tax_report_tax`, `tax_report_line_taxable_supplies`, `tax_report_line_standard_supplies`, `tax_report_line_standard_supplies_base`, `tax_report_line_standard_supplies_tax`, `tax_report_line_special_scheme`, `tax_report_line_special_scheme_base`, `tax_report_line_special_scheme_tax`, `tax_report_line_advance`, `tax_report_line_advance_base`, `tax_report_line_advance_tax`, `tax_report_line_free_supply`, `tax_report_line_free_supply_base`, `tax_report_line_free_supply_tax`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ge/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ge/models/template_ge.py:5)
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
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_ge/__init__.py`
- `addons/l10n_ge/__manifest__.py`
- `addons/l10n_ge/data/account_tax_report_data.xml`
- `addons/l10n_ge/data/template/account.account-ge.csv`
- `addons/l10n_ge/data/template/account.fiscal.position-ge.csv`
- `addons/l10n_ge/data/template/account.tax-ge.csv`
- `addons/l10n_ge/data/template/account.tax.group-ge.csv`
- `addons/l10n_ge/demo/demo_company.xml`
- `addons/l10n_ge/demo/res_partner_demo.xml`
- `addons/l10n_ge/i18n/ka.po`
- `addons/l10n_ge/i18n/l10n_ge.pot`
- `addons/l10n_ge/models/__init__.py`
- `addons/l10n_ge/models/template_ge.py`
