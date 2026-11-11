# Module: l10n_ca

- **Module ID:** MOD-142
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ca`
- **Manifest:** `addons/l10n_ca/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the module to manage the Canadian accounting chart in Odoo.
===========================================================================================

Canadian accounting charts and localizations.

Fiscal positions
----------------

When considering taxes to be applied, it is the province where the delivery occurs that matters.
Therefore we decided to implement the most common case in the fiscal positions: delivery is the
responsibility of the vendor and done at the customer location.

Some examples:

1) You have a customer from another province and you deliver to his location.
On the customer, set the fiscal position to his province.

2) You have a customer from another province. However this customer comes to your location
with their truck to pick up products. On the customer, do not set any fiscal position.

3) An international vendor doesn't charge you any tax. Taxes are charged at customs
by the customs broker. On the vendor, set the fiscal position to International.

4) An international vendor charge you your provincial tax. They are registered with your
position.

**Scope evidence:** The module contains 24 files, including 10 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 7
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

- **Description:** 5 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_ca/models/res_partner.py:4`, `addons/l10n_ca/models/res_config_settings.py:4`, `addons/l10n_ca/models/template_ca.py:6`, `addons/l10n_ca/models/res_company.py:4`, `addons/l10n_ca/models/res_company.py:26`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 159 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ca/demo/demo.xml:3`, `addons/l10n_ca/demo/demo.xml:16`, `addons/l10n_ca/demo/demo.xml:31`, `addons/l10n_ca/demo/demo.xml:47`, `addons/l10n_ca/demo/demo.xml:60`, `addons/l10n_ca/data/tax_report.xml:3`, `addons/l10n_ca/data/tax_report.xml:11`, `addons/l10n_ca/data/tax_report.xml:17`, `addons/l10n_ca/data/tax_report.xml:22`, `addons/l10n_ca/data/tax_report.xml:29`, `addons/l10n_ca/data/tax_report.xml:34`, `addons/l10n_ca/data/tax_report.xml:41`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ca/tests/__init__.py`, `addons/l10n_ca/tests/test_fiscal_position.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `base.partner_demo_company_ca`, `base.demo_company_ca`, `demo_ca_company_bank`, `partner_demo_ca_customer`, `bank_account_ca_customer`, `l10n_ca_tr_gsthst`, `l10n_ca_tr_gsthst_balance`, `l10n_ca_tr_gsthst_90`, `l10n_ca_tr_gsthst_90_tag`, `l10n_ca_tr_gsthst_91`, `l10n_ca_tr_gsthst_91_tag`, `l10n_ca_tr_gsthst_101`, `l10n_ca_tr_gsthst_103`, `l10n_ca_tr_gsthst_103_tag`, `l10n_ca_tr_gsthst_104`, `l10n_ca_tr_gsthst_104_tag`, `l10n_ca_tr_gsthst_105`, `l10n_ca_tr_gsthst_106`, `l10n_ca_tr_gsthst_106_tag`, `l10n_ca_tr_gsthst_107`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_ca/views/report_invoice.xml:2`, `addons/l10n_ca/views/report_template.xml:3`, `addons/l10n_ca/views/report_template.xml:10`, `addons/l10n_ca/views/report_template.xml:16`
- View/action field declarations: 6; representative evidence: `addons/l10n_ca/views/res_config_settings_views.xml:5`, `addons/l10n_ca/views/res_config_settings_views.xml:7`, `addons/l10n_ca/views/res_company_view.xml:6`, `addons/l10n_ca/views/res_company_view.xml:8`, `addons/l10n_ca/views/res_partner_view.xml:6`, `addons/l10n_ca/views/res_partner_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ca/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `res.partner` (addons/l10n_ca/models/res_partner.py:4); inherits `res.config.settings` (addons/l10n_ca/models/res_config_settings.py:4); inherits `account.chart.template` (addons/l10n_ca/models/template_ca.py:6); inherits `res.company` (addons/l10n_ca/models/res_company.py:4); inherits `base.document.layout` (addons/l10n_ca/models/res_company.py:26)
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

- `addons/l10n_ca/__init__.py`
- `addons/l10n_ca/__manifest__.py`
- `addons/l10n_ca/data/tax_report.xml`
- `addons/l10n_ca/data/template/account.account-ca_2023.csv`
- `addons/l10n_ca/data/template/account.depreciation.model-ca_2023.csv`
- `addons/l10n_ca/data/template/account.fiscal.position-ca_2023.csv`
- `addons/l10n_ca/data/template/account.tax-ca_2023.csv`
- `addons/l10n_ca/data/template/account.tax.group-ca_2023.csv`
- `addons/l10n_ca/demo/demo.xml`
- `addons/l10n_ca/i18n/fr.po`
- `addons/l10n_ca/i18n/l10n_ca.pot`
- `addons/l10n_ca/migrations/1.1/end-migrate-update_taxes.py`
- `addons/l10n_ca/models/__init__.py`
- `addons/l10n_ca/models/res_company.py`
- `addons/l10n_ca/models/res_config_settings.py`
- `addons/l10n_ca/models/res_partner.py`
- `addons/l10n_ca/models/template_ca.py`
- `addons/l10n_ca/tests/__init__.py`
- `addons/l10n_ca/tests/test_fiscal_position.py`
- `addons/l10n_ca/views/report_invoice.xml`
- `addons/l10n_ca/views/report_template.xml`
- `addons/l10n_ca/views/res_company_view.xml`
- `addons/l10n_ca/views/res_config_settings_views.xml`
- `addons/l10n_ca/views/res_partner_view.xml`
