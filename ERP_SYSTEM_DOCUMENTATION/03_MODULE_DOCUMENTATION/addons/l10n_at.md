# Module: l10n_at

- **Module ID:** MOD-125
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_at`
- **Manifest:** `addons/l10n_at/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Austrian Standardized Charts & Tax

**Manifest description:**

Austrian charts of accounts (Einheitskontenrahmen 2010).
==========================================================

    * Defines the following chart of account templates:
        * Austrian General Chart of accounts 2010
    * Defines templates for VAT on sales and purchases
    * Defines tax templates
    * Defines fiscal positions for Austrian fiscal legislation
    * Defines tax reports U1/U30

**Scope evidence:** The module contains 16 files, including 6 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`, `l10n_din5008`.

## 2. Module structure

- Model/business logic files: 2
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

- **Description:** 2 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_at/models/account_journal.py:6`, `addons/l10n_at/models/template_at.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 222 record/template/menu identifiers.
- **Evidence:** `addons/l10n_at/demo/demo_company.xml:3`, `addons/l10n_at/demo/demo_company.xml:16`, `addons/l10n_at/demo/demo_company.xml:21`, `addons/l10n_at/data/account_tax_report_data.xml:3`, `addons/l10n_at/data/account_tax_report_data.xml:11`, `addons/l10n_at/data/account_tax_report_data.xml:16`, `addons/l10n_at/data/account_tax_report_data.xml:23`, `addons/l10n_at/data/account_tax_report_data.xml:29`, `addons/l10n_at/data/account_tax_report_data.xml:34`, `addons/l10n_at/data/account_tax_report_data.xml:42`, `addons/l10n_at/data/account_tax_report_data.xml:47`, `addons/l10n_at/data/account_tax_report_data.xml:55`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_at`, `base.demo_company_at`, `base.demo_bank_at`, `tax_report`, `tax_report_balance`, `tax_report_vat`, `tax_report_line_l10n_at_non_tva_sale_report_title`, `tax_report_line_l10n_at_tva_line_3_zm_igl`, `tax_report_line_l10n_at_tva_line_3_zm_igl_tag`, `tax_report_line_l10n_at_tva_line_3_zm_igl3`, `tax_report_line_l10n_at_tva_line_3_zm_igl3_tag`, `tax_report_line_l10n_at_tva_line_3_zm_dl`, `tax_report_line_l10n_at_tva_line_3_zm_dl_tag`, `tax_report_line_l10n_at_tva_sale_report_title`, `tax_report_line_l10n_at_tva_total`, `tax_report_line_l10n_at_tva_line_4_1`, `tax_report_line_l10n_at_tva_line_4_1_tag`, `tax_report_line_l10n_at_tva_line_4_2`, `tax_report_line_l10n_at_tva_line_4_2_tag`, `tax_report_line_l10n_at_tva_line_4_3`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_at/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `account.journal` (addons/l10n_at/models/account_journal.py:6); inherits `account.chart.template` (addons/l10n_at/models/template_at.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_ubl_cii`, `l10n_din5008`
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

- `addons/l10n_at/__init__.py`
- `addons/l10n_at/__manifest__.py`
- `addons/l10n_at/data/account.account.tag.csv`
- `addons/l10n_at/data/account_account_tag.xml`
- `addons/l10n_at/data/account_tax_report_data.xml`
- `addons/l10n_at/data/template/account.account-at.csv`
- `addons/l10n_at/data/template/account.fiscal.position-at.csv`
- `addons/l10n_at/data/template/account.tax-at.csv`
- `addons/l10n_at/data/template/account.tax.group-at.csv`
- `addons/l10n_at/demo/demo_company.xml`
- `addons/l10n_at/i18n/de.po`
- `addons/l10n_at/i18n/l10n_at.pot`
- `addons/l10n_at/migrations/3.2/post-migrate.py`
- `addons/l10n_at/models/__init__.py`
- `addons/l10n_at/models/account_journal.py`
- `addons/l10n_at/models/template_at.py`
