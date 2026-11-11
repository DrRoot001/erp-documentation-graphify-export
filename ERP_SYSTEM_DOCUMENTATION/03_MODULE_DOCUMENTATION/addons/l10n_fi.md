# Module: l10n_fi

- **Module ID:** MOD-187
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fi`
- **Manifest:** `addons/l10n_fi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the Odoo module to manage the accounting in Finland.
============================================================

After installing this module, you'll have access to:
    * Finnish chart of account
    * Fiscal positions
    * Invoice Payment Reference Types (Finnish Standard Reference & Finnish Creditor Reference (RF))
    * Finnish Reference format for Sale Orders

Set the payment reference type from the Sales Journal.

**Scope evidence:** The module contains 19 files, including 10 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 20 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_fi/models/template_fi.py:6`, `addons/l10n_fi/models/account_journal.py:5`, `addons/l10n_fi/models/account_move.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 185 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fi/demo/demo_company.xml:3`, `addons/l10n_fi/demo/demo_company.xml:16`, `addons/l10n_fi/demo/demo_company.xml:21`, `addons/l10n_fi/data/account_tax_report_line.xml:3`, `addons/l10n_fi/data/account_tax_report_line.xml:11`, `addons/l10n_fi/data/account_tax_report_line.xml:18`, `addons/l10n_fi/data/account_tax_report_line.xml:26`, `addons/l10n_fi/data/account_tax_report_line.xml:33`, `addons/l10n_fi/data/account_tax_report_line.xml:38`, `addons/l10n_fi/data/account_tax_report_line.xml:45`, `addons/l10n_fi/data/account_tax_report_line.xml:50`, `addons/l10n_fi/data/account_tax_report_line.xml:59`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_fi/tests/test_references.py`, `addons/l10n_fi/tests/__init__.py`, `addons/l10n_fi/tests/test_get_reference.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `base.partner_demo_company_fi`, `base.demo_company_fi`, `base.demo_bank_fi`, `vat_report`, `vat_report_balance`, `tax_report_sales_title`, `tax_report_sales_25_5_and_24`, `tax_report_sales_25_5`, `tax_report_sales_25_5_tag`, `tax_report_sales_24`, `tax_report_sales_24_tag`, `tax_report_sales_14_and_13_5`, `tax_report_sales_14`, `tax_report_sales_14_tag`, `tax_report_sales_13_5`, `tax_report_sales_13_5_tag`, `tax_report_sales_10`, `tax_report_sales_10_tag`, `tax_report_tax_purchase_goods_eu`, `tax_report_tax_purchase_goods_eu_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `account.chart.template` (addons/l10n_fi/models/template_fi.py:6); inherits `account.journal` (addons/l10n_fi/models/account_journal.py:5); inherits `account.move` (addons/l10n_fi/models/account_move.py:10)
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

- `addons/l10n_fi/__init__.py`
- `addons/l10n_fi/__manifest__.py`
- `addons/l10n_fi/data/account_account_tag_data.xml`
- `addons/l10n_fi/data/account_tax_report_line.xml`
- `addons/l10n_fi/data/template/account.account-fi.csv`
- `addons/l10n_fi/data/template/account.fiscal.position-fi.csv`
- `addons/l10n_fi/data/template/account.tax-fi.csv`
- `addons/l10n_fi/data/template/account.tax.group-fi.csv`
- `addons/l10n_fi/demo/demo_company.xml`
- `addons/l10n_fi/i18n/fi.po`
- `addons/l10n_fi/i18n/l10n_fi.pot`
- `addons/l10n_fi/migrations/13.0.2/end-migrate_update_taxes.py`
- `addons/l10n_fi/models/__init__.py`
- `addons/l10n_fi/models/account_journal.py`
- `addons/l10n_fi/models/account_move.py`
- `addons/l10n_fi/models/template_fi.py`
- `addons/l10n_fi/tests/__init__.py`
- `addons/l10n_fi/tests/test_get_reference.py`
- `addons/l10n_fi/tests/test_references.py`
