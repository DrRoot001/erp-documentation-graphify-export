# Module: l10n_fr_pos_cert

- **Module ID:** MOD-197
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fr_pos_cert`
- **Manifest:** `addons/l10n_fr_pos_cert/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This add-on brings the technical requirements of the French regulation CGI art. 286, I. 3° bis that stipulates certain criteria concerning the inalterability, security, storage and archiving of data related to sales to private individuals (B2C).
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Install it if you use the Point of Sale app to sell to individuals.

The module adds following features:

    Inalterability: deactivation of all the ways to cancel or modify key data of POS orders, invoices and journal entries

    Security: chaining algorithm to verify the inalterability

    Storage: automatic sales closings with computation of both period and cumulative totals (daily, monthly, annually)

    Access to download the mandatory Certificate of Conformity delivered by Odoo SA (only for Odoo Enterprise users)

**Scope evidence:** The module contains 39 files, including 16 Python, 8 XML, and 11 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_fr_account`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 11
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 3
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_fr_pos_cert/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 37 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_fr_pos_cert/models/account_closing.py:11`, `addons/l10n_fr_pos_cert/models/pos.py:14`, `addons/l10n_fr_pos_cert/models/pos.py:27`, `addons/l10n_fr_pos_cert/models/pos.py:47`, `addons/l10n_fr_pos_cert/models/pos.py:226`, `addons/l10n_fr_pos_cert/models/account_fiscal_position.py:7`, `addons/l10n_fr_pos_cert/models/res_company.py:24`, `addons/l10n_fr_pos_cert/report/pos_hash_integrity.py:7`, `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 11 JavaScript/TypeScript files; static XML analysis found 17 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fr_pos_cert/report/pos_hash_integrity.xml:4`, `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml:2`, `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml:11`, `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml:20`, `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.xml:4`, `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.xml:12`, `addons/l10n_fr_pos_cert/views/res_config_settings_views.xml:3`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:2`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:19`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:53`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:66`, `addons/l10n_fr_pos_cert/views/pos_views.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_fr_pos_cert/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_fr_pos_cert/__manifest__.py`, `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_fr_pos_cert/tests/test_frontend.py`, `addons/l10n_fr_pos_cert/tests/test_string_to_hash.py`, `addons/l10n_fr_pos_cert/tests/test_fr_pos.py`, `addons/l10n_fr_pos_cert/tests/test_hash.py`, `addons/l10n_fr_pos_cert/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `report_pos_hash_integrity`, `account_sale_closing_daily`, `account_sale_closing_monthly`, `account_sale_closing_annually`, `l10n_fr_pos_cert.pos_order_receipt`, `l10n_fr_pos_cert.pos_orderline_receipt_information`, `res_config_settings_view_form`, `list_view_account_sale_closing`, `form_view_account_sale_closing`, `action_list_view_account_sale_closing`, `menu_account_closing_reporting`, `pos_order_form_inherit`, `action_report_pos_hash_integrity`, `action_check_pos_hash_integrity`, `French Statements`, `menu_account_closing`, `menu_check_move_integrity_reporting`
- Menus: 4; representative evidence: `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:66`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml:16`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml:17`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml:18`
- Templates: 3; representative evidence: `addons/l10n_fr_pos_cert/report/pos_hash_integrity.xml:4`, `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.xml:4`, `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.xml:12`
- View/action field declarations: 11; representative evidence: `addons/l10n_fr_pos_cert/views/res_config_settings_views.xml:5`, `addons/l10n_fr_pos_cert/views/res_config_settings_views.xml:7`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:4`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:5`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:21`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:22`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:55`, `addons/l10n_fr_pos_cert/views/account_sale_closure.xml:56`, `addons/l10n_fr_pos_cert/views/pos_views.xml:4`, `addons/l10n_fr_pos_cert/views/pos_views.xml:6`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml:4`
- Browser assets: 11; representative files: `addons/l10n_fr_pos_cert/static/src/js/Chrome.js`, `addons/l10n_fr_pos_cert/static/src/js/pos_order_line.js`, `addons/l10n_fr_pos_cert/static/src/js/generate_printer_data.js`, `addons/l10n_fr_pos_cert/static/src/js/Popups/ClosePosPopup.js`, `addons/l10n_fr_pos_cert/static/src/app/services/pos.js`, `addons/l10n_fr_pos_cert/static/tests/tours/l10n_fr_pos_cert_tour.js`, `addons/l10n_fr_pos_cert/static/tests/unit/models/pos_order_line.test.js`, `addons/l10n_fr_pos_cert/static/tests/unit/screens/feedback_screen.test.js`, `addons/l10n_fr_pos_cert/static/tests/unit/data/pos_config.data.js`, `addons/l10n_fr_pos_cert/static/tests/unit/data/res_country.data.js`, `addons/l10n_fr_pos_cert/static/tests/unit/data/res_company.data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fr_pos_cert/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_fr_pos_cert/__manifest__.py`, `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml`, `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml`
- **Report entry points:** `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml`

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: `account.sale.closing` (addons/l10n_fr_pos_cert/models/account_closing.py:11); inherits `pos.config` (addons/l10n_fr_pos_cert/models/pos.py:14); inherits `pos.session` (addons/l10n_fr_pos_cert/models/pos.py:27); inherits `pos.order` (addons/l10n_fr_pos_cert/models/pos.py:47); inherits `pos.order.line` (addons/l10n_fr_pos_cert/models/pos.py:226); inherits `account.fiscal.position` (addons/l10n_fr_pos_cert/models/account_fiscal_position.py:7); inherits `res.company` (addons/l10n_fr_pos_cert/models/res_company.py:24); `report.l10n_fr_pos_cert.report_pos_hash_integrity` (addons/l10n_fr_pos_cert/report/pos_hash_integrity.py:7); inherits `pos.order.receipt` (addons/l10n_fr_pos_cert/receipt/pos_order_receipt.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_fr_account`, `point_of_sale`
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

- `addons/l10n_fr_pos_cert/__init__.py`
- `addons/l10n_fr_pos_cert/__manifest__.py`
- `addons/l10n_fr_pos_cert/data/account_sale_closure_cron.xml`
- `addons/l10n_fr_pos_cert/i18n/fr.po`
- `addons/l10n_fr_pos_cert/i18n/l10n_fr_pos_cert.pot`
- `addons/l10n_fr_pos_cert/models/__init__.py`
- `addons/l10n_fr_pos_cert/models/account_closing.py`
- `addons/l10n_fr_pos_cert/models/account_fiscal_position.py`
- `addons/l10n_fr_pos_cert/models/pos.py`
- `addons/l10n_fr_pos_cert/models/res_company.py`
- `addons/l10n_fr_pos_cert/receipt/__init__.py`
- `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.py`
- `addons/l10n_fr_pos_cert/receipt/pos_order_receipt.xml`
- `addons/l10n_fr_pos_cert/report/__init__.py`
- `addons/l10n_fr_pos_cert/report/pos_hash_integrity.py`
- `addons/l10n_fr_pos_cert/report/pos_hash_integrity.xml`
- `addons/l10n_fr_pos_cert/security/ir.access.csv`
- `addons/l10n_fr_pos_cert/static/src/app/services/pos.js`
- `addons/l10n_fr_pos_cert/static/src/css/pos.css`
- `addons/l10n_fr_pos_cert/static/src/js/Chrome.js`
- `addons/l10n_fr_pos_cert/static/src/js/Popups/ClosePosPopup.js`
- `addons/l10n_fr_pos_cert/static/src/js/generate_printer_data.js`
- `addons/l10n_fr_pos_cert/static/src/js/pos_order_line.js`
- `addons/l10n_fr_pos_cert/static/src/xml/OrderSummary.xml`
- `addons/l10n_fr_pos_cert/static/tests/tours/l10n_fr_pos_cert_tour.js`
- `addons/l10n_fr_pos_cert/static/tests/unit/data/pos_config.data.js`
- `addons/l10n_fr_pos_cert/static/tests/unit/data/res_company.data.js`
- `addons/l10n_fr_pos_cert/static/tests/unit/data/res_country.data.js`
- `addons/l10n_fr_pos_cert/static/tests/unit/models/pos_order_line.test.js`
- `addons/l10n_fr_pos_cert/static/tests/unit/screens/feedback_screen.test.js`
- `addons/l10n_fr_pos_cert/tests/__init__.py`
- `addons/l10n_fr_pos_cert/tests/test_fr_pos.py`
- `addons/l10n_fr_pos_cert/tests/test_frontend.py`
- `addons/l10n_fr_pos_cert/tests/test_hash.py`
- `addons/l10n_fr_pos_cert/tests/test_string_to_hash.py`
- `addons/l10n_fr_pos_cert/views/account_sale_closure.xml`
- `addons/l10n_fr_pos_cert/views/pos_inalterability_menuitem.xml`
- `addons/l10n_fr_pos_cert/views/pos_views.xml`
- `addons/l10n_fr_pos_cert/views/res_config_settings_views.xml`
