# Module: l10n_sg

- **Module ID:** MOD-315
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sg`
- **Manifest:** `addons/l10n_sg/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Singapore accounting chart and localization.
=======================================================

This module add, for accounting:
 - The Chart of Accounts of Singapore
 - Field UEN (Unique Entity Number) on company and partner
 - Field PermitNo and PermitNoDate on invoice

**Scope evidence:** The module contains 33 files, including 19 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_qr_code_emv`, `account`, `account_edi_ubl_cii`, `account_peppol`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 31 methods, 1 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_sg/models/res_partner.py:4`, `addons/l10n_sg/models/account_edi_proxy_user.py:4`, `addons/l10n_sg/models/res_bank.py:7`, `addons/l10n_sg/models/base_document_layout.py:4`, `addons/l10n_sg/models/account_tax.py:5`, `addons/l10n_sg/models/template_sg.py:6`, `addons/l10n_sg/models/account_move.py:6`, `addons/l10n_sg/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 58 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sg/demo/demo_company.xml:3`, `addons/l10n_sg/demo/demo_company.xml:16`, `addons/l10n_sg/data/account_tax_report_data.xml:3`, `addons/l10n_sg/data/account_tax_report_data.xml:10`, `addons/l10n_sg/data/account_tax_report_data.xml:16`, `addons/l10n_sg/data/account_tax_report_data.xml:20`, `addons/l10n_sg/data/account_tax_report_data.xml:24`, `addons/l10n_sg/data/account_tax_report_data.xml:29`, `addons/l10n_sg/data/account_tax_report_data.xml:34`, `addons/l10n_sg/data/account_tax_report_data.xml:41`, `addons/l10n_sg/data/account_tax_report_data.xml:45`, `addons/l10n_sg/data/account_tax_report_data.xml:52`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_sg/__init__.py`, `addons/l10n_sg/models/account_edi_proxy_user.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_sg/tests/test_l10n_sg_emv_qr.py`, `addons/l10n_sg/tests/test_l10n_sg_reverse_charge_tax.py`, `addons/l10n_sg/tests/test_l10n_sg_customer_accounting.py`, `addons/l10n_sg/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `base.partner_demo_company_sg`, `base.demo_company_sg`, `tax_report`, `tax_report_balance`, `account_tax_report_line_supplies`, `account_tax_report_line_std_rated_supplies`, `account_tax_report_line_std_rated_supplies_tag`, `account_tax_report_line_std_rated_supplies_sub_balance_a`, `account_tax_report_line_std_rated_supplies_sub_balance_b`, `account_tax_report_line_zero_rated_supplies`, `account_tax_report_line_zero_rated_supplies_tag`, `account_tax_report_line_exempt_supplies`, `account_tax_report_line_exempt_supplies_tag`, `account_tax_report_line_total_supplies`, `account_tax_report_line_purchases`, `account_tax_report_line_total_taxable_purchases`, `account_tax_report_line_total_taxable_purchases_tag`, `account_tax_report_line_taxes`, `account_tax_report_line_output_tax_due`, `account_tax_report_line_output_tax_due_tag`
- Menus: 1; representative evidence: `addons/l10n_sg/data/l10n_sg_chart_data.xml:3`
- Templates: 3; representative evidence: `addons/l10n_sg/views/report_templates.xml:3`, `addons/l10n_sg/views/report_invoice.xml:3`, `addons/l10n_sg/views/report_invoice.xml:56`
- View/action field declarations: 6; representative evidence: `addons/l10n_sg/views/res_config_settings_views.xml:6`, `addons/l10n_sg/views/res_config_settings_views.xml:8`, `addons/l10n_sg/views/res_bank_views.xml:6`, `addons/l10n_sg/views/res_bank_views.xml:8`, `addons/l10n_sg/views/account_invoice_view.xml:6`, `addons/l10n_sg/views/account_invoice_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sg/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_sg/__init__.py`, `addons/l10n_sg/models/account_edi_proxy_user.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `res.partner` (addons/l10n_sg/models/res_partner.py:4); inherits `account_edi_proxy_client.user` (addons/l10n_sg/models/account_edi_proxy_user.py:4); inherits `res.partner.bank` (addons/l10n_sg/models/res_bank.py:7); inherits `base.document.layout` (addons/l10n_sg/models/base_document_layout.py:4); inherits `account.tax` (addons/l10n_sg/models/account_tax.py:5); inherits `account.chart.template` (addons/l10n_sg/models/template_sg.py:6); inherits `account.move` (addons/l10n_sg/models/account_move.py:6); `res.company` (addons/l10n_sg/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_qr_code_emv`, `account`, `account_edi_ubl_cii`, `account_peppol`
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

- `addons/l10n_sg/__init__.py`
- `addons/l10n_sg/__manifest__.py`
- `addons/l10n_sg/data/account.account.tag.csv`
- `addons/l10n_sg/data/account_tax_report_data.xml`
- `addons/l10n_sg/data/l10n_sg_chart_data.xml`
- `addons/l10n_sg/data/template/account.account-sg.csv`
- `addons/l10n_sg/data/template/account.depreciation.model-sg.csv`
- `addons/l10n_sg/data/template/account.fiscal.position-sg.csv`
- `addons/l10n_sg/data/template/account.tax-sg.csv`
- `addons/l10n_sg/data/template/account.tax.group-sg.csv`
- `addons/l10n_sg/demo/demo_company.xml`
- `addons/l10n_sg/migrations/2.1/end-migrate_update_tax.py`
- `addons/l10n_sg/migrations/2.2/end-migrate_update_taxes.py`
- `addons/l10n_sg/migrations/2.3/end-reactivate_rc_child_taxes.py`
- `addons/l10n_sg/migrations/9.0.2.0/pre-set_tags_and_taxes_updatable.py`
- `addons/l10n_sg/models/__init__.py`
- `addons/l10n_sg/models/account_edi_proxy_user.py`
- `addons/l10n_sg/models/account_move.py`
- `addons/l10n_sg/models/account_tax.py`
- `addons/l10n_sg/models/base_document_layout.py`
- `addons/l10n_sg/models/res_bank.py`
- `addons/l10n_sg/models/res_company.py`
- `addons/l10n_sg/models/res_partner.py`
- `addons/l10n_sg/models/template_sg.py`
- `addons/l10n_sg/tests/__init__.py`
- `addons/l10n_sg/tests/test_l10n_sg_customer_accounting.py`
- `addons/l10n_sg/tests/test_l10n_sg_emv_qr.py`
- `addons/l10n_sg/tests/test_l10n_sg_reverse_charge_tax.py`
- `addons/l10n_sg/views/account_invoice_view.xml`
- `addons/l10n_sg/views/report_invoice.xml`
- `addons/l10n_sg/views/report_templates.xml`
- `addons/l10n_sg/views/res_bank_views.xml`
- `addons/l10n_sg/views/res_config_settings_views.xml`
