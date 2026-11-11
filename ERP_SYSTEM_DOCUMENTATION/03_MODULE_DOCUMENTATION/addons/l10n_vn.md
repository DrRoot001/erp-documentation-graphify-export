# Module: l10n_vn

- **Module ID:** MOD-341
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_vn`
- **Manifest:** `addons/l10n_vn/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the module to manage the accounting chart, bank information for Vietnam in Odoo.
========================================================================================

- This module applies to companies based in Vietnamese Accounting Standard (VAS)
  with Chart of account under Circular No. 200/2014/TT-BTC
- Add Vietnamese bank information (like name, bic ..) as announced and yearly updated by State Bank
  of Viet Nam (https://sbv.gov.vn/webcenter/portal/en/home/sbv/paytreasury/bankidno).
- Add VietQR feature for invoice

**Credits:**
    - General Solutions.
    - Trobz
    - Jean Nguyen - The Bean Family (https://github.com/anhjean/vietqr) for VietQR.

**Scope evidence:** The module contains 22 files, including 12 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_qr_code_emv`, `account`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 5
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

- **Description:** 3 model declarations, 22 methods, 1 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_vn/models/res_bank.py:9`, `addons/l10n_vn/models/account_move.py:5`, `addons/l10n_vn/models/template_vn.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 119 record/template/menu identifiers.
- **Evidence:** `addons/l10n_vn/demo/demo_company.xml:3`, `addons/l10n_vn/demo/demo_company.xml:16`, `addons/l10n_vn/data/account_tax_report_data.xml:4`, `addons/l10n_vn/data/account_tax_report_data.xml:22`, `addons/l10n_vn/data/account_tax_report_data.xml:28`, `addons/l10n_vn/data/account_tax_report_data.xml:34`, `addons/l10n_vn/data/account_tax_report_data.xml:40`, `addons/l10n_vn/data/account_tax_report_data.xml:48`, `addons/l10n_vn/data/account_tax_report_data.xml:54`, `addons/l10n_vn/data/account_tax_report_data.xml:61`, `addons/l10n_vn/data/account_tax_report_data.xml:67`, `addons/l10n_vn/data/account_tax_report_data.xml:72`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_vn/tests/test_l10n_vn_emv_qr.py`, `addons/l10n_vn/tests/test_l10n_vn_account_codes.py`, `addons/l10n_vn/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `base.partner_demo_company_vn`, `base.demo_company_vn`, `form_01_gtgt_report`, `purchase_tax_report_invoice_number`, `purchase_tax_report_invoice_date`, `purchase_tax_report_partner_id`, `purchase_tax_report_tax_id`, `form_01_gtgt_report_A`, `form_01_gtgt_report_A_code_1`, `form_01_gtgt_report_B`, `form_01_gtgt_report_B_code_2`, `form_01_gtgt_report_B_applied_carryover`, `form_01_gtgt_report_B_balance`, `form_01_gtgt_report_C`, `form_01_gtgt_report_C_I`, `form_01_gtgt_report_C_I_1`, `form_01_gtgt_report_C_I_1_code_1`, `form_01_gtgt_report_C_I_1_amount_untaxed`, `form_01_gtgt_report_C_I_1_amount_untaxed_exempt`, `form_01_gtgt_report_C_I_1_amount_untaxed_0`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/l10n_vn/views/res_config_settings_views.xml:6`, `addons/l10n_vn/views/res_config_settings_views.xml:8`, `addons/l10n_vn/views/res_bank_views.xml:6`, `addons/l10n_vn/views/res_bank_views.xml:8`, `addons/l10n_vn/views/account_move_views.xml:6`, `addons/l10n_vn/views/account_move_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_vn/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner.bank` (addons/l10n_vn/models/res_bank.py:9); inherits `account.move` (addons/l10n_vn/models/account_move.py:5); inherits `account.chart.template` (addons/l10n_vn/models/template_vn.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_qr_code_emv`, `account`
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

- `addons/l10n_vn/__init__.py`
- `addons/l10n_vn/__manifest__.py`
- `addons/l10n_vn/data/account_tax_report_data.xml`
- `addons/l10n_vn/data/template/account.account-vn.csv`
- `addons/l10n_vn/data/template/account.tax-vn.csv`
- `addons/l10n_vn/data/template/account.tax.group-vn.csv`
- `addons/l10n_vn/demo/demo_company.xml`
- `addons/l10n_vn/i18n/l10n_vn.pot`
- `addons/l10n_vn/i18n/vi.po`
- `addons/l10n_vn/migrations/14.0.2.0.1/post-migration.py`
- `addons/l10n_vn/migrations/17.0.2.0.2/post-migration.py`
- `addons/l10n_vn/migrations/2.0.3/end-migrate_update_taxes.py`
- `addons/l10n_vn/models/__init__.py`
- `addons/l10n_vn/models/account_move.py`
- `addons/l10n_vn/models/res_bank.py`
- `addons/l10n_vn/models/template_vn.py`
- `addons/l10n_vn/tests/__init__.py`
- `addons/l10n_vn/tests/test_l10n_vn_account_codes.py`
- `addons/l10n_vn/tests/test_l10n_vn_emv_qr.py`
- `addons/l10n_vn/views/account_move_views.xml`
- `addons/l10n_vn/views/res_bank_views.xml`
- `addons/l10n_vn/views/res_config_settings_views.xml`
