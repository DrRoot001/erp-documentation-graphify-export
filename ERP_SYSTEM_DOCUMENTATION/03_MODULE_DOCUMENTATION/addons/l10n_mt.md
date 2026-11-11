# Module: l10n_mt

- **Module ID:** MOD-274
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_mt`
- **Manifest:** `addons/l10n_mt/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Malta basic package that contains the chart of accounts, the taxes, tax reports, etc.

**Scope evidence:** The module contains 12 files, including 5 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 1
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_mt/models/template_mt.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 91 record/template/menu identifiers.
- **Evidence:** `addons/l10n_mt/demo/demo_company.xml:3`, `addons/l10n_mt/demo/demo_company.xml:15`, `addons/l10n_mt/demo/demo_company.xml:20`, `addons/l10n_mt/data/account_tax_report_data.xml:3`, `addons/l10n_mt/data/account_tax_report_data.xml:10`, `addons/l10n_mt/data/account_tax_report_data.xml:14`, `addons/l10n_mt/data/account_tax_report_data.xml:20`, `addons/l10n_mt/data/account_tax_report_data.xml:24`, `addons/l10n_mt/data/account_tax_report_data.xml:28`, `addons/l10n_mt/data/account_tax_report_data.xml:35`, `addons/l10n_mt/data/account_tax_report_data.xml:39`, `addons/l10n_mt/data/account_tax_report_data.xml:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `partner_demo_company_mt`, `demo_company_mt`, `demo_bank_mt`, `tax_report`, `tax_report_tax_base`, `tax_report_tax_amount`, `tax_report_title_intra_com`, `tax_report_line_I_1`, `tax_report_line_I_1_tag_column1`, `tax_report_line_I_2`, `tax_report_line_I_2_tag_column1`, `tax_report_line_I_3`, `tax_report_line_I_3_tag_column1`, `tax_report_line_I_3_tag_column2`, `tax_report_line_I_4`, `tax_report_line_I_4_tag_column1`, `tax_report_line_I_4_tag_column2`, `tax_report_line_I_5_subtotal`, `tax_report_line_I_5_tag_column1`, `tax_report_line_I_5_tag_column1`
- Menus: 1; representative evidence: `addons/l10n_mt/data/menuitem_data.xml:3`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_mt/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `account.chart.template` (addons/l10n_mt/models/template_mt.py:6)
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

- `addons/l10n_mt/__init__.py`
- `addons/l10n_mt/__manifest__.py`
- `addons/l10n_mt/data/account_tax_report_data.xml`
- `addons/l10n_mt/data/menuitem_data.xml`
- `addons/l10n_mt/data/template/account.account-mt.csv`
- `addons/l10n_mt/data/template/account.fiscal.position-mt.csv`
- `addons/l10n_mt/data/template/account.tax-mt.csv`
- `addons/l10n_mt/data/template/account.tax.group-mt.csv`
- `addons/l10n_mt/demo/demo_company.xml`
- `addons/l10n_mt/migrations/1.1/post-fix-tax-grid-tags.py`
- `addons/l10n_mt/models/__init__.py`
- `addons/l10n_mt/models/template_mt.py`
