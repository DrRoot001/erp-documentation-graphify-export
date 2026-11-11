# Module: l10n_br

- **Module ID:** MOD-139
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_br`
- **Manifest:** `addons/l10n_br/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Base module for the Brazilian localization
==========================================

This module consists of:

- Generic Brazilian chart of accounts
- Brazilian taxes such as:

  - IPI
  - ICMS
  - PIS
  - COFINS
  - ISS
  - IR
  - CSLL

- Document Types as NFC-e, NFS-e, etc.
- Identification Documents as CNPJ and CPF

In addition to this module, the Brazilian Localizations is also
extended and complemented with several additional modules.

Brazil - Accounting Reports (l10n_br_reports)
---------------------------------------------
Adds a simple tax report that helps check the tax amount per tax group
in a given period of time. Also adds the P&L and BS adapted for the
Brazilian market.

Avatax Brazil (l10n_br_avatax)
------------------------------
Add Brazilian tax calculation via Avatax and all necessary fields needed to
configure Odoo in order to properly use Avatax and send the needed fiscal
information to retrieve the correct taxes.

Avatax for SOs in Brazil (l10n_br_avatax_sale)
----------------------------------------------
Same as the l10n_br_avatax module with the extension to the sales order module.

Electronic invoicing through Avatax (l10n_br_edi)
-------------------------------------------------
Create electronic sales invoices with Avatax.

**Scope evidence:** The module contains 50 files, including 24 Python, 14 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_qr_code_emv`, `l10n_latam_invoice_document`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 0
- XML/data/view/template files: 14
- Browser asset files: 1
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_br/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 38 methods, 2 constraint handlers, 1 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_br/demo/account_demo.py:6`, `addons/l10n_br/models/res_partner.py:8`, `addons/l10n_br/models/account.py:7`, `addons/l10n_br/models/template_br.py:6`, `addons/l10n_br/models/account_journal.py:5`, `addons/l10n_br/models/account_fiscal_position.py:12`, `addons/l10n_br/models/res_city.py:5`, `addons/l10n_br/models/l10n_br_zip_range.py:8`, `addons/l10n_br/models/res_country.py:6`, `addons/l10n_br/models/account_move.py:6`, `addons/l10n_br/models/res_partner_bank.py:10`, `addons/l10n_br/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 1 JavaScript/TypeScript files; static XML analysis found 269 record/template/menu identifiers.
- **Evidence:** `addons/l10n_br/demo/demo_company.xml:3`, `addons/l10n_br/demo/demo_company.xml:21`, `addons/l10n_br/data/account_tax_report_data.xml:3`, `addons/l10n_br/data/account_tax_report_data.xml:10`, `addons/l10n_br/data/account_tax_report_data.xml:17`, `addons/l10n_br/data/account_tax_report_data.xml:23`, `addons/l10n_br/data/account_tax_report_data.xml:29`, `addons/l10n_br/data/account_tax_report_data.xml:34`, `addons/l10n_br/data/account_tax_report_data.xml:43`, `addons/l10n_br/data/account_tax_report_data.xml:49`, `addons/l10n_br/data/account_tax_report_data.xml:54`, `addons/l10n_br/data/account_tax_report_data.xml:67`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_br/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_br/tests/__init__.py`, `addons/l10n_br/tests/test_l10n_br_fiscal_position.py`, `addons/l10n_br/tests/test_l10n_br_pix.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `base.partner_demo_company_br`, `base.demo_company_br`, `icms_tax_report`, `icms_tax_report_balance`, `tax_report_icms`, `tax_report_icms_tributada`, `tax_report_icms_1`, `tax_report_icms_1_tag`, `tax_report_icms_tributada_com`, `tax_report_icms_2`, `tax_report_icms_2_tag`, `icms_st_tax_report`, `icms_st_tax_report_balance`, `tax_report_icmsst`, `tax_report_icmsst_1`, `tax_report_icmsst_1_tag`, `tax_report_icmsst_2`, `tax_report_icmsst_2_tag`, `irpj_tax_report`, `irpj_tax_report_balance`
- Menus: 1; representative evidence: `addons/l10n_br/views/ir_ui_menu_brazil.xml:3`
- Templates: 3; representative evidence: `addons/l10n_br/views/report_invoice.xml:5`, `addons/l10n_br/views/report_invoice.xml:22`, `addons/l10n_br/views/portal_address_templates.xml:4`
- View/action field declarations: 18; representative evidence: `addons/l10n_br/views/res_city_view.xml:6`, `addons/l10n_br/views/res_city_view.xml:8`, `addons/l10n_br/views/res_config_settings_views.xml:6`, `addons/l10n_br/views/res_config_settings_views.xml:8`, `addons/l10n_br/views/res_company_views.xml:5`, `addons/l10n_br/views/res_company_views.xml:7`, `addons/l10n_br/views/res_bank_views.xml:5`, `addons/l10n_br/views/res_bank_views.xml:7`, `addons/l10n_br/views/account_fiscal_position_views.xml:6`, `addons/l10n_br/views/account_fiscal_position_views.xml:8`, `addons/l10n_br/views/res_partner_views.xml:6`, `addons/l10n_br/views/res_partner_views.xml:8`
- Browser assets: 1; representative files: `addons/l10n_br/static/src/interactions/address.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_br/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `account.chart.template` (addons/l10n_br/demo/account_demo.py:6); inherits `res.partner` (addons/l10n_br/models/res_partner.py:8); inherits `account.tax` (addons/l10n_br/models/account.py:7); inherits `account.chart.template` (addons/l10n_br/models/template_br.py:6); inherits `account.journal` (addons/l10n_br/models/account_journal.py:5); inherits `account.fiscal.position` (addons/l10n_br/models/account_fiscal_position.py:12); inherits `res.city` (addons/l10n_br/models/res_city.py:5); `l10n_br.zip.range` (addons/l10n_br/models/l10n_br_zip_range.py:8); inherits `res.country` (addons/l10n_br/models/res_country.py:6); inherits `account.move` (addons/l10n_br/models/account_move.py:6); inherits `res.partner.bank` (addons/l10n_br/models/res_partner_bank.py:10); inherits `res.company` (addons/l10n_br/models/res_company.py:6); inherits `account.move.reversal` (addons/l10n_br/wizard/account_move_reversal.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_qr_code_emv`, `l10n_latam_invoice_document`
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

- `addons/l10n_br/__init__.py`
- `addons/l10n_br/__manifest__.py`
- `addons/l10n_br/data/account_tax_report_data.xml`
- `addons/l10n_br/data/l10n_br.zip.range.csv`
- `addons/l10n_br/data/l10n_latam.document.type.csv`
- `addons/l10n_br/data/res.city.csv`
- `addons/l10n_br/data/res_country_data.xml`
- `addons/l10n_br/data/template/account.account-br.csv`
- `addons/l10n_br/data/template/account.depreciation.model-br.csv`
- `addons/l10n_br/data/template/account.fiscal.position-br.csv`
- `addons/l10n_br/data/template/account.tax-br.csv`
- `addons/l10n_br/data/template/account.tax.group-br.csv`
- `addons/l10n_br/demo/__init__.py`
- `addons/l10n_br/demo/account_demo.py`
- `addons/l10n_br/demo/demo_company.xml`
- `addons/l10n_br/i18n/l10n_br.pot`
- `addons/l10n_br/i18n/pt_BR.po`
- `addons/l10n_br/migrations/1.1/end-migrate-update_taxes.py`
- `addons/l10n_br/models/__init__.py`
- `addons/l10n_br/models/account.py`
- `addons/l10n_br/models/account_fiscal_position.py`
- `addons/l10n_br/models/account_journal.py`
- `addons/l10n_br/models/account_move.py`
- `addons/l10n_br/models/l10n_br_zip_range.py`
- `addons/l10n_br/models/res_city.py`
- `addons/l10n_br/models/res_company.py`
- `addons/l10n_br/models/res_country.py`
- `addons/l10n_br/models/res_partner.py`
- `addons/l10n_br/models/res_partner_bank.py`
- `addons/l10n_br/models/template_br.py`
- `addons/l10n_br/security/ir.access.csv`
- `addons/l10n_br/static/src/interactions/address.js`
- `addons/l10n_br/tests/__init__.py`
- `addons/l10n_br/tests/test_l10n_br_fiscal_position.py`
- `addons/l10n_br/tests/test_l10n_br_pix.py`
- `addons/l10n_br/tools/__init__.py`
- `addons/l10n_br/tools/partner_identifiers.py`
- `addons/l10n_br/views/account_fiscal_position_views.xml`
- `addons/l10n_br/views/account_journal_views.xml`
- `addons/l10n_br/views/account_view.xml`
- `addons/l10n_br/views/ir_ui_menu_brazil.xml`
- `addons/l10n_br/views/portal_address_templates.xml`
- `addons/l10n_br/views/report_invoice.xml`
- `addons/l10n_br/views/res_bank_views.xml`
- `addons/l10n_br/views/res_city_view.xml`
- `addons/l10n_br/views/res_company_views.xml`
- `addons/l10n_br/views/res_config_settings_views.xml`
- `addons/l10n_br/views/res_partner_views.xml`
- `addons/l10n_br/wizard/__init__.py`
- `addons/l10n_br/wizard/account_move_reversal.py`
