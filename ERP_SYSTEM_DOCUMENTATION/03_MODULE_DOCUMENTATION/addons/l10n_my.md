# Module: l10n_my

- **Module ID:** MOD-278
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_my`
- **Manifest:** `addons/l10n_my/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module to manage the accounting chart for Malaysia in Odoo.
==============================================================================

**Scope evidence:** The module contains 20 files, including 9 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_tax_python`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
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

- **Description:** 3 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_my/models/res_partner.py:4`, `addons/l10n_my/models/product_template.py:4`, `addons/l10n_my/models/template_my.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 101 record/template/menu identifiers.
- **Evidence:** `addons/l10n_my/demo/demo_company.xml:3`, `addons/l10n_my/demo/demo_company.xml:17`, `addons/l10n_my/data/account_tax_report_data.xml:4`, `addons/l10n_my/data/account_tax_report_data.xml:10`, `addons/l10n_my/data/account_tax_report_data.xml:15`, `addons/l10n_my/data/account_tax_report_data.xml:20`, `addons/l10n_my/data/account_tax_report_data.xml:25`, `addons/l10n_my/data/account_tax_report_data.xml:32`, `addons/l10n_my/data/account_tax_report_data.xml:38`, `addons/l10n_my/data/account_tax_report_data.xml:44`, `addons/l10n_my/data/account_tax_report_data.xml:50`, `addons/l10n_my/data/account_tax_report_data.xml:55`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_my/tests/__init__.py`, `addons/l10n_my/tests/test_res_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_my`, `base.demo_company_my`, `tax_report_sst_02_b2`, `l10n_my_tax_report_sst_02_b2_balance_a`, `l10n_my_tax_report_sst_02_b2_balance_b`, `l10n_my_tax_report_sst_02_b2_balance_c`, `l10n_my_tax_report_sst_02_b2_balance_d`, `l10n_my_sst_part_b2`, `l10n_my_sst_taxable_per_rate`, `l10n_my_sst_taxable_5`, `l10n_my_sst_taxable_5_tag_c`, `l10n_my_sst_taxable_5_tag_d`, `l10n_my_sst_taxable_10`, `l10n_my_sst_taxable_10_tag_c`, `l10n_my_sst_taxable_10_tag_d`, `l10n_my_sst_services_other_than_group_h`, `l10n_my_sst_services_other_than_group_h_6`, `l10n_my_sst_services_other_than_group_h_6_tag_c`, `l10n_my_sst_services_other_than_group_h_6_tag_d`, `l10n_my_sst_services_other_than_group_h_8`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_my/views/product_template_view.xml:6`, `addons/l10n_my/views/product_template_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_my/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner` (addons/l10n_my/models/res_partner.py:4); inherits `product.template` (addons/l10n_my/models/product_template.py:4); inherits `account.chart.template` (addons/l10n_my/models/template_my.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_tax_python`
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

- `addons/l10n_my/__init__.py`
- `addons/l10n_my/__manifest__.py`
- `addons/l10n_my/data/account.account.tag.csv`
- `addons/l10n_my/data/account_tax_report_data.xml`
- `addons/l10n_my/data/template/account.account-my.csv`
- `addons/l10n_my/data/template/account.depreciation.model-my.csv`
- `addons/l10n_my/data/template/account.fiscal.position-my.csv`
- `addons/l10n_my/data/template/account.tax-my.csv`
- `addons/l10n_my/data/template/account.tax.group-my.csv`
- `addons/l10n_my/demo/demo_company.xml`
- `addons/l10n_my/i18n/l10n_my.pot`
- `addons/l10n_my/i18n/ms.po`
- `addons/l10n_my/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_my/models/__init__.py`
- `addons/l10n_my/models/product_template.py`
- `addons/l10n_my/models/res_partner.py`
- `addons/l10n_my/models/template_my.py`
- `addons/l10n_my/tests/__init__.py`
- `addons/l10n_my/tests/test_res_partner.py`
- `addons/l10n_my/views/product_template_view.xml`
