# Module: l10n_ve

- **Module ID:** MOD-340
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ve`
- **Manifest:** `addons/l10n_ve/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Chart of Account for Venezuela.
===============================

Venezuela doesn't have any chart of account by law, but the default
proposed in Odoo should comply with some Accepted best practices in Venezuela,
this plan comply with this practices.

This module has been tested as base for more of 1000 companies, because
it is based in a mixtures of most common software in the Venezuelan
market what will allow for sure to accountants feel them first steps with
Odoo more comfortable.

This module doesn't pretend be the total localization for Venezuela,
but it will help you to start really quickly with Odoo in this country.

This module give you.
---------------------

- Basic taxes for Venezuela.
- Have basic data to run tests with community localization.
- Start a company from 0 if your needs are basic from an accounting PoV.

We recomend use of account_anglo_saxon if you want valued your
stocks as Venezuela does with out invoices.

If you install this module, and select Custom chart a basic chart will be proposed,
but you will need set manually account defaults for taxes.

**Scope evidence:** The module contains 10 files, including 4 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 1
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

- **Description:** 1 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ve/models/template_ve.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ve/demo/demo_company.xml:3`, `addons/l10n_ve/demo/demo_company.xml:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `base.partner_demo_company_ve`, `base.demo_company_ve`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ve/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ve/models/template_ve.py:6)
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

- `addons/l10n_ve/__init__.py`
- `addons/l10n_ve/__manifest__.py`
- `addons/l10n_ve/data/template/account.account-ve.csv`
- `addons/l10n_ve/data/template/account.tax-ve.csv`
- `addons/l10n_ve/data/template/account.tax.group-ve.csv`
- `addons/l10n_ve/demo/demo_company.xml`
- `addons/l10n_ve/i18n/es_419.po`
- `addons/l10n_ve/i18n/l10n_ve.pot`
- `addons/l10n_ve/models/__init__.py`
- `addons/l10n_ve/models/template_ve.py`
