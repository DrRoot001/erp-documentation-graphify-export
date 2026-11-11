# Module: l10n_se

- **Module ID:** MOD-314
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_se`
- **Manifest:** `addons/l10n_se/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Swedish Accounting
------------------

This is the base module to manage the accounting chart for Sweden in Odoo.
It also includes the invoice OCR payment reference handling.

**Scope evidence:** The module contains 27 files, including 11 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 7
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

- **Description:** 7 model declarations, 20 methods, 2 constraint handlers, 2 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_se/models/res_partner.py:8`, `addons/l10n_se/models/account_journal.py:8`, `addons/l10n_se/models/template_se_K3.py:6`, `addons/l10n_se/models/template_se.py:6`, `addons/l10n_se/models/template_se_K2.py:6`, `addons/l10n_se/models/account_move.py:9`, `addons/l10n_se/models/res_company.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 75 record/template/menu identifiers.
- **Evidence:** `addons/l10n_se/demo/demo_company.xml:3`, `addons/l10n_se/demo/demo_company.xml:16`, `addons/l10n_se/demo/demo_company.xml:22`, `addons/l10n_se/data/account_tax_report_data.xml:3`, `addons/l10n_se/data/account_tax_report_data.xml:10`, `addons/l10n_se/data/account_tax_report_data.xml:16`, `addons/l10n_se/data/account_tax_report_data.xml:22`, `addons/l10n_se/data/account_tax_report_data.xml:26`, `addons/l10n_se/data/account_tax_report_data.xml:33`, `addons/l10n_se/data/account_tax_report_data.xml:37`, `addons/l10n_se/data/account_tax_report_data.xml:44`, `addons/l10n_se/data/account_tax_report_data.xml:48`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_se`, `base.demo_company_se`, `base.demo_bank_se`, `tax_report`, `tax_report_balance`, `tax_report_title_sales`, `tax_report_line_05`, `tax_report_line_05_tag`, `tax_report_line_06`, `tax_report_line_06_tag`, `tax_report_line_07`, `tax_report_line_07_tag`, `tax_report_line_08`, `tax_report_line_08_tag`, `tax_report_title_output_vat_sales`, `tax_report_line_10`, `tax_report_line_10_tag`, `tax_report_line_11`, `tax_report_line_11_tag`, `tax_report_line_12`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_se/data/res_country_data.xml:5`, `addons/l10n_se/data/res_country_data.xml:7`, `addons/l10n_se/views/partner_view.xml:6`, `addons/l10n_se/views/partner_view.xml:8`, `addons/l10n_se/views/account_journal_view.xml:6`, `addons/l10n_se/views/account_journal_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_se/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.partner` (addons/l10n_se/models/res_partner.py:8); inherits `account.journal` (addons/l10n_se/models/account_journal.py:8); inherits `account.chart.template` (addons/l10n_se/models/template_se_K3.py:6); inherits `account.chart.template` (addons/l10n_se/models/template_se.py:6); inherits `account.chart.template` (addons/l10n_se/models/template_se_K2.py:6); inherits `account.move` (addons/l10n_se/models/account_move.py:9); inherits `res.company` (addons/l10n_se/models/res_company.py:8)
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

- `addons/l10n_se/__init__.py`
- `addons/l10n_se/__manifest__.py`
- `addons/l10n_se/data/account.account.tag.csv`
- `addons/l10n_se/data/account_tax_report_data.xml`
- `addons/l10n_se/data/res_country_data.xml`
- `addons/l10n_se/data/template/account.account-se.csv`
- `addons/l10n_se/data/template/account.account-se_K2.csv`
- `addons/l10n_se/data/template/account.account-se_K3.csv`
- `addons/l10n_se/data/template/account.fiscal.position-se.csv`
- `addons/l10n_se/data/template/account.tax-se.csv`
- `addons/l10n_se/data/template/account.tax.group-se.csv`
- `addons/l10n_se/data/template/account.tax.group-se_K2.csv`
- `addons/l10n_se/data/template/account.tax.group-se_K3.csv`
- `addons/l10n_se/demo/demo_company.xml`
- `addons/l10n_se/i18n/l10n_se.pot`
- `addons/l10n_se/i18n/sv.po`
- `addons/l10n_se/migrations/1.1/end-migrate.py`
- `addons/l10n_se/models/__init__.py`
- `addons/l10n_se/models/account_journal.py`
- `addons/l10n_se/models/account_move.py`
- `addons/l10n_se/models/res_company.py`
- `addons/l10n_se/models/res_partner.py`
- `addons/l10n_se/models/template_se.py`
- `addons/l10n_se/models/template_se_K2.py`
- `addons/l10n_se/models/template_se_K3.py`
- `addons/l10n_se/views/account_journal_view.xml`
- `addons/l10n_se/views/partner_view.xml`
