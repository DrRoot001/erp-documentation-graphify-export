# Module: l10n_ph

- **Module ID:** MOD-292
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ph`
- **Manifest:** `addons/l10n_ph/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** This is the module to manage the accounting chart for The Philippines.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 34 files, including 16 Python, 12 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_account_withholding_tax`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 12
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 28 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_ph/models/res_partner.py:80`, `addons/l10n_ph/models/base_document_layout.py:5`, `addons/l10n_ph/models/res_config_settings.py:6`, `addons/l10n_ph/models/account_payment.py:6`, `addons/l10n_ph/models/account_tax.py:6`, `addons/l10n_ph/models/account_move.py:6`, `addons/l10n_ph/models/template_ph.py:6`, `addons/l10n_ph/models/res_company.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 12 XML files and 0 JavaScript/TypeScript files; static XML analysis found 197 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ph/demo/demo_company.xml:3`, `addons/l10n_ph/demo/demo_company.xml:15`, `addons/l10n_ph/data/account_tax_report_data.xml:3`, `addons/l10n_ph/data/account_tax_report_data.xml:11`, `addons/l10n_ph/data/account_tax_report_data.xml:15`, `addons/l10n_ph/data/account_tax_report_data.xml:21`, `addons/l10n_ph/data/account_tax_report_data.xml:26`, `addons/l10n_ph/data/account_tax_report_data.xml:31`, `addons/l10n_ph/data/account_tax_report_data.xml:38`, `addons/l10n_ph/data/account_tax_report_data.xml:43`, `addons/l10n_ph/data/account_tax_report_data.xml:48`, `addons/l10n_ph/data/account_tax_report_data.xml:55`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_ph/views/report_invoice.xml`, `addons/l10n_ph/views/account_report.xml`, `addons/l10n_ph/tests/test_cas_invoice_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_ph/tests/test_partner_name.py`, `addons/l10n_ph/tests/common.py`, `addons/l10n_ph/tests/test_cas_invoice_report.py`, `addons/l10n_ph/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 12; representative identifiers: `base.partner_demo_company_ph`, `base.demo_company_ph`, `vat`, `l10n_ph_2550Q_tax_base`, `l10n_ph_2550Q_balance`, `l10n_ph_2550Q_2550q_ttp`, `l10n_ph_2550Q_2550q_15`, `l10n_ph_2550Q_2550q_15_balance`, `l10n_ph_2550Q_2550q_ltc`, `l10n_ph_2550Q_2550q_16`, `l10n_ph_2550Q_2550q_16_balance`, `l10n_ph_2550Q_2550q_17`, `l10n_ph_2550Q_2550q_17_balance`, `l10n_ph_2550Q_2550q_18`, `l10n_ph_2550Q_2550q_18_balance`, `l10n_ph_2550Q_2550q_19`, `l10n_ph_2550Q_2550q_19_balance`, `l10n_ph_2550Q_2550q_20`, `l10n_ph_2550Q_2550q_20_balance`, `l10n_ph_2550Q_2550q_21`
- Menus: 1; representative evidence: `addons/l10n_ph/data/menuitem_data.xml:3`
- Templates: 12; representative evidence: `addons/l10n_ph/views/report_templates.xml:3`, `addons/l10n_ph/views/report_templates.xml:12`, `addons/l10n_ph/views/report_invoice.xml:9`, `addons/l10n_ph/views/report_invoice.xml:118`, `addons/l10n_ph/views/report_invoice.xml:126`, `addons/l10n_ph/views/report_invoice.xml:140`, `addons/l10n_ph/views/report_disbursement_voucher_template.xml:3`, `addons/l10n_ph/views/report_disbursement_voucher_template.xml:29`, `addons/l10n_ph/views/report_disbursement_voucher_template.xml:52`, `addons/l10n_ph/views/report_disbursement_voucher_template.xml:133`, `addons/l10n_ph/views/report_disbursement_voucher_internal_template.xml:3`, `addons/l10n_ph/views/report_disbursement_voucher_internal_template.xml:58`
- View/action field declarations: 12; representative evidence: `addons/l10n_ph/views/res_config_settings_views.xml:5`, `addons/l10n_ph/views/res_config_settings_views.xml:7`, `addons/l10n_ph/views/report_invoice.xml:132`, `addons/l10n_ph/views/report_invoice.xml:151`, `addons/l10n_ph/views/account_report.xml:4`, `addons/l10n_ph/views/account_report.xml:14`, `addons/l10n_ph/views/res_company_views.xml:5`, `addons/l10n_ph/views/res_company_views.xml:7`, `addons/l10n_ph/views/account_tax_views.xml:5`, `addons/l10n_ph/views/account_tax_views.xml:7`, `addons/l10n_ph/views/res_partner_views.xml:5`, `addons/l10n_ph/views/res_partner_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ph/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/l10n_ph/views/report_invoice.xml`, `addons/l10n_ph/views/account_report.xml`, `addons/l10n_ph/tests/test_cas_invoice_report.py`

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/l10n_ph/models/res_partner.py:80); inherits `base.document.layout` (addons/l10n_ph/models/base_document_layout.py:5); inherits `res.config.settings` (addons/l10n_ph/models/res_config_settings.py:6); inherits `account.payment` (addons/l10n_ph/models/account_payment.py:6); inherits `account.tax` (addons/l10n_ph/models/account_tax.py:6); inherits `account.move` (addons/l10n_ph/models/account_move.py:6); inherits `account.chart.template` (addons/l10n_ph/models/template_ph.py:6); inherits `res.company` (addons/l10n_ph/models/res_company.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `l10n_account_withholding_tax`
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

- `addons/l10n_ph/__init__.py`
- `addons/l10n_ph/__manifest__.py`
- `addons/l10n_ph/data/account_tax_report_data.xml`
- `addons/l10n_ph/data/menuitem_data.xml`
- `addons/l10n_ph/data/template/account.account-ph.csv`
- `addons/l10n_ph/data/template/account.fiscal.position-ph.csv`
- `addons/l10n_ph/data/template/account.tax-ph.csv`
- `addons/l10n_ph/data/template/account.tax.group-ph.csv`
- `addons/l10n_ph/demo/demo_company.xml`
- `addons/l10n_ph/i18n/l10n_ph.pot`
- `addons/l10n_ph/i18n/tl.po`
- `addons/l10n_ph/migrations/1.1/end-migrate_update_taxes.py`
- `addons/l10n_ph/models/__init__.py`
- `addons/l10n_ph/models/account_move.py`
- `addons/l10n_ph/models/account_payment.py`
- `addons/l10n_ph/models/account_tax.py`
- `addons/l10n_ph/models/base_document_layout.py`
- `addons/l10n_ph/models/res_company.py`
- `addons/l10n_ph/models/res_config_settings.py`
- `addons/l10n_ph/models/res_partner.py`
- `addons/l10n_ph/models/template_ph.py`
- `addons/l10n_ph/tests/__init__.py`
- `addons/l10n_ph/tests/common.py`
- `addons/l10n_ph/tests/test_cas_invoice_report.py`
- `addons/l10n_ph/tests/test_partner_name.py`
- `addons/l10n_ph/views/account_report.xml`
- `addons/l10n_ph/views/account_tax_views.xml`
- `addons/l10n_ph/views/report_disbursement_voucher_internal_template.xml`
- `addons/l10n_ph/views/report_disbursement_voucher_template.xml`
- `addons/l10n_ph/views/report_invoice.xml`
- `addons/l10n_ph/views/report_templates.xml`
- `addons/l10n_ph/views/res_company_views.xml`
- `addons/l10n_ph/views/res_config_settings_views.xml`
- `addons/l10n_ph/views/res_partner_views.xml`
