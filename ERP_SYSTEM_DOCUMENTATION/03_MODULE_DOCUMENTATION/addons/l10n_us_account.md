# Module: l10n_us_account

- **Module ID:** MOD-337
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_us_account`
- **Manifest:** `addons/l10n_us_account/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**



**Scope evidence:** The module contains 23 files, including 9 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_us`, `account`, `base_address_extended`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 7
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

- **Description:** 5 model declarations, 14 methods, 1 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_us_account/demo/account_demo.py:12`, `addons/l10n_us_account/models/res_config_settings.py:4`, `addons/l10n_us_account/models/account_tax.py:6`, `addons/l10n_us_account/models/res_partner_bank.py:4`, `addons/l10n_us_account/models/template_us.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/l10n_us_account/data/tax_report.xml:3`, `addons/l10n_us_account/data/tax_report.xml:9`, `addons/l10n_us_account/data/tax_report.xml:14`, `addons/l10n_us_account/data/uom_data.xml:5`, `addons/l10n_us_account/data/uom_data.xml:8`, `addons/l10n_us_account/data/uom_data.xml:13`, `addons/l10n_us_account/data/uom_data.xml:18`, `addons/l10n_us_account/data/uom_data.xml:21`, `addons/l10n_us_account/data/uom_data.xml:26`, `addons/l10n_us_account/views/l10n_us_account_menus.xml:3`, `addons/l10n_us_account/views/l10n_us_account_menus.xml:9`, `addons/l10n_us_account/views/res_config_settings_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `tax_report`, `column_net`, `column_tax`, `uom.product_uom_inch`, `uom.product_uom_foot`, `uom.product_uom_square_foot`, `uom.product_uom_lb`, `uom.product_uom_oz`, `uom.product_uom_gal`, `United States`, `United States`, `res_config_settings_view_form`, `view_partner_bank_form`, `view_tax_form`
- Menus: 2; representative evidence: `addons/l10n_us_account/views/l10n_us_account_menus.xml:3`, `addons/l10n_us_account/views/l10n_us_account_menus.xml:9`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_us_account/views/res_config_settings_views.xml:5`, `addons/l10n_us_account/views/res_config_settings_views.xml:7`, `addons/l10n_us_account/views/res_partner_bank_views.xml:5`, `addons/l10n_us_account/views/res_partner_bank_views.xml:7`, `addons/l10n_us_account/views/account_tax_views.xml:5`, `addons/l10n_us_account/views/account_tax_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_us_account/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `account.chart.template` (addons/l10n_us_account/demo/account_demo.py:12); inherits `res.config.settings` (addons/l10n_us_account/models/res_config_settings.py:4); inherits `account.tax` (addons/l10n_us_account/models/account_tax.py:6); inherits `res.partner.bank` (addons/l10n_us_account/models/res_partner_bank.py:4); inherits `account.chart.template` (addons/l10n_us_account/models/template_us.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_us`, `account`, `base_address_extended`
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

- `addons/l10n_us_account/__init__.py`
- `addons/l10n_us_account/__manifest__.py`
- `addons/l10n_us_account/data/tax_report.xml`
- `addons/l10n_us_account/data/template/account.account-us.csv`
- `addons/l10n_us_account/data/template/account.depreciation.model-us.csv`
- `addons/l10n_us_account/data/template/account.fiscal.position-us.csv`
- `addons/l10n_us_account/data/template/account.tax-us.csv`
- `addons/l10n_us_account/data/template/account.tax.group-us.csv`
- `addons/l10n_us_account/data/uom_data.xml`
- `addons/l10n_us_account/demo/__init__.py`
- `addons/l10n_us_account/demo/account_demo.py`
- `addons/l10n_us_account/demo/demo_company.xml`
- `addons/l10n_us_account/i18n/es_419.po`
- `addons/l10n_us_account/i18n/l10n_us_account.pot`
- `addons/l10n_us_account/models/__init__.py`
- `addons/l10n_us_account/models/account_tax.py`
- `addons/l10n_us_account/models/res_config_settings.py`
- `addons/l10n_us_account/models/res_partner_bank.py`
- `addons/l10n_us_account/models/template_us.py`
- `addons/l10n_us_account/views/account_tax_views.xml`
- `addons/l10n_us_account/views/l10n_us_account_menus.xml`
- `addons/l10n_us_account/views/res_config_settings_views.xml`
- `addons/l10n_us_account/views/res_partner_bank_views.xml`
