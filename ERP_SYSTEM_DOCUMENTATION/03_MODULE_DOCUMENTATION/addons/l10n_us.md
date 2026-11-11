# Module: l10n_us

- **Module ID:** MOD-336
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_us`
- **Manifest:** `addons/l10n_us/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**



**Scope evidence:** The module contains 15 files, including 6 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `base_address_extended`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_us/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 0 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_us/models/l10n_us_res_county.py:6`, `addons/l10n_us/models/res_city.py:6`, `addons/l10n_us/models/res_partner_bank.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/l10n_us/demo/demo_company.xml:3`, `addons/l10n_us/demo/demo_company.xml:13`, `addons/l10n_us/demo/demo_company.xml:19`, `addons/l10n_us/data/res_company_data.xml:3`, `addons/l10n_us/views/res_partner_bank_views.xml:3`, `addons/l10n_us/views/res_city_views.xml:3`, `addons/l10n_us/views/res_city_views.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_us/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `partner_demo_company_us`, `demo_company_us`, `demo_bank_us`, `base.main_company`, `view_partner_bank_form_inherit_l10n_us`, `res_city_view_list_inherit_l10n_us`, `res_city_view_form_inherit_l10n_us`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_us/views/res_partner_bank_views.xml:5`, `addons/l10n_us/views/res_partner_bank_views.xml:7`, `addons/l10n_us/views/res_city_views.xml:5`, `addons/l10n_us/views/res_city_views.xml:7`, `addons/l10n_us/views/res_city_views.xml:16`, `addons/l10n_us/views/res_city_views.xml:18`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_us/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: `l10n_us.res.county` (addons/l10n_us/models/l10n_us_res_county.py:6); inherits `res.city` (addons/l10n_us/models/res_city.py:6); inherits `res.partner.bank` (addons/l10n_us/models/res_partner_bank.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `base_address_extended`
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

- `addons/l10n_us/__init__.py`
- `addons/l10n_us/__manifest__.py`
- `addons/l10n_us/data/l10n_us.res.county.csv`
- `addons/l10n_us/data/res.city.csv`
- `addons/l10n_us/data/res_company_data.xml`
- `addons/l10n_us/demo/demo_company.xml`
- `addons/l10n_us/i18n/es_419.po`
- `addons/l10n_us/i18n/l10n_us.pot`
- `addons/l10n_us/models/__init__.py`
- `addons/l10n_us/models/l10n_us_res_county.py`
- `addons/l10n_us/models/res_city.py`
- `addons/l10n_us/models/res_partner_bank.py`
- `addons/l10n_us/security/ir.access.csv`
- `addons/l10n_us/views/res_city_views.xml`
- `addons/l10n_us/views/res_partner_bank_views.xml`
