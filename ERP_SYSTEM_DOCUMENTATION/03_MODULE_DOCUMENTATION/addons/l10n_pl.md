# Module: l10n_pl

- **Module ID:** MOD-298
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pl`
- **Manifest:** `addons/l10n_pl/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the module to manage the accounting chart and taxes for Poland in Odoo.
==================================================================================

To jest moduł do tworzenia wzorcowego planu kont, podatków, obszarów podatkowych i
rejestrów podatkowych. Moduł ustawia też konta do kupna i sprzedaży towarów
zakładając, że wszystkie towary są w obrocie hurtowym.

Niniejszy moduł jest przeznaczony dla odoo 8.0.
Wewnętrzny numer wersji OpenGLOBE 1.02

**Scope evidence:** The module contains 38 files, including 20 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_pl/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 61 methods, 0 constraint handlers, 0 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/l10n_pl/models/res_partner.py:7`, `addons/l10n_pl/models/bank_account_verification.py:16`, `addons/l10n_pl/models/res_config_settings.py:7`, `addons/l10n_pl/models/account_payment.py:6`, `addons/l10n_pl/models/product.py:4`, `addons/l10n_pl/models/template_pl.py:6`, `addons/l10n_pl/models/l10n_pl_tax_office.py:4`, `addons/l10n_pl/models/account_move.py:4`, `addons/l10n_pl/models/res_company.py:4`, `addons/l10n_pl/wizard/account_payment_register.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 108 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pl/demo/demo_company.xml:3`, `addons/l10n_pl/demo/demo_company.xml:16`, `addons/l10n_pl/demo/demo_company.xml:21`, `addons/l10n_pl/wizard/account_payment_register_views.xml:4`, `addons/l10n_pl/data/account_tax_report_data.xml:3`, `addons/l10n_pl/data/account_tax_report_data.xml:11`, `addons/l10n_pl/data/account_tax_report_data.xml:18`, `addons/l10n_pl/data/account_tax_report_data.xml:24`, `addons/l10n_pl/data/account_tax_report_data.xml:29`, `addons/l10n_pl/data/account_tax_report_data.xml:36`, `addons/l10n_pl/data/account_tax_report_data.xml:42`, `addons/l10n_pl/data/account_tax_report_data.xml:47`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_pl/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_pl/models/bank_account_verification.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/l10n_pl/tests/test_bank_account_verification.py`, `addons/l10n_pl/tests/test_taxable_supply_date_with_lock_dates.py`, `addons/l10n_pl/tests/__init__.py`, `addons/l10n_pl/tests/utils/utils.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `base.partner_demo_company_pl`, `base.demo_company_pl`, `base.demo_bank_pl`, `l10n_pl_view_account_payment_register_form`, `tax_report`, `tax_report_balance`, `account_tax_report_line_razem_c`, `account_tax_report_line_kraj_zwolnione`, `account_tax_report_line_kraj_zwolnione_tag`, `account_tax_report_line_poza_kraj`, `account_tax_report_line_poza_kraj_tag`, `account_tax_report_line_poza_kraj_tag_rc`, `account_tax_report_line_uslugi_art_100_1_4`, `account_tax_report_line_uslugi_art_100_1_4_tag`, `account_tax_report_line_triangular_buyer_2nd_payer`, `account_tax_report_line_triangular_buyer_2nd_payer_tag`, `account_tax_report_line_uslugi_kraj_0`, `account_tax_report_line_uslugi_kraj_0_tag`, `account_tax_report_line_uslugi_kraj_0_formula`, `account_tax_report_line_towary_art_129`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 12; representative evidence: `addons/l10n_pl/wizard/account_payment_register_views.xml:6`, `addons/l10n_pl/wizard/account_payment_register_views.xml:8`, `addons/l10n_pl/views/res_config_settings_views.xml:5`, `addons/l10n_pl/views/res_config_settings_views.xml:7`, `addons/l10n_pl/views/account_payment_view.xml:6`, `addons/l10n_pl/views/account_payment_view.xml:8`, `addons/l10n_pl/views/account_move_views.xml:5`, `addons/l10n_pl/views/account_move_views.xml:7`, `addons/l10n_pl/views/product_views.xml:5`, `addons/l10n_pl/views/product_views.xml:7`, `addons/l10n_pl/views/res_partner_views.xml:7`, `addons/l10n_pl/views/res_partner_views.xml:9`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pl/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_pl/models/bank_account_verification.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `res.partner` (addons/l10n_pl/models/res_partner.py:7); `l10n_pl.bank.account.verification` (addons/l10n_pl/models/bank_account_verification.py:16); inherits `res.config.settings` (addons/l10n_pl/models/res_config_settings.py:7); inherits `account.payment` (addons/l10n_pl/models/account_payment.py:6); inherits `product.template` (addons/l10n_pl/models/product.py:4); inherits `account.chart.template` (addons/l10n_pl/models/template_pl.py:6); `l10n_pl.l10n_pl_tax_office` (addons/l10n_pl/models/l10n_pl_tax_office.py:4); inherits `account.move` (addons/l10n_pl/models/account_move.py:4); inherits `res.company` (addons/l10n_pl/models/res_company.py:4); inherits `account.payment.register` (addons/l10n_pl/wizard/account_payment_register.py:6)
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

- `addons/l10n_pl/__init__.py`
- `addons/l10n_pl/__manifest__.py`
- `addons/l10n_pl/data/account.account.tag.csv`
- `addons/l10n_pl/data/account_tax_report_data.xml`
- `addons/l10n_pl/data/l10n_pl.l10n_pl_tax_office.csv`
- `addons/l10n_pl/data/template/account.account-pl.csv`
- `addons/l10n_pl/data/template/account.fiscal.position-pl.csv`
- `addons/l10n_pl/data/template/account.tax-pl.csv`
- `addons/l10n_pl/data/template/account.tax.group-pl.csv`
- `addons/l10n_pl/demo/demo_company.xml`
- `addons/l10n_pl/i18n/l10n_pl.pot`
- `addons/l10n_pl/i18n/pl.po`
- `addons/l10n_pl/migrations/2.1/end-migrate.py`
- `addons/l10n_pl/migrations/9.0.2.0/pre-set_tags_and_taxes_updatable.py`
- `addons/l10n_pl/models/__init__.py`
- `addons/l10n_pl/models/account_move.py`
- `addons/l10n_pl/models/account_payment.py`
- `addons/l10n_pl/models/bank_account_verification.py`
- `addons/l10n_pl/models/l10n_pl_tax_office.py`
- `addons/l10n_pl/models/product.py`
- `addons/l10n_pl/models/res_company.py`
- `addons/l10n_pl/models/res_config_settings.py`
- `addons/l10n_pl/models/res_partner.py`
- `addons/l10n_pl/models/template_pl.py`
- `addons/l10n_pl/security/ir.access.csv`
- `addons/l10n_pl/tests/__init__.py`
- `addons/l10n_pl/tests/test_bank_account_verification.py`
- `addons/l10n_pl/tests/test_taxable_supply_date_with_lock_dates.py`
- `addons/l10n_pl/tests/utils/fake_response.json`
- `addons/l10n_pl/tests/utils/utils.py`
- `addons/l10n_pl/views/account_move_views.xml`
- `addons/l10n_pl/views/account_payment_view.xml`
- `addons/l10n_pl/views/product_views.xml`
- `addons/l10n_pl/views/res_config_settings_views.xml`
- `addons/l10n_pl/views/res_partner_views.xml`
- `addons/l10n_pl/wizard/__init__.py`
- `addons/l10n_pl/wizard/account_payment_register.py`
- `addons/l10n_pl/wizard/account_payment_register_views.xml`
