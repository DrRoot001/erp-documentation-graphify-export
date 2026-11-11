# Module: l10n_de

- **Module ID:** MOD-157
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_de`
- **Manifest:** `addons/l10n_de/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Dieses  Modul beinhaltet einen deutschen Kontenrahmen basierend auf dem SKR03 oder SKR04.
=========================================================================================

German accounting chart and localization.
By default, the audit trail is enabled for GoBD compliance.

**Scope evidence:** The module contains 35 files, including 18 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_din5008`, `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 28 methods, 1 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_de/models/datev.py:4`, `addons/l10n_de/models/datev.py:10`, `addons/l10n_de/models/chart_template.py:6`, `addons/l10n_de/models/ir_actions_report.py:4`, `addons/l10n_de/models/account_journal.py:6`, `addons/l10n_de/models/account_account.py:5`, `addons/l10n_de/models/template_de_skr03.py:6`, `addons/l10n_de/models/account_move.py:4`, `addons/l10n_de/models/template_de_skr04.py:6`, `addons/l10n_de/models/res_company.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 207 record/template/menu identifiers.
- **Evidence:** `addons/l10n_de/demo/demo_company.xml:3`, `addons/l10n_de/demo/demo_company.xml:16`, `addons/l10n_de/demo/demo_company.xml:21`, `addons/l10n_de/wizard/account_secure_entries_wizard.xml:3`, `addons/l10n_de/data/account_account_tags_data.xml:3`, `addons/l10n_de/data/account_account_tags_data.xml:11`, `addons/l10n_de/data/account_account_tags_data.xml:16`, `addons/l10n_de/data/account_account_tags_data.xml:23`, `addons/l10n_de/data/account_account_tags_data.xml:29`, `addons/l10n_de/data/account_account_tags_data.xml:35`, `addons/l10n_de/data/account_account_tags_data.xml:40`, `addons/l10n_de/data/account_account_tags_data.xml:47`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_de/models/ir_actions_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_de/tests/test_audit_trail.py`, `addons/l10n_de/tests/__init__.py`, `addons/l10n_de/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_de`, `base.demo_company_de`, `base.demo_bank_de`, `view_account_secure_entries_wizard`, `tax_report`, `tax_report_base`, `tax_report_tax`, `tax_report_de_section_a`, `tax_report_de_tag_81`, `tax_report_de_tag_81_tag`, `tax_report_de_tag_26_tag`, `tax_report_de_tag_86`, `tax_report_de_tag_86_tag`, `tax_report_de_tag_27_tag`, `tax_report_de_tag_87`, `tax_report_de_tag_87_tag`, `tax_report_de_tag_35`, `tax_report_de_tag_35_tag`, `tax_report_de_tag_35_label`, `tax_report_de_tag_36_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_de/wizard/account_secure_entries_wizard.xml:5`, `addons/l10n_de/wizard/account_secure_entries_wizard.xml:8`, `addons/l10n_de/views/res_company_views.xml:5`, `addons/l10n_de/views/res_company_views.xml:7`, `addons/l10n_de/views/account_view.xml:5`, `addons/l10n_de/views/account_view.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_de/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_de/models/ir_actions_report.py`

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `account.tax` (addons/l10n_de/models/datev.py:4); inherits `product.template` (addons/l10n_de/models/datev.py:10); inherits `account.chart.template` (addons/l10n_de/models/chart_template.py:6); inherits `ir.actions.report` (addons/l10n_de/models/ir_actions_report.py:4); inherits `account.journal` (addons/l10n_de/models/account_journal.py:6); inherits `account.account` (addons/l10n_de/models/account_account.py:5); inherits `account.chart.template` (addons/l10n_de/models/template_de_skr03.py:6); inherits `account.move` (addons/l10n_de/models/account_move.py:4); inherits `account.chart.template` (addons/l10n_de/models/template_de_skr04.py:6); inherits `res.company` (addons/l10n_de/models/res_company.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_din5008`, `account`, `account_edi_ubl_cii`
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

- `addons/l10n_de/__init__.py`
- `addons/l10n_de/__manifest__.py`
- `addons/l10n_de/data/account_account_tags_data.xml`
- `addons/l10n_de/data/template/account.account-de_skr03.csv`
- `addons/l10n_de/data/template/account.account-de_skr04.csv`
- `addons/l10n_de/data/template/account.depreciation.model-de_skr03.csv`
- `addons/l10n_de/data/template/account.depreciation.model-de_skr04.csv`
- `addons/l10n_de/data/template/account.fiscal.position-de_skr03.csv`
- `addons/l10n_de/data/template/account.fiscal.position-de_skr04.csv`
- `addons/l10n_de/data/template/account.tax-de_skr03.csv`
- `addons/l10n_de/data/template/account.tax-de_skr04.csv`
- `addons/l10n_de/data/template/account.tax.group-de_skr03.csv`
- `addons/l10n_de/data/template/account.tax.group-de_skr04.csv`
- `addons/l10n_de/demo/demo_company.xml`
- `addons/l10n_de/i18n/de.po`
- `addons/l10n_de/i18n/l10n_de.pot`
- `addons/l10n_de/migrations/1.1/post-migrate_update_amls.py`
- `addons/l10n_de/migrations/2.0/pre-migrate.py`
- `addons/l10n_de/migrations/3.0/pre-migrate.py`
- `addons/l10n_de/models/__init__.py`
- `addons/l10n_de/models/account_account.py`
- `addons/l10n_de/models/account_journal.py`
- `addons/l10n_de/models/account_move.py`
- `addons/l10n_de/models/chart_template.py`
- `addons/l10n_de/models/datev.py`
- `addons/l10n_de/models/ir_actions_report.py`
- `addons/l10n_de/models/res_company.py`
- `addons/l10n_de/models/template_de_skr03.py`
- `addons/l10n_de/models/template_de_skr04.py`
- `addons/l10n_de/tests/__init__.py`
- `addons/l10n_de/tests/test_account_move.py`
- `addons/l10n_de/tests/test_audit_trail.py`
- `addons/l10n_de/views/account_view.xml`
- `addons/l10n_de/views/res_company_views.xml`
- `addons/l10n_de/wizard/account_secure_entries_wizard.xml`
