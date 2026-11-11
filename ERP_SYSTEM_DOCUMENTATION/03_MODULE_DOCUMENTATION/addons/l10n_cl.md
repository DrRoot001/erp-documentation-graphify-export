# Module: l10n_cl

- **Module ID:** MOD-149
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_cl`
- **Manifest:** `addons/l10n_cl/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Chilean accounting chart and tax localization.
Plan contable chileno e impuestos de acuerdo a disposiciones vigentes.

**Scope evidence:** The module contains 51 files, including 20 Python, 17 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `contacts`, `l10n_latam_invoice_document`, `uom`, `account`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 17
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 38 methods, 1 constraint handlers, 1 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_cl/demo/account_demo.py:7`, `addons/l10n_cl/models/res_partner.py:8`, `addons/l10n_cl/models/uom_uom.py:6`, `addons/l10n_cl/models/res_currency.py:5`, `addons/l10n_cl/models/template_cl.py:6`, `addons/l10n_cl/models/account_tax.py:6`, `addons/l10n_cl/models/res_country.py:6`, `addons/l10n_cl/models/l10n_latam_document_type.py:6`, `addons/l10n_cl/models/account_move.py:14`, `addons/l10n_cl/models/account_move_line.py:7`, `addons/l10n_cl/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 17 XML files and 0 JavaScript/TypeScript files; static XML analysis found 171 record/template/menu identifiers.
- **Evidence:** `addons/l10n_cl/demo/company_demo.xml:3`, `addons/l10n_cl/demo/company_demo.xml:17`, `addons/l10n_cl/demo/partner_demo.xml:4`, `addons/l10n_cl/demo/partner_demo.xml:17`, `addons/l10n_cl/demo/partner_demo.xml:23`, `addons/l10n_cl/demo/partner_demo.xml:36`, `addons/l10n_cl/demo/partner_demo.xml:40`, `addons/l10n_cl/demo/partner_demo.xml:44`, `addons/l10n_cl/demo/partner_demo.xml:48`, `addons/l10n_cl/demo/partner_demo.xml:52`, `addons/l10n_cl/demo/partner_demo.xml:56`, `addons/l10n_cl/demo/partner_demo.xml:60`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_cl/views/report_invoice.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_cl/tests/test_latam_document_type.py`, `addons/l10n_cl/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 17; representative identifiers: `base.partner_demo_company_cl`, `base.demo_company_cl`, `res_partner_bmya`, `res_partner_bmya_dab`, `res_partner_teksa`, `base.res_partner_2`, `base.res_partner_3`, `base.res_partner_4`, `base.res_partner_5`, `base.res_partner_6`, `base.res_partner_12`, `demo_partner_cl_1`, `demo_partner_cl_2`, `demo_partner_cl_3`, `demo_partner_supermarket`, `demo_partner_cl_fee_receipts`, `tag_cl_sale_mnt_exe`, `tag_cl_sale_mnt_neto`, `tag_cl_sale_valor_neto_comis`, `tag_cl_sale_valor_comisiones_no_afecto`
- Menus: 2; representative evidence: `addons/l10n_cl/views/account_move_view.xml:76`, `addons/l10n_cl/views/account_move_view.xml:77`
- Templates: 6; representative evidence: `addons/l10n_cl/views/report_invoice.xml:5`, `addons/l10n_cl/views/report_invoice.xml:79`, `addons/l10n_cl/views/report_invoice.xml:129`, `addons/l10n_cl/views/report_invoice.xml:133`, `addons/l10n_cl/views/report_invoice.xml:223`, `addons/l10n_cl/views/report_invoice.xml:231`
- View/action field declarations: 26; representative evidence: `addons/l10n_cl/views/account_move_view.xml:5`, `addons/l10n_cl/views/account_move_view.xml:7`, `addons/l10n_cl/views/account_move_view.xml:16`, `addons/l10n_cl/views/account_move_view.xml:18`, `addons/l10n_cl/views/account_move_view.xml:29`, `addons/l10n_cl/views/account_move_view.xml:30`, `addons/l10n_cl/views/account_move_view.xml:59`, `addons/l10n_cl/views/account_move_view.xml:63`, `addons/l10n_cl/views/account_move_view.xml:69`, `addons/l10n_cl/views/account_move_view.xml:73`, `addons/l10n_cl/views/res_company_view.xml:5`, `addons/l10n_cl/views/res_company_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_cl/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_cl/views/report_invoice.xml`

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `account.chart.template` (addons/l10n_cl/demo/account_demo.py:7); inherits `res.partner` (addons/l10n_cl/models/res_partner.py:8); inherits `uom.uom` (addons/l10n_cl/models/uom_uom.py:6); inherits `res.currency` (addons/l10n_cl/models/res_currency.py:5); inherits `account.chart.template` (addons/l10n_cl/models/template_cl.py:6); inherits `account.tax` (addons/l10n_cl/models/account_tax.py:6); inherits `res.country` (addons/l10n_cl/models/res_country.py:6); inherits `l10n_latam.document.type` (addons/l10n_cl/models/l10n_latam_document_type.py:6); inherits `account.move` (addons/l10n_cl/models/account_move.py:14); inherits `account.move.line` (addons/l10n_cl/models/account_move_line.py:7); inherits `res.company` (addons/l10n_cl/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `contacts`, `l10n_latam_invoice_document`, `uom`, `account`
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

- `addons/l10n_cl/__init__.py`
- `addons/l10n_cl/__manifest__.py`
- `addons/l10n_cl/data/account_tax_report_data.xml`
- `addons/l10n_cl/data/account_tax_tags_data.xml`
- `addons/l10n_cl/data/l10n_cl_chart_data.xml`
- `addons/l10n_cl/data/l10n_latam.document.type.csv`
- `addons/l10n_cl/data/product_data.xml`
- `addons/l10n_cl/data/res.city.csv`
- `addons/l10n_cl/data/res.country.csv`
- `addons/l10n_cl/data/res.currency.csv`
- `addons/l10n_cl/data/res_country.xml`
- `addons/l10n_cl/data/res_currency_data.xml`
- `addons/l10n_cl/data/res_partner.xml`
- `addons/l10n_cl/data/template/account.account-cl.csv`
- `addons/l10n_cl/data/template/account.depreciation.model-cl.csv`
- `addons/l10n_cl/data/template/account.fiscal.position-cl.csv`
- `addons/l10n_cl/data/template/account.tax-cl.csv`
- `addons/l10n_cl/data/template/account.tax.group-cl.csv`
- `addons/l10n_cl/data/uom_data.xml`
- `addons/l10n_cl/demo/__init__.py`
- `addons/l10n_cl/demo/account_demo.py`
- `addons/l10n_cl/demo/bmya_icon.png`
- `addons/l10n_cl/demo/company_demo.xml`
- `addons/l10n_cl/demo/partner_demo.xml`
- `addons/l10n_cl/i18n/es_419.po`
- `addons/l10n_cl/i18n/l10n_cl.pot`
- `addons/l10n_cl/migrations/3.1/end-migrate_update_taxes.py`
- `addons/l10n_cl/models/__init__.py`
- `addons/l10n_cl/models/account_move.py`
- `addons/l10n_cl/models/account_move_line.py`
- `addons/l10n_cl/models/account_tax.py`
- `addons/l10n_cl/models/l10n_latam_document_type.py`
- `addons/l10n_cl/models/res_company.py`
- `addons/l10n_cl/models/res_country.py`
- `addons/l10n_cl/models/res_currency.py`
- `addons/l10n_cl/models/res_partner.py`
- `addons/l10n_cl/models/template_cl.py`
- `addons/l10n_cl/models/uom_uom.py`
- `addons/l10n_cl/static/sii_logo.jpeg`
- `addons/l10n_cl/static/tgr_logo.png`
- `addons/l10n_cl/tests/__init__.py`
- `addons/l10n_cl/tests/test_latam_document_type.py`
- `addons/l10n_cl/tools/__init__.py`
- `addons/l10n_cl/tools/partner_identifiers.py`
- `addons/l10n_cl/views/account_move_view.xml`
- `addons/l10n_cl/views/account_tax_view.xml`
- `addons/l10n_cl/views/report_invoice.xml`
- `addons/l10n_cl/views/res_company_view.xml`
- `addons/l10n_cl/views/res_config_settings_view.xml`
- `addons/l10n_cl/views/res_country_view.xml`
- `addons/l10n_cl/views/res_partner.xml`
