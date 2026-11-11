# Module: l10n_vn_edi_viettel_pos

- **Module ID:** MOD-343
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_vn_edi_viettel_pos`
- **Manifest:** `addons/l10n_vn_edi_viettel_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** POS E-invoicing using SInvoice by Viettel

**Manifest description:**

Vietnam - POS E-invoicing
=========================
Using SInvoice by Viettel

**Scope evidence:** The module contains 27 files, including 13 Python, 4 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_vn_edi_viettel`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 7
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_vn_edi_viettel_pos/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 25 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_vn_edi_viettel_pos/models/res_partner.py:8`, `addons/l10n_vn_edi_viettel_pos/models/pos_config.py:6`, `addons/l10n_vn_edi_viettel_pos/models/res_config_settings.py:6`, `addons/l10n_vn_edi_viettel_pos/models/pos_session.py:6`, `addons/l10n_vn_edi_viettel_pos/models/pos_order.py:6`, `addons/l10n_vn_edi_viettel_pos/models/account_move.py:6`, `addons/l10n_vn_edi_viettel_pos/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 7 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/l10n_vn_edi_viettel_pos/data/res_partner_data.xml:3`, `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:3`, `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:17`, `addons/l10n_vn_edi_viettel_pos/views/account_move_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel_pos/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/l10n_vn_edi_viettel_pos/views/account_move_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_vn_edi_viettel_pos/tests/test_l10n_vn_edi_pos_tour.py`, `addons/l10n_vn_edi_viettel_pos/tests/test_l10n_vn_edi_pos.py`, `addons/l10n_vn_edi_viettel_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `partner_walk_in_customer`, `res_config_settings_view_form_inherit_l10n_vn_edi_pos_account`, `res_config_settings_view_form_inherit_l10n_vn_edi_pos_pos`, `l10n_vn_edi_pos_fetch_tax_invoice`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:5`, `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:7`, `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:19`, `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml:21`
- Browser assets: 7; representative files: `addons/l10n_vn_edi_viettel_pos/static/src/overrides/models/pos_store.js`, `addons/l10n_vn_edi_viettel_pos/static/src/overrides/models/pos_order.js`, `addons/l10n_vn_edi_viettel_pos/static/src/overrides/utils/order_payment_validation.js`, `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/invoice_button/invoice_button.js`, `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`, `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/payment_screen/payment_screen.js`, `addons/l10n_vn_edi_viettel_pos/static/tests/tours/l10n_vn_edi_viettel_pos_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_vn_edi_viettel_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/l10n_vn_edi_viettel_pos/views/account_move_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.partner` (addons/l10n_vn_edi_viettel_pos/models/res_partner.py:8); inherits `pos.config` (addons/l10n_vn_edi_viettel_pos/models/pos_config.py:6); inherits `res.config.settings` (addons/l10n_vn_edi_viettel_pos/models/res_config_settings.py:6); inherits `pos.session` (addons/l10n_vn_edi_viettel_pos/models/pos_session.py:6); inherits `pos.order` (addons/l10n_vn_edi_viettel_pos/models/pos_order.py:6); inherits `account.move` (addons/l10n_vn_edi_viettel_pos/models/account_move.py:6); inherits `res.company` (addons/l10n_vn_edi_viettel_pos/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_vn_edi_viettel`, `point_of_sale`
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

- `addons/l10n_vn_edi_viettel_pos/__init__.py`
- `addons/l10n_vn_edi_viettel_pos/__manifest__.py`
- `addons/l10n_vn_edi_viettel_pos/data/res_partner_data.xml`
- `addons/l10n_vn_edi_viettel_pos/i18n/l10n_vn_edi_viettel_pos.pot`
- `addons/l10n_vn_edi_viettel_pos/i18n/vi.po`
- `addons/l10n_vn_edi_viettel_pos/models/__init__.py`
- `addons/l10n_vn_edi_viettel_pos/models/account_move.py`
- `addons/l10n_vn_edi_viettel_pos/models/pos_config.py`
- `addons/l10n_vn_edi_viettel_pos/models/pos_order.py`
- `addons/l10n_vn_edi_viettel_pos/models/pos_session.py`
- `addons/l10n_vn_edi_viettel_pos/models/res_company.py`
- `addons/l10n_vn_edi_viettel_pos/models/res_config_settings.py`
- `addons/l10n_vn_edi_viettel_pos/models/res_partner.py`
- `addons/l10n_vn_edi_viettel_pos/security/ir.access.csv`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/invoice_button/invoice_button.js`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/payment_screen/payment_screen.js`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/payment_screen/payment_screen.xml`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/models/pos_order.js`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/models/pos_store.js`
- `addons/l10n_vn_edi_viettel_pos/static/src/overrides/utils/order_payment_validation.js`
- `addons/l10n_vn_edi_viettel_pos/static/tests/tours/l10n_vn_edi_viettel_pos_tour.js`
- `addons/l10n_vn_edi_viettel_pos/tests/__init__.py`
- `addons/l10n_vn_edi_viettel_pos/tests/test_l10n_vn_edi_pos.py`
- `addons/l10n_vn_edi_viettel_pos/tests/test_l10n_vn_edi_pos_tour.py`
- `addons/l10n_vn_edi_viettel_pos/views/account_move_views.xml`
- `addons/l10n_vn_edi_viettel_pos/views/res_config_settings_views.xml`
