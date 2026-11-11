# Module: l10n_ke

- **Module ID:** MOD-250
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ke`
- **Manifest:** `addons/l10n_ke/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This provides a base chart of accounts and taxes template for use in Odoo.

**Scope evidence:** The module contains 22 files, including 8 Python, 6 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ke/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 6 methods, 0 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_ke/models/account_tax.py:5`, `addons/l10n_ke/models/l10n_ke_item_code.py:7`, `addons/l10n_ke/models/template_ke.py:6`, `addons/l10n_ke/models/account_move.py:4`, `addons/l10n_ke/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 0 JavaScript/TypeScript files; static XML analysis found 86 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ke/demo/demo_company.xml:3`, `addons/l10n_ke/demo/demo_company.xml:15`, `addons/l10n_ke/data/account_tax_report_data.xml:3`, `addons/l10n_ke/data/account_tax_report_data.xml:10`, `addons/l10n_ke/data/account_tax_report_data.xml:14`, `addons/l10n_ke/data/account_tax_report_data.xml:20`, `addons/l10n_ke/data/account_tax_report_data.xml:24`, `addons/l10n_ke/data/account_tax_report_data.xml:29`, `addons/l10n_ke/data/account_tax_report_data.xml:36`, `addons/l10n_ke/data/account_tax_report_data.xml:40`, `addons/l10n_ke/data/account_tax_report_data.xml:45`, `addons/l10n_ke/data/account_tax_report_data.xml:52`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ke/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.partner_demo_company_ke`, `base.demo_company_ke`, `tax_report_ke`, `tax_report_base_column`, `tax_report_tax_column`, `tax_report_line_general_rate_sales`, `tax_report_general_rate_sales_base_tag`, `tax_report_general_rate_sales_tax_tag`, `tax_report_line_other_rate_sales`, `tax_report_other_rate_sales_base_tag`, `tax_report_other_rate_sales_tax_tag`, `tax_report_line_zero_rated_sales`, `tax_report_zero_rated_sales_base_tag`, `tax_report_line_exempt_sales`, `tax_report_exempt_sales_base_tag`, `tax_report_line_total_sales`, `tax_report_total_sales_base_tag`, `tax_report_total_sales_tax_tag`, `tax_report_line_output_vat`, `tax_report_output_vat_base_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/l10n_ke/views/account_move_views.xml:5`, `addons/l10n_ke/views/account_move_views.xml:7`, `addons/l10n_ke/views/account_tax_views.xml:5`, `addons/l10n_ke/views/account_tax_views.xml:7`, `addons/l10n_ke/views/account_tax_views.xml:16`, `addons/l10n_ke/views/account_tax_views.xml:18`, `addons/l10n_ke/views/l10n_ke_item_code_views.xml:6`, `addons/l10n_ke/views/l10n_ke_item_code_views.xml:7`, `addons/l10n_ke/views/l10n_ke_item_code_views.xml:17`, `addons/l10n_ke/views/l10n_ke_item_code_views.xml:18`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ke/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `account.tax` (addons/l10n_ke/models/account_tax.py:5); `l10n_ke.item.code` (addons/l10n_ke/models/l10n_ke_item_code.py:7); inherits `account.chart.template` (addons/l10n_ke/models/template_ke.py:6); inherits `account.move` (addons/l10n_ke/models/account_move.py:4); inherits `res.company` (addons/l10n_ke/models/res_company.py:7)
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
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_ke/__init__.py`
- `addons/l10n_ke/__manifest__.py`
- `addons/l10n_ke/data/account_tax_report_data.xml`
- `addons/l10n_ke/data/account_wh_tax_report_data.xml`
- `addons/l10n_ke/data/l10n_ke.item.code.csv`
- `addons/l10n_ke/data/template/account.account-ke.csv`
- `addons/l10n_ke/data/template/account.fiscal.position-ke.csv`
- `addons/l10n_ke/data/template/account.tax-ke.csv`
- `addons/l10n_ke/data/template/account.tax.group-ke.csv`
- `addons/l10n_ke/demo/demo_company.xml`
- `addons/l10n_ke/i18n/l10n_ke.pot`
- `addons/l10n_ke/i18n/sw.po`
- `addons/l10n_ke/models/__init__.py`
- `addons/l10n_ke/models/account_move.py`
- `addons/l10n_ke/models/account_tax.py`
- `addons/l10n_ke/models/l10n_ke_item_code.py`
- `addons/l10n_ke/models/res_company.py`
- `addons/l10n_ke/models/template_ke.py`
- `addons/l10n_ke/security/ir.access.csv`
- `addons/l10n_ke/views/account_move_views.xml`
- `addons/l10n_ke/views/account_tax_views.xml`
- `addons/l10n_ke/views/l10n_ke_item_code_views.xml`
