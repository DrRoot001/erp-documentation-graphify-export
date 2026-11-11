# Module: l10n_pl_edi

- **Module ID:** MOD-299
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pl_edi`
- **Manifest:** `addons/l10n_pl_edi/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Support for FA(3) electronic invoices in Poland via KSeF

**Manifest description:**

Export FA(3) compliant XML invoices and prepare for integration with KSeF.

**Scope evidence:** The module contains 40 files, including 15 Python, 19 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_pl`, `certificate`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 19
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 5
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 102 methods, 0 constraint handlers, 1 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_pl_edi/models/res_partner.py:4`, `addons/l10n_pl_edi/models/res_config_settings.py:10`, `addons/l10n_pl_edi/models/account_journal.py:4`, `addons/l10n_pl_edi/models/account_move.py:24`, `addons/l10n_pl_edi/models/account_move_send.py:11`, `addons/l10n_pl_edi/models/res_company.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 19 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pl_edi/demo/account_invoice_demo.xml:4`, `addons/l10n_pl_edi/data/fa3_template.xml:8`, `addons/l10n_pl_edi/data/ir_cron_data.xml:4`, `addons/l10n_pl_edi/data/ir_cron_data.xml:16`, `addons/l10n_pl_edi/data/ir_cron_data.xml:26`, `addons/l10n_pl_edi/views/res_config_settings_views.xml:3`, `addons/l10n_pl_edi/views/report_invoice.xml:3`, `addons/l10n_pl_edi/views/account_move_views.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_pl_edi/__manifest__.py`, `addons/l10n_pl_edi/models/account_move.py`, `addons/l10n_pl_edi/models/res_company.py`, `addons/l10n_pl_edi/data/ir_cron_data.xml`, `addons/l10n_pl_edi/tests/test_l10n_pl_edi.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_pl_edi/models/account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pl_edi/tests/test_l10n_pl_edi.py`, `addons/l10n_pl_edi/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 19; representative identifiers: `demo_l10n_pl_partner_a`, `Polish FA(3) XML Template`, `cron_auto_checks_the_polish_invoice_status`, `cron_l10n_pl_edi_ksef_download_bills`, `cron_l10n_pl_edi_refresh_tokens`, `res_config_settings_view_form_l10n_pl_edi`, `report_invoice_document`, `view_move_form_l10n_pl_edi`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_pl_edi/data/fa3_template.xml:8`, `addons/l10n_pl_edi/views/report_invoice.xml:3`
- View/action field declarations: 4; representative evidence: `addons/l10n_pl_edi/views/res_config_settings_views.xml:5`, `addons/l10n_pl_edi/views/res_config_settings_views.xml:7`, `addons/l10n_pl_edi/views/account_move_views.xml:4`, `addons/l10n_pl_edi/views/account_move_views.xml:6`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pl_edi/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_pl_edi/__manifest__.py`, `addons/l10n_pl_edi/models/account_move.py`, `addons/l10n_pl_edi/models/res_company.py`, `addons/l10n_pl_edi/data/ir_cron_data.xml`, `addons/l10n_pl_edi/tests/test_l10n_pl_edi.py`
- **Report entry points:** `addons/l10n_pl_edi/models/account_move.py`

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `res.partner` (addons/l10n_pl_edi/models/res_partner.py:4); inherits `res.config.settings` (addons/l10n_pl_edi/models/res_config_settings.py:10); inherits `account.journal` (addons/l10n_pl_edi/models/account_journal.py:4); inherits `account.move` (addons/l10n_pl_edi/models/account_move.py:24); inherits `account.move.send` (addons/l10n_pl_edi/models/account_move_send.py:11); inherits `res.company` (addons/l10n_pl_edi/models/res_company.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_pl`, `certificate`
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

- `addons/l10n_pl_edi/__init__.py`
- `addons/l10n_pl_edi/__manifest__.py`
- `addons/l10n_pl_edi/data/fa3_schema.xsd`
- `addons/l10n_pl_edi/data/fa3_template.xml`
- `addons/l10n_pl_edi/data/ir_cron_data.xml`
- `addons/l10n_pl_edi/data/neutralize.sql`
- `addons/l10n_pl_edi/demo/account_invoice_demo.xml`
- `addons/l10n_pl_edi/exceptions.py`
- `addons/l10n_pl_edi/i18n/l10n_pl_edi.pot`
- `addons/l10n_pl_edi/i18n/pl.po`
- `addons/l10n_pl_edi/models/__init__.py`
- `addons/l10n_pl_edi/models/account_journal.py`
- `addons/l10n_pl_edi/models/account_move.py`
- `addons/l10n_pl_edi/models/account_move_send.py`
- `addons/l10n_pl_edi/models/res_company.py`
- `addons/l10n_pl_edi/models/res_config_settings.py`
- `addons/l10n_pl_edi/models/res_partner.py`
- `addons/l10n_pl_edi/tests/__init__.py`
- `addons/l10n_pl_edi/tests/certificate/l10n_pl_edi_test.key`
- `addons/l10n_pl_edi/tests/certificate/l10n_pl_edi_test.pem`
- `addons/l10n_pl_edi/tests/export_xmls/fa3_bill.xml`
- `addons/l10n_pl_edi/tests/export_xmls/fa3_invoice_foreign_currency.xml`
- `addons/l10n_pl_edi/tests/export_xmls/full_paid_invoice.xml`
- `addons/l10n_pl_edi/tests/export_xmls/partial_paid_invoice_bank_cash.xml`
- `addons/l10n_pl_edi/tests/export_xmls/standard_fa3_format_credit_note_reverse_charge.xml`
- `addons/l10n_pl_edi/tests/export_xmls/standard_fa3_format_invoice_reverse_charge.xml`
- `addons/l10n_pl_edi/tests/export_xmls/standerd_fa3_credit_note.xml`
- `addons/l10n_pl_edi/tests/export_xmls/standert_fa3_format.xml`
- `addons/l10n_pl_edi/tests/import_xmls/fa3_standard_bill.xml`
- `addons/l10n_pl_edi/tests/import_xmls/invoice_from_foreign_country.xml`
- `addons/l10n_pl_edi/tests/import_xmls/invoice_with_discount.xml`
- `addons/l10n_pl_edi/tests/import_xmls/invoice_with_net_and_gross_unit_price.xml`
- `addons/l10n_pl_edi/tests/import_xmls/invoice_with_zero_value_line_missing_unit_prices.xml`
- `addons/l10n_pl_edi/tests/test_l10n_pl_edi.py`
- `addons/l10n_pl_edi/tools/__init__.py`
- `addons/l10n_pl_edi/tools/ksef_api_service.py`
- `addons/l10n_pl_edi/tools/xades_signer.py`
- `addons/l10n_pl_edi/views/account_move_views.xml`
- `addons/l10n_pl_edi/views/report_invoice.xml`
- `addons/l10n_pl_edi/views/res_config_settings_views.xml`
