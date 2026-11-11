# Module: l10n_jo_edi_pos

- **Module ID:** MOD-247
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_jo_edi_pos`
- **Manifest:** `addons/l10n_jo_edi_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Jordan Accounting EDI for POS
=============================
Provides electronic invoicing for Jordan in the POS.

**Scope evidence:** The module contains 30 files, including 16 Python, 6 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_jo_edi`, `pos_edi_ubl`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 6
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 77 methods, 0 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/l10n_jo_edi_pos/models/res_config_settings.py:4`, `addons/l10n_jo_edi_pos/models/pos_edi_ubl_21_jo.py:20`, `addons/l10n_jo_edi_pos/models/pos_order.py:10`, `addons/l10n_jo_edi_pos/models/pos_payment_method.py:4`, `addons/l10n_jo_edi_pos/models/account_move.py:4`, `addons/l10n_jo_edi_pos/models/res_company.py:4`, `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 6 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/l10n_jo_edi_pos/demo/demo_company.xml:4`, `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.xml:11`, `addons/l10n_jo_edi_pos/views/pos_payment_method_views.xml:3`, `addons/l10n_jo_edi_pos/views/res_config_settings_views.xml:3`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:3`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:34`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/l10n_jo_edi_pos/tests/test_l10n_jo_edi_pos_tour.py`, `addons/l10n_jo_edi_pos/tests/test_jo_edi_pos_types.py`, `addons/l10n_jo_edi_pos/tests/test_jo_edi_pos_precision.py`, `addons/l10n_jo_edi_pos/tests/jo_edi_pos_common.py`, `addons/l10n_jo_edi_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `base.demo_company_jo`, `l10n_jo_edi_pos.pos_order_receipt_header`, `l10n_jo_edi_pos.pos_order_receipt_footer`, `pos_payment_method_view_form`, `res_config_settings_view_form`, `view_pos_pos_form`, `view_pos_order_tree`, `view_pos_order_filter`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.xml:11`
- View/action field declarations: 10; representative evidence: `addons/l10n_jo_edi_pos/views/pos_payment_method_views.xml:5`, `addons/l10n_jo_edi_pos/views/pos_payment_method_views.xml:7`, `addons/l10n_jo_edi_pos/views/res_config_settings_views.xml:5`, `addons/l10n_jo_edi_pos/views/res_config_settings_views.xml:7`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:5`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:7`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:35`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:37`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:48`, `addons/l10n_jo_edi_pos/views/pos_order_views.xml:50`
- Browser assets: 6; representative files: `addons/l10n_jo_edi_pos/static/src/overrides/models/invoice_button.js`, `addons/l10n_jo_edi_pos/static/src/overrides/models/pos_order.js`, `addons/l10n_jo_edi_pos/static/src/overrides/models/feedback_screen.js`, `addons/l10n_jo_edi_pos/static/src/overrides/screens/ticket_screen.js`, `addons/l10n_jo_edi_pos/static/src/overrides/app/utils/generate_printer_data.js`, `addons/l10n_jo_edi_pos/static/tests/tours/l10n_jo_edi_pos_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_jo_edi_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `res.config.settings` (addons/l10n_jo_edi_pos/models/res_config_settings.py:4); `pos.edi.xml.ubl_21.jo` (addons/l10n_jo_edi_pos/models/pos_edi_ubl_21_jo.py:20); inherits `pos.order` (addons/l10n_jo_edi_pos/models/pos_order.py:10); inherits `pos.payment.method` (addons/l10n_jo_edi_pos/models/pos_payment_method.py:4); inherits `account.move` (addons/l10n_jo_edi_pos/models/account_move.py:4); inherits `res.company` (addons/l10n_jo_edi_pos/models/res_company.py:4); inherits `pos.order.receipt` (addons/l10n_jo_edi_pos/receipt/pos_order_receipt.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_jo_edi`, `pos_edi_ubl`
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

- `addons/l10n_jo_edi_pos/__init__.py`
- `addons/l10n_jo_edi_pos/__manifest__.py`
- `addons/l10n_jo_edi_pos/demo/demo_company.xml`
- `addons/l10n_jo_edi_pos/i18n/ar.po`
- `addons/l10n_jo_edi_pos/i18n/l10n_jo_edi_pos.pot`
- `addons/l10n_jo_edi_pos/models/__init__.py`
- `addons/l10n_jo_edi_pos/models/account_move.py`
- `addons/l10n_jo_edi_pos/models/pos_edi_ubl_21_jo.py`
- `addons/l10n_jo_edi_pos/models/pos_order.py`
- `addons/l10n_jo_edi_pos/models/pos_payment_method.py`
- `addons/l10n_jo_edi_pos/models/res_company.py`
- `addons/l10n_jo_edi_pos/models/res_config_settings.py`
- `addons/l10n_jo_edi_pos/receipt/__init__.py`
- `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.py`
- `addons/l10n_jo_edi_pos/receipt/pos_order_receipt.xml`
- `addons/l10n_jo_edi_pos/static/src/overrides/app/utils/generate_printer_data.js`
- `addons/l10n_jo_edi_pos/static/src/overrides/models/feedback_screen.js`
- `addons/l10n_jo_edi_pos/static/src/overrides/models/invoice_button.js`
- `addons/l10n_jo_edi_pos/static/src/overrides/models/pos_order.js`
- `addons/l10n_jo_edi_pos/static/src/overrides/screens/ticket_screen.js`
- `addons/l10n_jo_edi_pos/static/src/overrides/screens/ticket_screen.xml`
- `addons/l10n_jo_edi_pos/static/tests/tours/l10n_jo_edi_pos_tour.js`
- `addons/l10n_jo_edi_pos/tests/__init__.py`
- `addons/l10n_jo_edi_pos/tests/jo_edi_pos_common.py`
- `addons/l10n_jo_edi_pos/tests/test_jo_edi_pos_precision.py`
- `addons/l10n_jo_edi_pos/tests/test_jo_edi_pos_types.py`
- `addons/l10n_jo_edi_pos/tests/test_l10n_jo_edi_pos_tour.py`
- `addons/l10n_jo_edi_pos/views/pos_order_views.xml`
- `addons/l10n_jo_edi_pos/views/pos_payment_method_views.xml`
- `addons/l10n_jo_edi_pos/views/res_config_settings_views.xml`
