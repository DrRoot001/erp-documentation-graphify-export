# Module: l10n_cz

- **Module ID:** MOD-156
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_cz`
- **Manifest:** `addons/l10n_cz/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Czech accounting chart and localization.  With Chart of Accounts with taxes and basic fiscal positions.

Tento modul definuje:

- Českou účetní osnovu za rok 2020

- Základní sazby pro DPH z prodeje a nákupu

- Základní fiskální pozice pro českou legislativu

**Scope evidence:** The module contains 29 files, including 12 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_cz/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 22 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_cz/models/res_bank.py:6`, `addons/l10n_cz/models/template_cz.py:7`, `addons/l10n_cz/models/account_move.py:5`, `addons/l10n_cz/models/l10n_cz_tax_office.py:4`, `addons/l10n_cz/models/res_company.py:6`, `addons/l10n_cz/models/res_company.py:94`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 179 record/template/menu identifiers.
- **Evidence:** `addons/l10n_cz/demo/demo_company.xml:3`, `addons/l10n_cz/demo/demo_company.xml:15`, `addons/l10n_cz/demo/demo_company.xml:20`, `addons/l10n_cz/data/res_country_data.xml:3`, `addons/l10n_cz/data/tax_report.xml:3`, `addons/l10n_cz/data/tax_report.xml:15`, `addons/l10n_cz/data/tax_report.xml:21`, `addons/l10n_cz/data/tax_report.xml:27`, `addons/l10n_cz/data/tax_report.xml:33`, `addons/l10n_cz/data/tax_report.xml:39`, `addons/l10n_cz/data/tax_report.xml:45`, `addons/l10n_cz/data/tax_report.xml:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_cz/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_cz/tests/test_cz_qr.py`, `addons/l10n_cz/tests/test_moves.py`, `addons/l10n_cz/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `base.partner_demo_company_cz`, `base.demo_company_cz`, `base.demo_bank_cz`, `base.cz`, `l10n_cz_vat_declaration`, `l10n_cz_vat_declaration_tax_base`, `l10n_cz_vat_declaration_output_tax`, `l10n_cz_vat_declaration_value`, `l10n_cz_vat_declaration_in_full_amount`, `l10n_cz_vat_declaration_reduced_claim`, `l10n_cz_vat_declaration_coefficient`, `l10n_cz_vat_declaration_line_1`, `l10n_cz_vat_declaration_line_2`, `l10n_cz_vat_declaration_line_3`, `l10n_cz_vat_declaration_line_3_tax_base`, `l10n_cz_vat_declaration_line_3_raw_output_tax`, `l10n_cz_vat_declaration_line_3_output_tax`, `l10n_cz_vat_declaration_line_4`, `l10n_cz_vat_declaration_line_4_tax_base`, `l10n_cz_vat_declaration_line_4_raw_output_tax`
- Menus: 1; representative evidence: `addons/l10n_cz/views/tax_office_view.xml:55`
- Templates: 4; representative evidence: `addons/l10n_cz/views/report_invoice.xml:3`, `addons/l10n_cz/views/report_template.xml:3`, `addons/l10n_cz/views/report_template.xml:9`, `addons/l10n_cz/views/report_template.xml:15`
- View/action field declarations: 12; representative evidence: `addons/l10n_cz/views/res_company_views.xml:6`, `addons/l10n_cz/views/res_company_views.xml:7`, `addons/l10n_cz/views/res_partner_views.xml:6`, `addons/l10n_cz/views/res_partner_views.xml:8`, `addons/l10n_cz/views/tax_office_view.xml:6`, `addons/l10n_cz/views/tax_office_view.xml:7`, `addons/l10n_cz/views/tax_office_view.xml:19`, `addons/l10n_cz/views/tax_office_view.xml:20`, `addons/l10n_cz/views/tax_office_view.xml:33`, `addons/l10n_cz/views/tax_office_view.xml:34`, `addons/l10n_cz/views/tax_office_view.xml:50`, `addons/l10n_cz/views/tax_office_view.xml:52`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_cz/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.partner.bank` (addons/l10n_cz/models/res_bank.py:6); inherits `account.chart.template` (addons/l10n_cz/models/template_cz.py:7); inherits `account.move` (addons/l10n_cz/models/account_move.py:5); `l10n_cz.tax_office` (addons/l10n_cz/models/l10n_cz_tax_office.py:4); inherits `res.company` (addons/l10n_cz/models/res_company.py:6); inherits `base.document.layout` (addons/l10n_cz/models/res_company.py:94)
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
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_cz/__init__.py`
- `addons/l10n_cz/__manifest__.py`
- `addons/l10n_cz/data/l10n_cz.tax_office.csv`
- `addons/l10n_cz/data/res_country_data.xml`
- `addons/l10n_cz/data/tax_report.xml`
- `addons/l10n_cz/data/template/account.account-cz.csv`
- `addons/l10n_cz/data/template/account.depreciation.model-cz.csv`
- `addons/l10n_cz/data/template/account.fiscal.position-cz.csv`
- `addons/l10n_cz/data/template/account.tax-cz.csv`
- `addons/l10n_cz/data/template/account.tax.group-cz.csv`
- `addons/l10n_cz/demo/demo_company.xml`
- `addons/l10n_cz/i18n/cs.po`
- `addons/l10n_cz/i18n/l10n_cz.pot`
- `addons/l10n_cz/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_cz/models/__init__.py`
- `addons/l10n_cz/models/account_move.py`
- `addons/l10n_cz/models/l10n_cz_tax_office.py`
- `addons/l10n_cz/models/res_bank.py`
- `addons/l10n_cz/models/res_company.py`
- `addons/l10n_cz/models/template_cz.py`
- `addons/l10n_cz/security/ir.access.csv`
- `addons/l10n_cz/tests/__init__.py`
- `addons/l10n_cz/tests/test_cz_qr.py`
- `addons/l10n_cz/tests/test_moves.py`
- `addons/l10n_cz/views/report_invoice.xml`
- `addons/l10n_cz/views/report_template.xml`
- `addons/l10n_cz/views/res_company_views.xml`
- `addons/l10n_cz/views/res_partner_views.xml`
- `addons/l10n_cz/views/tax_office_view.xml`
