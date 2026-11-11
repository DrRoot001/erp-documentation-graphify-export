# Module: l10n_pk

- **Module ID:** MOD-295
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pk`
- **Manifest:** `addons/l10n_pk/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Pakistan Accounting Module
=======================================================
Pakistan accounting basic charts and localization.

Activates:

- Chart of Accounts
- Taxes
- Tax Report
- Withholding Tax Report

**Scope evidence:** The module contains 23 files, including 13 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_tax_python`, `l10n_account_withholding_tax`, `product`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 18 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_pk/demo/account_demo.py:9`, `addons/l10n_pk/models/res_config_settings.py:5`, `addons/l10n_pk/models/account_journal.py:4`, `addons/l10n_pk/models/account_tax.py:4`, `addons/l10n_pk/models/template_pk.py:6`, `addons/l10n_pk/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pk/demo/demo_company.xml:3`, `addons/l10n_pk/demo/demo_company.xml:17`, `addons/l10n_pk/demo/res_partner_demo.xml:3`, `addons/l10n_pk/demo/res_partner_demo.xml:16`, `addons/l10n_pk/demo/res_partner_demo.xml:29`, `addons/l10n_pk/data/ir_actions_server_data.xml:3`, `addons/l10n_pk/data/res_country_data.xml:4`, `addons/l10n_pk/data/ir_config_data.xml:3`, `addons/l10n_pk/views/account_tax_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_pk/data/ir_actions_server_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pk/tests/test_l10n_pk_identifiers.py`, `addons/l10n_pk/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_pk`, `base.demo_company_pk`, `res_partner_punjab`, `res_partner_islamabad`, `res_partner_adil_khan`, `action_l10n_pk_edi_activate`, `base.pk`, `l10n_pk_iap_endpoint`, `view_tax_form_inherit_l10n_pk`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_pk/views/account_tax_views.xml:5`, `addons/l10n_pk/views/account_tax_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pk/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_pk/data/ir_actions_server_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `account.chart.template` (addons/l10n_pk/demo/account_demo.py:9); inherits `res.config.settings` (addons/l10n_pk/models/res_config_settings.py:5); inherits `account.journal` (addons/l10n_pk/models/account_journal.py:4); inherits `account.tax` (addons/l10n_pk/models/account_tax.py:4); inherits `account.chart.template` (addons/l10n_pk/models/template_pk.py:6); inherits `res.company` (addons/l10n_pk/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_tax_python`, `l10n_account_withholding_tax`, `product`
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

- `addons/l10n_pk/__init__.py`
- `addons/l10n_pk/__manifest__.py`
- `addons/l10n_pk/data/ir_actions_server_data.xml`
- `addons/l10n_pk/data/ir_config_data.xml`
- `addons/l10n_pk/data/res_country_data.xml`
- `addons/l10n_pk/data/template/account.account-pk.csv`
- `addons/l10n_pk/data/template/account.depreciation.model-pk.csv`
- `addons/l10n_pk/data/template/account.tax-pk.csv`
- `addons/l10n_pk/data/template/account.tax.group-pk.csv`
- `addons/l10n_pk/demo/__init__.py`
- `addons/l10n_pk/demo/account_demo.py`
- `addons/l10n_pk/demo/demo_company.xml`
- `addons/l10n_pk/demo/res_partner_demo.xml`
- `addons/l10n_pk/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_pk/models/__init__.py`
- `addons/l10n_pk/models/account_journal.py`
- `addons/l10n_pk/models/account_tax.py`
- `addons/l10n_pk/models/res_company.py`
- `addons/l10n_pk/models/res_config_settings.py`
- `addons/l10n_pk/models/template_pk.py`
- `addons/l10n_pk/tests/__init__.py`
- `addons/l10n_pk/tests/test_l10n_pk_identifiers.py`
- `addons/l10n_pk/views/account_tax_views.xml`
