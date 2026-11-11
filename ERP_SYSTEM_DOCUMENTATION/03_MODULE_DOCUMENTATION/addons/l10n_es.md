# Module: l10n_es

- **Module ID:** MOD-174
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_es`
- **Manifest:** `addons/l10n_es/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Spanish charts of accounts (PGCE 2008).
========================================

    * Defines the following chart of account templates:
        * Spanish general chart of accounts 2008
        * Spanish general chart of accounts 2008 for small and medium companies
        * Spanish general chart of accounts 2008 for associations
    * Defines templates for sale and purchase VAT
    * Defines tax templates
    * Defines fiscal positions for spanish fiscal legislation
    * Defines tax reports mod 111, 115, 130 and 303

5.3: Update taxes starting Q4 2024 according to BOE-A-2024-12944 (Royal Decree 4/2024) https://www.boe.es/buscar/act.php?id=BOE-A-2024-12944

**Scope evidence:** The module contains 52 files, including 19 Python, 20 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 20
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 77 methods, 0 constraint handlers, 0 onchange handlers, and 10 dependency declarations.
- **Evidence:** `addons/l10n_es/models/res_partner.py:7`, `addons/l10n_es/models/template_es_pymes.py:6`, `addons/l10n_es/models/res_config_settings.py:6`, `addons/l10n_es/models/template_es_coop_pymes.py:5`, `addons/l10n_es/models/account_tax.py:24`, `addons/l10n_es/models/template_es_assec.py:6`, `addons/l10n_es/models/template_es_common.py:6`, `addons/l10n_es/models/template_es_coop_full.py:5`, `addons/l10n_es/models/account_move.py:11`, `addons/l10n_es/models/template_es_full.py:6`, `addons/l10n_es/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 20 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1131 record/template/menu identifiers.
- **Evidence:** `addons/l10n_es/demo/demo_company.xml:3`, `addons/l10n_es/demo/demo_company.xml:16`, `addons/l10n_es/demo/demo_company.xml:21`, `addons/l10n_es/demo/demo_company.xml:44`, `addons/l10n_es/demo/demo_partner.xml:3`, `addons/l10n_es/demo/demo_partner.xml:16`, `addons/l10n_es/data/mod115.xml:4`, `addons/l10n_es/data/mod115.xml:16`, `addons/l10n_es/data/mod115.xml:23`, `addons/l10n_es/data/mod115.xml:29`, `addons/l10n_es/data/mod115.xml:34`, `addons/l10n_es/data/mod115.xml:44`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_es/tests/__init__.py`, `addons/l10n_es/tests/test_res_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 20; representative identifiers: `base.partner_demo_company_es`, `base.demo_company_es`, `base.demo_bank_es`, `partner_demo_bilbao_es`, `partner_demo_canary`, `partner_demo_mainland`, `mod_115`, `mod_115_column`, `mod_115_title_1`, `mod_115_casilla_01`, `mod_115_casilla_01_balance`, `mod_115_casilla_02`, `mod_115_casilla_02_balance`, `mod_115_casilla_03`, `mod_115_casilla_03_balance`, `mod_115_title_2`, `mod_115_casilla_04`, `mod_115_casilla_04_balance`, `mod_115_casilla_05`, `mod_130`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_es/views/res_config_settings_views.xml:5`, `addons/l10n_es/views/res_config_settings_views.xml:7`, `addons/l10n_es/views/account_move_views.xml:5`, `addons/l10n_es/views/account_move_views.xml:7`, `addons/l10n_es/views/account_tax_views.xml:6`, `addons/l10n_es/views/account_tax_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_es/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `res.partner` (addons/l10n_es/models/res_partner.py:7); inherits `account.chart.template` (addons/l10n_es/models/template_es_pymes.py:6); inherits `res.config.settings` (addons/l10n_es/models/res_config_settings.py:6); inherits `account.chart.template` (addons/l10n_es/models/template_es_coop_pymes.py:5); inherits `account.tax` (addons/l10n_es/models/account_tax.py:24); inherits `account.chart.template` (addons/l10n_es/models/template_es_assec.py:6); inherits `account.chart.template` (addons/l10n_es/models/template_es_common.py:6); inherits `account.chart.template` (addons/l10n_es/models/template_es_coop_full.py:5); inherits `account.move` (addons/l10n_es/models/account_move.py:11); inherits `account.chart.template` (addons/l10n_es/models/template_es_full.py:6); inherits `res.company` (addons/l10n_es/models/res_company.py:6)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_es/__init__.py`
- `addons/l10n_es/__manifest__.py`
- `addons/l10n_es/data/account.account.tag.csv`
- `addons/l10n_es/data/mod111.xml`
- `addons/l10n_es/data/mod115.xml`
- `addons/l10n_es/data/mod130.xml`
- `addons/l10n_es/data/mod303.xml`
- `addons/l10n_es/data/mod390/mod390.xml`
- `addons/l10n_es/data/mod390/mod390_section1.xml`
- `addons/l10n_es/data/mod390/mod390_section2.xml`
- `addons/l10n_es/data/mod390/mod390_section3.xml`
- `addons/l10n_es/data/mod390/mod390_section4.xml`
- `addons/l10n_es/data/mod390/mod390_section5.xml`
- `addons/l10n_es/data/mod390/mod390_section6.xml`
- `addons/l10n_es/data/mod390/mod390_section7.xml`
- `addons/l10n_es/data/mod420.xml`
- `addons/l10n_es/data/res_country_group.xml`
- `addons/l10n_es/data/res_partner_data.xml`
- `addons/l10n_es/data/template/account.account-es_assec.csv`
- `addons/l10n_es/data/template/account.account-es_common.csv`
- `addons/l10n_es/data/template/account.account-es_coop_full.csv`
- `addons/l10n_es/data/template/account.account-es_coop_pymes.csv`
- `addons/l10n_es/data/template/account.account-es_full.csv`
- `addons/l10n_es/data/template/account.account-es_pymes.csv`
- `addons/l10n_es/data/template/account.depreciation.model-es_common.csv`
- `addons/l10n_es/data/template/account.fiscal.position-es_common.csv`
- `addons/l10n_es/data/template/account.tax-es_common.csv`
- `addons/l10n_es/data/template/account.tax.group-es_common.csv`
- `addons/l10n_es/demo/demo_company.xml`
- `addons/l10n_es/demo/demo_partner.xml`
- `addons/l10n_es/i18n/es.po`
- `addons/l10n_es/i18n/l10n_es.pot`
- `addons/l10n_es/migrations/5.3/end-migrate_update_taxes.py`
- `addons/l10n_es/migrations/5.4/end-migrate.py`
- `addons/l10n_es/models/__init__.py`
- `addons/l10n_es/models/account_move.py`
- `addons/l10n_es/models/account_tax.py`
- `addons/l10n_es/models/res_company.py`
- `addons/l10n_es/models/res_config_settings.py`
- `addons/l10n_es/models/res_partner.py`
- `addons/l10n_es/models/template_es_assec.py`
- `addons/l10n_es/models/template_es_common.py`
- `addons/l10n_es/models/template_es_coop_full.py`
- `addons/l10n_es/models/template_es_coop_pymes.py`
- `addons/l10n_es/models/template_es_full.py`
- `addons/l10n_es/models/template_es_pymes.py`
- `addons/l10n_es/tests/__init__.py`
- `addons/l10n_es/tests/test_res_partner.py`
- `addons/l10n_es/upgrades/15.0.5.0/post-61-tag-split-2021.py`
- `addons/l10n_es/views/account_move_views.xml`
- `addons/l10n_es/views/account_tax_views.xml`
- `addons/l10n_es/views/res_config_settings_views.xml`
