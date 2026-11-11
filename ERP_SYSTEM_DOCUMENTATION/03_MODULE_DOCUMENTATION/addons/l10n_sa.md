# Module: l10n_sa

- **Module ID:** MOD-310
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sa`
- **Manifest:** `addons/l10n_sa/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Saudi Arabia Accounting Module
===========================================================
Saudi Arabia Accounting Basic Charts and Localization

Activates:

- Chart of Accounts
- Taxes
- VAT Return
- Withholding Return
- Fiscal Positions

**Scope evidence:** The module contains 41 files, including 22 Python, 11 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_gcc_invoice`, `account`, `account_debit_note`, `l10n_account_withholding_tax`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 11
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

- **Description:** 9 model declarations, 48 methods, 0 constraint handlers, 1 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_sa/demo/account_demo.py:7`, `addons/l10n_sa/models/res_partner.py:7`, `addons/l10n_sa/models/template_sa.py:6`, `addons/l10n_sa/models/account_move.py:11`, `addons/l10n_sa/models/account_move_line.py:4`, `addons/l10n_sa/models/zatca_mixin.py:15`, `addons/l10n_sa/models/ir_attachment.py:5`, `addons/l10n_sa/wizard/account_move_reversal.py:5`, `addons/l10n_sa/wizard/account_debit_note.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 0 JavaScript/TypeScript files; static XML analysis found 142 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sa/demo/demo_company.xml:3`, `addons/l10n_sa/demo/demo_company.xml:20`, `addons/l10n_sa/wizard/account_debit_note.xml:4`, `addons/l10n_sa/wizard/account_move_reversal_views.xml:4`, `addons/l10n_sa/data/account_tax_report_data.xml:3`, `addons/l10n_sa/data/account_tax_report_data.xml:10`, `addons/l10n_sa/data/account_tax_report_data.xml:14`, `addons/l10n_sa/data/account_tax_report_data.xml:20`, `addons/l10n_sa/data/account_tax_report_data.xml:24`, `addons/l10n_sa/data/account_tax_report_data.xml:29`, `addons/l10n_sa/data/account_tax_report_data.xml:34`, `addons/l10n_sa/data/account_tax_report_data.xml:41`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_sa/tests/test_sa_additional_identifiers.py`, `addons/l10n_sa/tests/__init__.py`, `addons/l10n_sa/tests/test_account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `base.partner_demo_company_sa`, `base.demo_company_sa`, `view_account_debit_note_inherit_l10n_sa`, `view_account_move_reversal_inherit_l10n_sa`, `tax_report_vat_filing`, `tax_report_vat_filing_amount`, `tax_report_vat_filing_vat_amount`, `tax_report_line_vat_on_sale`, `tax_report_line_standard_rated_sale`, `tax_report_line_standard_rated_sale_base`, `tax_report_line_standard_rated_sale_tax`, `tax_report_line_ph_pe_fh`, `tax_report_line_ph_pe_fh_base`, `tax_report_line_zero_rated_domestic_sale`, `tax_report_line_zero_rated_domestic_sale_base`, `tax_report_line_exports`, `tax_report_line_exports_base`, `tax_report_line_exempt_sale`, `tax_report_line_exempt_sale_base`, `tax_report_line_total_sale`
- Menus: 0; representative evidence: Not found in module
- Templates: 13; representative evidence: `addons/l10n_sa/views/report_templates_views.xml:3`, `addons/l10n_sa/views/report_templates_views.xml:8`, `addons/l10n_sa/views/report_templates_views.xml:14`, `addons/l10n_sa/views/report_templates_views.xml:23`, `addons/l10n_sa/views/report_templates_views.xml:29`, `addons/l10n_sa/views/report_templates_views.xml:35`, `addons/l10n_sa/views/report_templates_views.xml:41`, `addons/l10n_sa/views/report_templates_views.xml:47`, `addons/l10n_sa/views/report_templates_views.xml:53`, `addons/l10n_sa/views/report_invoice.xml:3`, `addons/l10n_sa/views/report_invoice.xml:232`, `addons/l10n_sa/views/report_invoice.xml:269`
- View/action field declarations: 8; representative evidence: `addons/l10n_sa/wizard/account_debit_note.xml:7`, `addons/l10n_sa/wizard/account_debit_note.xml:8`, `addons/l10n_sa/wizard/account_move_reversal_views.xml:7`, `addons/l10n_sa/wizard/account_move_reversal_views.xml:8`, `addons/l10n_sa/views/res_config_settings_views.xml:4`, `addons/l10n_sa/views/res_config_settings_views.xml:6`, `addons/l10n_sa/views/account_move_views.xml:6`, `addons/l10n_sa/views/account_move_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sa/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `account.chart.template` (addons/l10n_sa/demo/account_demo.py:7); inherits `res.partner` (addons/l10n_sa/models/res_partner.py:7); inherits `account.chart.template` (addons/l10n_sa/models/template_sa.py:6); `account.move` (addons/l10n_sa/models/account_move.py:11); inherits `account.move.line` (addons/l10n_sa/models/account_move_line.py:4); `zatca.mixin` (addons/l10n_sa/models/zatca_mixin.py:15); inherits `ir.attachment` (addons/l10n_sa/models/ir_attachment.py:5); inherits `account.move.reversal` (addons/l10n_sa/wizard/account_move_reversal.py:5); inherits `account.debit.note` (addons/l10n_sa/wizard/account_debit_note.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_gcc_invoice`, `account`, `account_debit_note`, `l10n_account_withholding_tax`
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

- `addons/l10n_sa/__init__.py`
- `addons/l10n_sa/__manifest__.py`
- `addons/l10n_sa/data/account_data.xml`
- `addons/l10n_sa/data/account_tax_report_data.xml`
- `addons/l10n_sa/data/account_tax_report_withholding_data.xml`
- `addons/l10n_sa/data/report_paperformat_data.xml`
- `addons/l10n_sa/data/template/account.account-sa.csv`
- `addons/l10n_sa/data/template/account.depreciation.model-sa.csv`
- `addons/l10n_sa/data/template/account.fiscal.position-sa.csv`
- `addons/l10n_sa/data/template/account.tax-sa.csv`
- `addons/l10n_sa/data/template/account.tax.group-sa.csv`
- `addons/l10n_sa/demo/__init__.py`
- `addons/l10n_sa/demo/account_demo.py`
- `addons/l10n_sa/demo/demo_company.xml`
- `addons/l10n_sa/i18n/ar.po`
- `addons/l10n_sa/i18n/l10n_sa.pot`
- `addons/l10n_sa/migrations/2.2/end-migrate.py`
- `addons/l10n_sa/migrations/2.3/end-migrate.py`
- `addons/l10n_sa/migrations/2.3/post-migrate.py`
- `addons/l10n_sa/migrations/2.3/pre-migrate.py`
- `addons/l10n_sa/models/__init__.py`
- `addons/l10n_sa/models/account_move.py`
- `addons/l10n_sa/models/account_move_line.py`
- `addons/l10n_sa/models/ir_attachment.py`
- `addons/l10n_sa/models/res_partner.py`
- `addons/l10n_sa/models/template_sa.py`
- `addons/l10n_sa/models/zatca_mixin.py`
- `addons/l10n_sa/static/src/scss/styles.scss`
- `addons/l10n_sa/tests/__init__.py`
- `addons/l10n_sa/tests/test_account_move.py`
- `addons/l10n_sa/tests/test_sa_additional_identifiers.py`
- `addons/l10n_sa/tools/partner_identifiers.py`
- `addons/l10n_sa/views/account_move_views.xml`
- `addons/l10n_sa/views/report_invoice.xml`
- `addons/l10n_sa/views/report_templates_views.xml`
- `addons/l10n_sa/views/res_config_settings_views.xml`
- `addons/l10n_sa/wizard/__init__.py`
- `addons/l10n_sa/wizard/account_debit_note.py`
- `addons/l10n_sa/wizard/account_debit_note.xml`
- `addons/l10n_sa/wizard/account_move_reversal.py`
- `addons/l10n_sa/wizard/account_move_reversal_views.xml`
