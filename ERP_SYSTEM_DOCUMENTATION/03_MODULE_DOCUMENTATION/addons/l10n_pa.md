# Module: l10n_pa

- **Module ID:** MOD-289
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pa`
- **Manifest:** `addons/l10n_pa/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Panamenian accounting chart and tax localization.

Plan contable panameño e impuestos de acuerdo a disposiciones vigentes

Con la Colaboración de
- AHMNET CORP http://www.ahmnet.com

**Scope evidence:** The module contains 30 files, including 12 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `base_address_extended`, `contacts`, `l10n_latam_invoice_document`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_pa/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 10 methods, 0 constraint handlers, 2 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_pa/demo/account_demo.py:7`, `addons/l10n_pa/models/res_partner.py:7`, `addons/l10n_pa/models/res_city_corregimiento.py:6`, `addons/l10n_pa/models/res_city.py:6`, `addons/l10n_pa/models/template_pa.py:6`, `addons/l10n_pa/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 15 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pa/demo/demo_company.xml:3`, `addons/l10n_pa/demo/demo_company.xml:18`, `addons/l10n_pa/demo/demo_partner.xml:3`, `addons/l10n_pa/demo/demo_partner.xml:15`, `addons/l10n_pa/demo/demo_partner.xml:27`, `addons/l10n_pa/demo/demo_partner.xml:36`, `addons/l10n_pa/data/res_country_data.xml:4`, `addons/l10n_pa/views/res_company_views.xml:4`, `addons/l10n_pa/views/res_city_views.xml:4`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:4`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:16`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:41`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_pa/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `base.partner_demo_company_pa`, `base.demo_company_pa`, `partner_pa_demo_1`, `partner_pa_demo_2`, `partner_pa_demo_4`, `partner_pa_demo_5`, `base.pa`, `res_company_view_form_inherit_l10n_pa`, `res_city_view_form_inherit_l10n_pa`, `res_city_corregimiento_view_list`, `res_city_corregimiento_view_form`, `res_city_corregimiento_view_search`, `action_res_city_corregimiento`, `Corregimiento (PA)`, `res_partner_view_form_inherit_l10n_pa`
- Menus: 1; representative evidence: `addons/l10n_pa/views/res_city_corregimiento_views.xml:69`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 14; representative evidence: `addons/l10n_pa/views/res_company_views.xml:6`, `addons/l10n_pa/views/res_company_views.xml:8`, `addons/l10n_pa/views/res_city_views.xml:6`, `addons/l10n_pa/views/res_city_views.xml:8`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:6`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:7`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:18`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:19`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:43`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:44`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:57`, `addons/l10n_pa/views/res_city_corregimiento_views.xml:58`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pa/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `account.chart.template` (addons/l10n_pa/demo/account_demo.py:7); inherits `res.partner` (addons/l10n_pa/models/res_partner.py:7); `l10n_pa.res.city.corregimiento` (addons/l10n_pa/models/res_city_corregimiento.py:6); inherits `res.city` (addons/l10n_pa/models/res_city.py:6); inherits `account.chart.template` (addons/l10n_pa/models/template_pa.py:6); inherits `res.company` (addons/l10n_pa/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `base_address_extended`, `contacts`, `l10n_latam_invoice_document`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_pa/__init__.py`
- `addons/l10n_pa/__manifest__.py`
- `addons/l10n_pa/data/l10n_latam.document.type.csv`
- `addons/l10n_pa/data/l10n_pa.res.city.corregimiento.csv`
- `addons/l10n_pa/data/res.city.csv`
- `addons/l10n_pa/data/res_country_data.xml`
- `addons/l10n_pa/data/template/account.account-pa.csv`
- `addons/l10n_pa/data/template/account.depreciation.model-pa.csv`
- `addons/l10n_pa/data/template/account.fiscal.position-pa.csv`
- `addons/l10n_pa/data/template/account.tax-pa.csv`
- `addons/l10n_pa/data/template/account.tax.group-pa.csv`
- `addons/l10n_pa/demo/__init__.py`
- `addons/l10n_pa/demo/account_demo.py`
- `addons/l10n_pa/demo/demo_company.xml`
- `addons/l10n_pa/demo/demo_partner.xml`
- `addons/l10n_pa/i18n/es_419.po`
- `addons/l10n_pa/i18n/l10n_pa.pot`
- `addons/l10n_pa/models/__init__.py`
- `addons/l10n_pa/models/res_city.py`
- `addons/l10n_pa/models/res_city_corregimiento.py`
- `addons/l10n_pa/models/res_company.py`
- `addons/l10n_pa/models/res_partner.py`
- `addons/l10n_pa/models/template_pa.py`
- `addons/l10n_pa/security/ir.access.csv`
- `addons/l10n_pa/tools/__init__.py`
- `addons/l10n_pa/tools/partner_identifiers.py`
- `addons/l10n_pa/views/res_city_corregimiento_views.xml`
- `addons/l10n_pa/views/res_city_views.xml`
- `addons/l10n_pa/views/res_company_views.xml`
- `addons/l10n_pa/views/res_partner_views.xml`
