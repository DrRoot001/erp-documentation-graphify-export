# Module: l10n_ch

- **Module ID:** MOD-146
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ch`
- **Manifest:** `addons/l10n_ch/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Swiss localization
==================
This module defines a chart of account for Switzerland (Swiss PME/KMU 2015), taxes and enables the generation of a QR-bill when you print an invoice or send it by mail.
The QR bill is attached to the invoice and eases its payment.

A QR-bill will be generated if:
    - The partner set on your invoice has a complete address (street, city, postal code and country) in Switzerland
    - The option to generate the Swiss QR-code is selected on the invoice (done by default)
    - A correct account number/QR IBAN is set on your bank journal
    - (when using a QR-IBAN): the payment reference of the invoice is a QR-reference

The generation of the QR-bill is automatic if you meet the previous criteria. The QR-bill will be appended after the invoice when printing or sending by mail.

**Scope evidence:** The module contains 57 files, including 25 Python, 11 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `account_edi_ubl_cii`, `l10n_din5008`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 11
- Browser asset files: 0
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 2
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ch/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 70 methods, 0 constraint handlers, 1 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/l10n_ch/models/res_bank.py:43`, `addons/l10n_ch/models/account_payment.py:8`, `addons/l10n_ch/models/ir_actions_report.py:14`, `addons/l10n_ch/models/template_ch.py:6`, `addons/l10n_ch/models/account_journal.py:7`, `addons/l10n_ch/models/account_invoice.py:12`, `addons/l10n_ch/models/account_move_send.py:4`, `addons/l10n_ch/report/swissqr_report.py:5`, `addons/l10n_ch/wizard/setup_wizards.py:5`, `addons/l10n_ch/wizard/qr_invoice_wizard.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 11 XML files and 0 JavaScript/TypeScript files; static XML analysis found 96 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ch/demo/account_cash_rounding.xml:4`, `addons/l10n_ch/demo/demo_company.xml:3`, `addons/l10n_ch/demo/demo_company.xml:16`, `addons/l10n_ch/demo/demo_company.xml:23`, `addons/l10n_ch/demo/res_partner_demo.xml:3`, `addons/l10n_ch/demo/res_partner_demo.xml:16`, `addons/l10n_ch/report/swissqr_report.xml:4`, `addons/l10n_ch/report/swissqr_report.xml:17`, `addons/l10n_ch/report/swissqr_report.xml:26`, `addons/l10n_ch/report/swissqr_report.xml:220`, `addons/l10n_ch/report/swissqr_report.xml:229`, `addons/l10n_ch/data/account_tax_report_data.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ch/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_ch/models/account_move_send.py`, `addons/l10n_ch/tests/test_l10n_ch_qr_print.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_ch/models/ir_actions_report.py`, `addons/l10n_ch/models/account_move_send.py`, `addons/l10n_ch/report/swissqr_report.xml`, `addons/l10n_ch/tests/test_ch_qr_code.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_ch/tests/test_swissqr.py`, `addons/l10n_ch/tests/test_l10n_ch_qr_print.py`, `addons/l10n_ch/tests/test_ch_qr_code.py`, `addons/l10n_ch/tests/test_gen_qrr_reference.py`, `addons/l10n_ch/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 11; representative identifiers: `cash_rounding_5_centime`, `base.partner_demo_company_ch`, `base.demo_bank_ch`, `base.demo_company_ch`, `res_partner_ch_qr`, `bank_iban_main_partner_ch`, `paperformat_euro_no_margin`, `l10n_ch_qr_report`, `l10n_ch_swissqr_template`, `l10n_ch.qr_report_main`, `minimal_layout_with_report_attribute`, `tax_report`, `tax_report_balance`, `account_tax_report_line_chiffre_af`, `account_tax_report_line_chtax_200`, `account_tax_report_line_chtax_205`, `account_tax_report_line_chtax_205_tag`, `account_tax_report_line_chtax_220_289`, `account_tax_report_line_chtax_220_289_tag`, `account_tax_report_line_chtax_221`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_ch/report/swissqr_report.xml:26`, `addons/l10n_ch/report/swissqr_report.xml:220`, `addons/l10n_ch/report/swissqr_report.xml:229`, `addons/l10n_ch/views/account_invoice.xml:3`
- View/action field declarations: 13; representative evidence: `addons/l10n_ch/report/swissqr_report.xml:19`, `addons/l10n_ch/views/qr_invoice_wizard_view.xml:5`, `addons/l10n_ch/views/qr_invoice_wizard_view.xml:6`, `addons/l10n_ch/views/qr_invoice_wizard_view.xml:28`, `addons/l10n_ch/views/qr_invoice_wizard_view.xml:29`, `addons/l10n_ch/views/res_config_settings_views.xml:6`, `addons/l10n_ch/views/res_config_settings_views.xml:8`, `addons/l10n_ch/views/account_payment_view.xml:6`, `addons/l10n_ch/views/account_payment_view.xml:8`, `addons/l10n_ch/views/setup_wizard_views.xml:6`, `addons/l10n_ch/views/setup_wizard_views.xml:8`, `addons/l10n_ch/views/res_bank_view.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ch/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_ch/models/account_move_send.py`, `addons/l10n_ch/tests/test_l10n_ch_qr_print.py`
- **Report entry points:** `addons/l10n_ch/models/ir_actions_report.py`, `addons/l10n_ch/models/account_move_send.py`, `addons/l10n_ch/report/swissqr_report.xml`, `addons/l10n_ch/tests/test_ch_qr_code.py`

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `res.partner.bank` (addons/l10n_ch/models/res_bank.py:43); inherits `account.payment` (addons/l10n_ch/models/account_payment.py:8); inherits `ir.actions.report` (addons/l10n_ch/models/ir_actions_report.py:14); inherits `account.chart.template` (addons/l10n_ch/models/template_ch.py:6); inherits `account.journal` (addons/l10n_ch/models/account_journal.py:7); inherits `account.move` (addons/l10n_ch/models/account_invoice.py:12); inherits `account.move.send` (addons/l10n_ch/models/account_move_send.py:4); `report.l10n_ch.qr_report_main` (addons/l10n_ch/report/swissqr_report.py:5); inherits `account.setup.bank.manual.config` (addons/l10n_ch/wizard/setup_wizards.py:5); `l10n_ch.qr_invoice.wizard` (addons/l10n_ch/wizard/qr_invoice_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `account_edi_ubl_cii`, `l10n_din5008`
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

- `addons/l10n_ch/__init__.py`
- `addons/l10n_ch/__manifest__.py`
- `addons/l10n_ch/data/account_tax_report_data.xml`
- `addons/l10n_ch/data/template/account.account-ch.csv`
- `addons/l10n_ch/data/template/account.asset-ch.csv`
- `addons/l10n_ch/data/template/account.fiscal.position-ch.csv`
- `addons/l10n_ch/data/template/account.tax-ch.csv`
- `addons/l10n_ch/data/template/account.tax.group-ch.csv`
- `addons/l10n_ch/demo/account_cash_rounding.xml`
- `addons/l10n_ch/demo/demo_company.xml`
- `addons/l10n_ch/demo/res_partner_demo.xml`
- `addons/l10n_ch/i18n/de.po`
- `addons/l10n_ch/i18n/fr.po`
- `addons/l10n_ch/i18n/it.po`
- `addons/l10n_ch/i18n/l10n_ch.pot`
- `addons/l10n_ch/migrations/0.0.0/pre-migrate-qr-template.py`
- `addons/l10n_ch/migrations/11.1/end-migrate_update_taxes.py`
- `addons/l10n_ch/migrations/11.2/pre-migrate.py`
- `addons/l10n_ch/migrations/11.3/end-migrate.py`
- `addons/l10n_ch/migrations/9.0.9.0/pre-set_tags_and_taxes_updatable.py`
- `addons/l10n_ch/models/__init__.py`
- `addons/l10n_ch/models/account_invoice.py`
- `addons/l10n_ch/models/account_journal.py`
- `addons/l10n_ch/models/account_move_send.py`
- `addons/l10n_ch/models/account_payment.py`
- `addons/l10n_ch/models/ir_actions_report.py`
- `addons/l10n_ch/models/res_bank.py`
- `addons/l10n_ch/models/template_ch.py`
- `addons/l10n_ch/report/__init__.py`
- `addons/l10n_ch/report/swissqr_report.py`
- `addons/l10n_ch/report/swissqr_report.xml`
- `addons/l10n_ch/security/ir.access.csv`
- `addons/l10n_ch/static/src/font/LiberationSans-Bold.woff`
- `addons/l10n_ch/static/src/font/LiberationSans-Regular.woff`
- `addons/l10n_ch/static/src/font/liberation_sans_license.txt`
- `addons/l10n_ch/static/src/font/ocrb-license.txt`
- `addons/l10n_ch/static/src/font/ocrb.otf`
- `addons/l10n_ch/static/src/img/CH-Cross_7mm.png`
- `addons/l10n_ch/static/src/img/background_virgin_isr.png`
- `addons/l10n_ch/static/src/img/background_virgin_isr_bank.png`
- `addons/l10n_ch/static/src/img/scissors_h.png`
- `addons/l10n_ch/static/src/img/scissors_v.png`
- `addons/l10n_ch/static/src/scss/report_swissqr.scss`
- `addons/l10n_ch/tests/__init__.py`
- `addons/l10n_ch/tests/test_ch_qr_code.py`
- `addons/l10n_ch/tests/test_gen_qrr_reference.py`
- `addons/l10n_ch/tests/test_l10n_ch_qr_print.py`
- `addons/l10n_ch/tests/test_swissqr.py`
- `addons/l10n_ch/views/account_invoice.xml`
- `addons/l10n_ch/views/account_payment_view.xml`
- `addons/l10n_ch/views/qr_invoice_wizard_view.xml`
- `addons/l10n_ch/views/res_bank_view.xml`
- `addons/l10n_ch/views/res_config_settings_views.xml`
- `addons/l10n_ch/views/setup_wizard_views.xml`
- `addons/l10n_ch/wizard/__init__.py`
- `addons/l10n_ch/wizard/qr_invoice_wizard.py`
- `addons/l10n_ch/wizard/setup_wizards.py`
