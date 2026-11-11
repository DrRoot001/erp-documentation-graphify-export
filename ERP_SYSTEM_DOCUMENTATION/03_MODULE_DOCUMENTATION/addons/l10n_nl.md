# Module: l10n_nl

- **Module ID:** MOD-285
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_nl`
- **Manifest:** `addons/l10n_nl/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 24 files, including 12 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 5
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

- **Description:** 5 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_nl/models/res_partner.py:6`, `addons/l10n_nl/models/template_nl.py:6`, `addons/l10n_nl/models/account_journal.py:6`, `addons/l10n_nl/models/account_chart_template.py:6`, `addons/l10n_nl/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 118 record/template/menu identifiers.
- **Evidence:** `addons/l10n_nl/demo/demo_company.xml:3`, `addons/l10n_nl/demo/demo_company.xml:16`, `addons/l10n_nl/demo/demo_company.xml:21`, `addons/l10n_nl/data/account_tax_report_data.xml:3`, `addons/l10n_nl/data/account_tax_report_data.xml:13`, `addons/l10n_nl/data/account_tax_report_data.xml:19`, `addons/l10n_nl/data/account_tax_report_data.xml:27`, `addons/l10n_nl/data/account_tax_report_data.xml:35`, `addons/l10n_nl/data/account_tax_report_data.xml:41`, `addons/l10n_nl/data/account_tax_report_data.xml:46`, `addons/l10n_nl/data/account_tax_report_data.xml:53`, `addons/l10n_nl/data/account_tax_report_data.xml:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_nl`, `base.demo_company_nl`, `base.demo_bank_nl`, `tax_report`, `tax_report_base`, `tax_report_tax`, `tax_report_rub_1`, `tax_report_rub_1a`, `tax_report_rub_1a_tag`, `tax_report_rub_btw_1a_tag`, `tax_report_rub_1b`, `tax_report_rub_1b_tag`, `tax_report_rub_btw_1b_tag`, `tax_report_rub_1c`, `tax_report_rub_1c_tag`, `tax_report_rub_btw_1c_tag`, `tax_report_rub_1d`, `tax_report_rub_1d_tag`, `tax_report_rub_btw_1d_tag`, `tax_report_rub_1e`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_nl/views/res_config_settings_view.xml:6`, `addons/l10n_nl/views/res_config_settings_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_nl/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.partner` (addons/l10n_nl/models/res_partner.py:6); inherits `account.chart.template` (addons/l10n_nl/models/template_nl.py:6); inherits `account.journal` (addons/l10n_nl/models/account_journal.py:6); inherits `account.chart.template` (addons/l10n_nl/models/account_chart_template.py:6); inherits `res.company` (addons/l10n_nl/models/res_company.py:6)
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

- `addons/l10n_nl/README.md`
- `addons/l10n_nl/__init__.py`
- `addons/l10n_nl/__manifest__.py`
- `addons/l10n_nl/data/account_account_tag.xml`
- `addons/l10n_nl/data/account_tax_report_data.xml`
- `addons/l10n_nl/data/res_country_group.xml`
- `addons/l10n_nl/data/template/account.account-nl.csv`
- `addons/l10n_nl/data/template/account.fiscal.position-nl.csv`
- `addons/l10n_nl/data/template/account.tax-nl.csv`
- `addons/l10n_nl/data/template/account.tax.group-nl.csv`
- `addons/l10n_nl/demo/demo_company.xml`
- `addons/l10n_nl/i18n/l10n_nl.pot`
- `addons/l10n_nl/i18n/nl.po`
- `addons/l10n_nl/migrations/3.1/end-migrate_update_taxes.py`
- `addons/l10n_nl/migrations/3.3/post-migrate_update_taxes.py`
- `addons/l10n_nl/migrations/3.4/end-migrate.py`
- `addons/l10n_nl/migrations/9.0.2.0/pre-set_tags_and_taxes_updatable.py`
- `addons/l10n_nl/models/__init__.py`
- `addons/l10n_nl/models/account_chart_template.py`
- `addons/l10n_nl/models/account_journal.py`
- `addons/l10n_nl/models/res_company.py`
- `addons/l10n_nl/models/res_partner.py`
- `addons/l10n_nl/models/template_nl.py`
- `addons/l10n_nl/views/res_config_settings_view.xml`
