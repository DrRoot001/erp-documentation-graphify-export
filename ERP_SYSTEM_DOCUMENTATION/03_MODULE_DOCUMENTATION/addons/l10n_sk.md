# Module: l10n_sk

- **Module ID:** MOD-318
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sk`
- **Manifest:** `addons/l10n_sk/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Slovakia accounting chart and localization: Chart of Accounts 2020, basic VAT rates +
fiscal positions.

Tento modul definuje:
• Slovenskú účtovú osnovu za rok 2020

• Základné sadzby pre DPH z predaja a nákupu

• Základné fiškálne pozície pre slovenskú legislatívu


Pre viac informácií kontaktujte info@26house.com alebo navštívte https://www.26house.com.

**Scope evidence:** The module contains 23 files, including 11 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 5
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

- **Description:** 6 model declarations, 19 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_sk/models/res_partner.py:6`, `addons/l10n_sk/models/res_bank.py:23`, `addons/l10n_sk/models/template_sk.py:6`, `addons/l10n_sk/models/account_move.py:5`, `addons/l10n_sk/models/res_company.py:6`, `addons/l10n_sk/models/res_company.py:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 158 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sk/demo/demo_company.xml:3`, `addons/l10n_sk/demo/demo_company.xml:15`, `addons/l10n_sk/demo/demo_company.xml:20`, `addons/l10n_sk/data/tax_report.xml:13`, `addons/l10n_sk/data/tax_report.xml:19`, `addons/l10n_sk/data/tax_report.xml:24`, `addons/l10n_sk/data/tax_report.xml:31`, `addons/l10n_sk/data/tax_report.xml:36`, `addons/l10n_sk/data/tax_report.xml:41`, `addons/l10n_sk/data/tax_report.xml:46`, `addons/l10n_sk/data/tax_report.xml:51`, `addons/l10n_sk/data/tax_report.xml:58`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_sk/tests/__init__.py`, `addons/l10n_sk/tests/test_l10n_sk_qr_code.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_sk`, `base.demo_company_sk`, `base.demo_bank_sk`, `l10n_sk_vat_report`, `l10n_sk_base_report_column`, `l10n_sk_vat_report_column`, `sk_ops_out`, `sk_ops_out_dom_sale`, `sk_ops_out_dom_sale_01_02`, `sk_ops_out_dom_sale_01_02_base`, `sk_ops_out_dom_sale_01_02_vat`, `sk_ops_out_dom_sale_01a_02a`, `sk_ops_out_dom_sale_01a_02a_base`, `sk_ops_out_dom_sale_01a_02a_vat`, `sk_ops_out_dom_sale_03_04`, `sk_ops_out_dom_sale_03_04_base`, `sk_ops_out_dom_sale_03_04_vat`, `sk_ops_in`, `sk_ops_in_purchase`, `sk_ops_in_purchase_05_06`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_sk/views/report_invoice.xml:3`, `addons/l10n_sk/views/report_template.xml:3`, `addons/l10n_sk/views/report_template.xml:12`, `addons/l10n_sk/views/report_template.xml:18`
- View/action field declarations: 2; representative evidence: `addons/l10n_sk/views/res_company_views.xml:6`, `addons/l10n_sk/views/res_company_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sk/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.partner` (addons/l10n_sk/models/res_partner.py:6); inherits `res.partner.bank` (addons/l10n_sk/models/res_bank.py:23); inherits `account.chart.template` (addons/l10n_sk/models/template_sk.py:6); inherits `account.move` (addons/l10n_sk/models/account_move.py:5); inherits `res.company` (addons/l10n_sk/models/res_company.py:6); inherits `base.document.layout` (addons/l10n_sk/models/res_company.py:18)
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
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_sk/__init__.py`
- `addons/l10n_sk/__manifest__.py`
- `addons/l10n_sk/data/tax_report.xml`
- `addons/l10n_sk/data/template/account.account-sk.csv`
- `addons/l10n_sk/data/template/account.depreciation.model-sk.csv`
- `addons/l10n_sk/data/template/account.fiscal.position-sk.csv`
- `addons/l10n_sk/data/template/account.tax-sk.csv`
- `addons/l10n_sk/data/template/account.tax.group-sk.csv`
- `addons/l10n_sk/demo/demo_company.xml`
- `addons/l10n_sk/i18n/l10n_sk.pot`
- `addons/l10n_sk/i18n/sk.po`
- `addons/l10n_sk/migrations/1.1/pre-migrate.py`
- `addons/l10n_sk/models/__init__.py`
- `addons/l10n_sk/models/account_move.py`
- `addons/l10n_sk/models/res_bank.py`
- `addons/l10n_sk/models/res_company.py`
- `addons/l10n_sk/models/res_partner.py`
- `addons/l10n_sk/models/template_sk.py`
- `addons/l10n_sk/tests/__init__.py`
- `addons/l10n_sk/tests/test_l10n_sk_qr_code.py`
- `addons/l10n_sk/views/report_invoice.xml`
- `addons/l10n_sk/views/report_template.xml`
- `addons/l10n_sk/views/res_company_views.xml`
