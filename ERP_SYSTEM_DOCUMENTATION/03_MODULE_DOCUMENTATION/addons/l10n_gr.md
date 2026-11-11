# Module: l10n_gr

- **Module ID:** MOD-207
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_gr`
- **Manifest:** `addons/l10n_gr/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Greece.
==================================================================

Greek accounting chart and localization.

**Scope evidence:** The module contains 12 files, including 4 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 2
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_gr/models/template_gr.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 142 record/template/menu identifiers.
- **Evidence:** `addons/l10n_gr/demo/demo_company.xml:3`, `addons/l10n_gr/demo/demo_company.xml:16`, `addons/l10n_gr/demo/demo_company.xml:21`, `addons/l10n_gr/data/account_tax_report_data.xml:3`, `addons/l10n_gr/data/account_tax_report_data.xml:11`, `addons/l10n_gr/data/account_tax_report_data.xml:18`, `addons/l10n_gr/data/account_tax_report_data.xml:23`, `addons/l10n_gr/data/account_tax_report_data.xml:28`, `addons/l10n_gr/data/account_tax_report_data.xml:34`, `addons/l10n_gr/data/account_tax_report_data.xml:39`, `addons/l10n_gr/data/account_tax_report_data.xml:44`, `addons/l10n_gr/data/account_tax_report_data.xml:51`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `base.partner_demo_company_gr`, `base.demo_company_gr`, `base.demo_bank_gr`, `tax_report`, `tax_report_balance`, `l10n_gr_tr_table_B`, `l10n_gr_tr_section_a`, `l10n_gr_tr_301`, `l10n_gr_tr_301_tag`, `l10n_gr_tr_301_tag_sale`, `l10n_gr_tr_301_tag_purchase`, `l10n_gr_tr_302`, `l10n_gr_tr_302_tag`, `l10n_gr_tr_302_tag_sale`, `l10n_gr_tr_302_tag_purchase`, `l10n_gr_tr_303`, `l10n_gr_tr_303_tag`, `l10n_gr_tr_303_tag_sale`, `l10n_gr_tr_303_tag_purchase`, `l10n_gr_tr_308`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_gr/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_gr/models/template_gr.py:6)
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

- `addons/l10n_gr/__init__.py`
- `addons/l10n_gr/__manifest__.py`
- `addons/l10n_gr/data/account_tax_report_data.xml`
- `addons/l10n_gr/data/template/account.account-gr.csv`
- `addons/l10n_gr/data/template/account.fiscal.position-gr.csv`
- `addons/l10n_gr/data/template/account.tax-gr.csv`
- `addons/l10n_gr/data/template/account.tax.group-gr.csv`
- `addons/l10n_gr/demo/demo_company.xml`
- `addons/l10n_gr/i18n/el.po`
- `addons/l10n_gr/i18n/l10n_gr.pot`
- `addons/l10n_gr/models/__init__.py`
- `addons/l10n_gr/models/template_gr.py`
