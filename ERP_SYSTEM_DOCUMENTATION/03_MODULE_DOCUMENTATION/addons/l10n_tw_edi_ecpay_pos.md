# Module: l10n_tw_edi_ecpay_pos

- **Module ID:** MOD-329
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_tw_edi_ecpay_pos`
- **Manifest:** `addons/l10n_tw_edi_ecpay_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Point of sale/Localizations/EDI`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** ECpay E-invoice bridge module for POS

**Manifest description:**

This bridge module allows the user to input Ecpay information in pos for sending their invoices to the Ecpay system

**Scope evidence:** The module contains 31 files, including 13 Python, 6 XML, and 10 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `l10n_tw_edi_ecpay`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 10
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 31 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/l10n_tw_edi_ecpay_pos/models/ir_ui_view.py:4`, `addons/l10n_tw_edi_ecpay_pos/models/pos_config.py:6`, `addons/l10n_tw_edi_ecpay_pos/models/pos_session.py:9`, `addons/l10n_tw_edi_ecpay_pos/models/account_tax.py:6`, `addons/l10n_tw_edi_ecpay_pos/models/pos_order.py:14`, `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 10 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/l10n_tw_edi_ecpay_pos/data/res_partner_data.xml:7`, `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.xml:13`, `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_certificate_receipt.xml:4`, `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_transaction_receipt.xml:4`, `addons/l10n_tw_edi_ecpay_pos/views/pos_order_view.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_tw_edi_ecpay_pos/tests/test_edi_pos_order.py`, `addons/l10n_tw_edi_ecpay_pos/tests/test_edi_pos_order_ui.py`, `addons/l10n_tw_edi_ecpay_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `ecpay_default_walk_in_customer`, `l10n_tw_edi_ecpay_pos.pos_order_receipt_header`, `l10n_tw_edi_ecpay_pos.pos_order_receipt_style`, `l10n_tw_edi_ecpay_pos.ecpay_certificate_receipt`, `l10n_tw_edi_ecpay_pos.ecpay_transaction_receipt`, `view_pos_order_form_inherit_ecpay`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.xml:13`, `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_certificate_receipt.xml:4`, `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_transaction_receipt.xml:4`
- View/action field declarations: 2; representative evidence: `addons/l10n_tw_edi_ecpay_pos/views/pos_order_view.xml:6`, `addons/l10n_tw_edi_ecpay_pos/views/pos_order_view.xml:8`
- Browser assets: 10; representative files: `addons/l10n_tw_edi_ecpay_pos/static/src/app/services/pos_store.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/models/pos_order.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/plugins/pos_ticket_printer_plugin.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/ticket_screen/ticket_screen.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/payment_screen/payment_screen.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/ticket_screen/invoice_button/invoice_button.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/components/popups/ecpay_info_popup.js`, `addons/l10n_tw_edi_ecpay_pos/static/src/app/utils/printer/generate_printer_data.js`, `addons/l10n_tw_edi_ecpay_pos/static/tests/unit/ecpay_info_popup.test.js`, `addons/l10n_tw_edi_ecpay_pos/static/tests/tours/ecpay_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_tw_edi_ecpay_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: `ir.ui.view` (addons/l10n_tw_edi_ecpay_pos/models/ir_ui_view.py:4); inherits `pos.config` (addons/l10n_tw_edi_ecpay_pos/models/pos_config.py:6); inherits `pos.session` (addons/l10n_tw_edi_ecpay_pos/models/pos_session.py:9); inherits `account.tax` (addons/l10n_tw_edi_ecpay_pos/models/account_tax.py:6); inherits `pos.order` (addons/l10n_tw_edi_ecpay_pos/models/pos_order.py:14); inherits `pos.order.receipt` (addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `l10n_tw_edi_ecpay`
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

- `addons/l10n_tw_edi_ecpay_pos/__init__.py`
- `addons/l10n_tw_edi_ecpay_pos/__manifest__.py`
- `addons/l10n_tw_edi_ecpay_pos/data/res_partner_data.xml`
- `addons/l10n_tw_edi_ecpay_pos/i18n/l10n_tw_edi_ecpay_pos.pot`
- `addons/l10n_tw_edi_ecpay_pos/i18n/zh_TW.po`
- `addons/l10n_tw_edi_ecpay_pos/models/__init__.py`
- `addons/l10n_tw_edi_ecpay_pos/models/account_tax.py`
- `addons/l10n_tw_edi_ecpay_pos/models/ir_ui_view.py`
- `addons/l10n_tw_edi_ecpay_pos/models/pos_config.py`
- `addons/l10n_tw_edi_ecpay_pos/models/pos_order.py`
- `addons/l10n_tw_edi_ecpay_pos/models/pos_session.py`
- `addons/l10n_tw_edi_ecpay_pos/receipt/__init__.py`
- `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_certificate_receipt.xml`
- `addons/l10n_tw_edi_ecpay_pos/receipt/ecpay_transaction_receipt.xml`
- `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.py`
- `addons/l10n_tw_edi_ecpay_pos/receipt/pos_order_receipt.xml`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/components/popups/ecpay_info_popup.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/components/popups/ecpay_info_popup.xml`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/models/pos_order.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/plugins/pos_ticket_printer_plugin.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/payment_screen/payment_screen.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/ticket_screen/invoice_button/invoice_button.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/screens/ticket_screen/ticket_screen.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/services/pos_store.js`
- `addons/l10n_tw_edi_ecpay_pos/static/src/app/utils/printer/generate_printer_data.js`
- `addons/l10n_tw_edi_ecpay_pos/static/tests/tours/ecpay_tour.js`
- `addons/l10n_tw_edi_ecpay_pos/static/tests/unit/ecpay_info_popup.test.js`
- `addons/l10n_tw_edi_ecpay_pos/tests/__init__.py`
- `addons/l10n_tw_edi_ecpay_pos/tests/test_edi_pos_order.py`
- `addons/l10n_tw_edi_ecpay_pos/tests/test_edi_pos_order_ui.py`
- `addons/l10n_tw_edi_ecpay_pos/views/pos_order_view.xml`
