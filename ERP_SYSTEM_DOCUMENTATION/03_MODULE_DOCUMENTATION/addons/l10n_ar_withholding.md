# Module: l10n_ar_withholding

- **Module ID:** MOD-124
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ar_withholding`
- **Manifest:** `addons/l10n_ar_withholding/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows to register withholdings during the payment of an invoice.

**Scope evidence:** The module contains 33 files, including 19 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_ar`, `l10n_latam_check`, `l10n_account_withholding_tax`.

## 2. Module structure

- Model/business logic files: 12
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ar_withholding/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 12 model declarations, 95 methods, 3 constraint handlers, 1 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/l10n_ar_withholding/demo/account_demo.py:6`, `addons/l10n_ar_withholding/models/res_partner.py:8`, `addons/l10n_ar_withholding/models/account_payment.py:5`, `addons/l10n_ar_withholding/models/account_payment_withholding_line.py:4`, `addons/l10n_ar_withholding/models/account_tax.py:7`, `addons/l10n_ar_withholding/models/l10n_ar_earnings_scale_line.py:4`, `addons/l10n_ar_withholding/models/account_chart_template.py:5`, `addons/l10n_ar_withholding/models/account_withholding_line.py:6`, `addons/l10n_ar_withholding/models/l10n_ar_partner_tax.py:5`, `addons/l10n_ar_withholding/models/l10n_ar_earnings_scale.py:4`, `addons/l10n_ar_withholding/wizards/account_payment_register_withholding_line.py:4`, `addons/l10n_ar_withholding/wizards/account_payment_register.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 26 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ar_withholding/wizards/account_payment_register_views.xml:3`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:6`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:10`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:16`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:22`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:28`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:34`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:40`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:46`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:52`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:63`, `addons/l10n_ar_withholding/data/earnings_table_data.xml:67`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ar_withholding/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ar_withholding/tests/test_withholding_ar_ri.py`, `addons/l10n_ar_withholding/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `view_account_payment_register_form`, `normal_scale`, `scale_1`, `scale_2`, `scale_3`, `scale_4`, `scale_5`, `scale_6`, `scale_7`, `scale_8`, `scale_119`, `scale_9`, `scale_10`, `scale_11`, `scale_12`, `scale_13`, `scale_14`, `scale_15`, `scale_16`, `view_partner_form`
- Menus: 1; representative evidence: `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:58`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 14; representative evidence: `addons/l10n_ar_withholding/wizards/account_payment_register_views.xml:5`, `addons/l10n_ar_withholding/wizards/account_payment_register_views.xml:7`, `addons/l10n_ar_withholding/views/res_partner_view.xml:7`, `addons/l10n_ar_withholding/views/res_partner_view.xml:8`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:6`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:7`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:16`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:17`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:53`, `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml:54`, `addons/l10n_ar_withholding/views/account_tax_views.xml:5`, `addons/l10n_ar_withholding/views/account_tax_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ar_withholding/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 12
- Representative model evidence: inherits `account.chart.template` (addons/l10n_ar_withholding/demo/account_demo.py:6); inherits `res.partner` (addons/l10n_ar_withholding/models/res_partner.py:8); inherits `account.payment` (addons/l10n_ar_withholding/models/account_payment.py:5); inherits `account.payment.withholding.line` (addons/l10n_ar_withholding/models/account_payment_withholding_line.py:4); inherits `account.tax` (addons/l10n_ar_withholding/models/account_tax.py:7); `l10n_ar.earnings.scale.line` (addons/l10n_ar_withholding/models/l10n_ar_earnings_scale_line.py:4); inherits `account.chart.template` (addons/l10n_ar_withholding/models/account_chart_template.py:5); inherits `account.withholding.line` (addons/l10n_ar_withholding/models/account_withholding_line.py:6); `l10n_ar.partner.tax` (addons/l10n_ar_withholding/models/l10n_ar_partner_tax.py:5); `l10n_ar.earnings.scale` (addons/l10n_ar_withholding/models/l10n_ar_earnings_scale.py:4); inherits `account.payment.register.withholding.line` (addons/l10n_ar_withholding/wizards/account_payment_register_withholding_line.py:4); inherits `account.payment.register` (addons/l10n_ar_withholding/wizards/account_payment_register.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_ar`, `l10n_latam_check`, `l10n_account_withholding_tax`
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

- `addons/l10n_ar_withholding/__init__.py`
- `addons/l10n_ar_withholding/__manifest__.py`
- `addons/l10n_ar_withholding/data/earnings_table_data.xml`
- `addons/l10n_ar_withholding/data/template/account.account-ar_base.csv`
- `addons/l10n_ar_withholding/data/template/account.tax-ar_base.csv`
- `addons/l10n_ar_withholding/data/template/account.tax-ar_ex.csv`
- `addons/l10n_ar_withholding/data/template/account.tax-ar_ri.csv`
- `addons/l10n_ar_withholding/data/template/account.tax.group-ar_base.csv`
- `addons/l10n_ar_withholding/data/template/account.tax.group-ar_ex.csv`
- `addons/l10n_ar_withholding/demo/__init__.py`
- `addons/l10n_ar_withholding/demo/account_demo.py`
- `addons/l10n_ar_withholding/i18n/es_419.po`
- `addons/l10n_ar_withholding/i18n/l10n_ar_withholding.pot`
- `addons/l10n_ar_withholding/models/__init__.py`
- `addons/l10n_ar_withholding/models/account_chart_template.py`
- `addons/l10n_ar_withholding/models/account_payment.py`
- `addons/l10n_ar_withholding/models/account_payment_withholding_line.py`
- `addons/l10n_ar_withholding/models/account_tax.py`
- `addons/l10n_ar_withholding/models/account_withholding_line.py`
- `addons/l10n_ar_withholding/models/l10n_ar_earnings_scale.py`
- `addons/l10n_ar_withholding/models/l10n_ar_earnings_scale_line.py`
- `addons/l10n_ar_withholding/models/l10n_ar_partner_tax.py`
- `addons/l10n_ar_withholding/models/res_partner.py`
- `addons/l10n_ar_withholding/security/ir.access.csv`
- `addons/l10n_ar_withholding/tests/__init__.py`
- `addons/l10n_ar_withholding/tests/test_withholding_ar_ri.py`
- `addons/l10n_ar_withholding/views/account_tax_views.xml`
- `addons/l10n_ar_withholding/views/l10n_ar_earnings_scale_view.xml`
- `addons/l10n_ar_withholding/views/res_partner_view.xml`
- `addons/l10n_ar_withholding/wizards/__init__.py`
- `addons/l10n_ar_withholding/wizards/account_payment_register.py`
- `addons/l10n_ar_withholding/wizards/account_payment_register_views.xml`
- `addons/l10n_ar_withholding/wizards/account_payment_register_withholding_line.py`
