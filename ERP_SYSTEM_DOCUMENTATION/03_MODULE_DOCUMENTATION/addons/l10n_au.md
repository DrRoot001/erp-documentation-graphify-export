# Module: l10n_au

- **Module ID:** MOD-126
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_au`
- **Manifest:** `addons/l10n_au/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Australian Accounting Module
============================

Australian accounting basic charts and localizations.

Also:
    - activates a number of regional currencies.
    - sets up Australian taxes.

**Scope evidence:** The module contains 29 files, including 7 Python, 16 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 16
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

- **Description:** 4 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_au/models/template_au.py:6`, `addons/l10n_au/models/account_move.py:5`, `addons/l10n_au/models/res_partner_bank.py:6`, `addons/l10n_au/models/res_company.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1031 record/template/menu identifiers.
- **Evidence:** `addons/l10n_au/demo/demo_company.xml:3`, `addons/l10n_au/demo/demo_company.xml:16`, `addons/l10n_au/data/res_currency_data.xml:4`, `addons/l10n_au/data/res_currency_data.xml:10`, `addons/l10n_au/data/res_currency_data.xml:14`, `addons/l10n_au/data/res_currency_data.xml:18`, `addons/l10n_au/data/res_currency_data.xml:22`, `addons/l10n_au/data/bas_d.xml:3`, `addons/l10n_au/data/bas_d.xml:12`, `addons/l10n_au/data/bas_d.xml:18`, `addons/l10n_au/data/bas_d.xml:23`, `addons/l10n_au/data/bas_d.xml:28`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `base.partner_demo_company_au`, `base.demo_company_au`, `base.AUD`, `base.NZD`, `base.JPY`, `base.INR`, `base.GBP`, `l10n_au_bas_d`, `l10n_au_bas_d_balance`, `l10n_au_bas_d_gst`, `l10n_au_bas_d_gst_owed`, `l10n_au_bas_d_g1`, `l10n_au_bas_d_g1_balance`, `l10n_au_bas_d_g2`, `l10n_au_bas_d_g2_balance`, `l10n_au_bas_d_g3`, `l10n_au_bas_d_g3_balance`, `l10n_au_bas_d_g4`, `l10n_au_bas_d_g4_balance`, `l10n_au_bas_d_gst_paid`
- Menus: 1; representative evidence: `addons/l10n_au/views/menuitems.xml:3`
- Templates: 2; representative evidence: `addons/l10n_au/views/report_invoice.xml:3`, `addons/l10n_au/views/report_invoice.xml:76`
- View/action field declarations: 2; representative evidence: `addons/l10n_au/views/res_company_views.xml:6`, `addons/l10n_au/views/res_company_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_au/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `account.chart.template` (addons/l10n_au/models/template_au.py:6); inherits `account.move` (addons/l10n_au/models/account_move.py:5); inherits `res.partner.bank` (addons/l10n_au/models/res_partner_bank.py:6); inherits `res.company` (addons/l10n_au/models/res_company.py:4)
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

- `addons/l10n_au/__init__.py`
- `addons/l10n_au/__manifest__.py`
- `addons/l10n_au/data/account.account.tag.csv`
- `addons/l10n_au/data/account_tax_template_data.xml`
- `addons/l10n_au/data/bas_a.xml`
- `addons/l10n_au/data/bas_c.xml`
- `addons/l10n_au/data/bas_d.xml`
- `addons/l10n_au/data/bas_f.xml`
- `addons/l10n_au/data/bas_g.xml`
- `addons/l10n_au/data/bas_u.xml`
- `addons/l10n_au/data/bas_v.xml`
- `addons/l10n_au/data/bas_w.xml`
- `addons/l10n_au/data/bas_x.xml`
- `addons/l10n_au/data/bas_y.xml`
- `addons/l10n_au/data/res_currency_data.xml`
- `addons/l10n_au/data/template/account.account-au.csv`
- `addons/l10n_au/data/template/account.depreciation.model-au.csv`
- `addons/l10n_au/data/template/account.fiscal.position-au.csv`
- `addons/l10n_au/data/template/account.tax-au.csv`
- `addons/l10n_au/data/template/account.tax.group-au.csv`
- `addons/l10n_au/demo/demo_company.xml`
- `addons/l10n_au/models/__init__.py`
- `addons/l10n_au/models/account_move.py`
- `addons/l10n_au/models/res_company.py`
- `addons/l10n_au/models/res_partner_bank.py`
- `addons/l10n_au/models/template_au.py`
- `addons/l10n_au/views/menuitems.xml`
- `addons/l10n_au/views/report_invoice.xml`
- `addons/l10n_au/views/res_company_views.xml`
