# Module: l10n_sa_pos

- **Module ID:** MOD-313
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_sa_pos`
- **Manifest:** `addons/l10n_sa_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Saudi Arabia POS Localization
===========================================================

**Scope evidence:** The module contains 21 files, including 10 Python, 2 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_gcc_pos`, `l10n_sa`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 7
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 15 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_sa_pos/models/pos_config.py:8`, `addons/l10n_sa_pos/models/pos_order.py:7`, `addons/l10n_sa_pos/receipt/pos_order_receipt.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 7 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_sa_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_sa_pos/receipt/pos_order_receipt.xml:20`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_sa_pos/tests/test_sa_pos.py`, `addons/l10n_sa_pos/tests/__init__.py`, `addons/l10n_sa_pos/tests/test_order_receipt.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `l10n_sa_pos.pos_order_receipt_header`, `l10n_sa_pos.pos_order_receipt`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/l10n_sa_pos/receipt/pos_order_receipt.xml:4`, `addons/l10n_sa_pos/receipt/pos_order_receipt.xml:20`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 7; representative files: `addons/l10n_sa_pos/static/src/overrides/models/pos_order.js`, `addons/l10n_sa_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`, `addons/l10n_sa_pos/static/src/app/utils/qr.js`, `addons/l10n_sa_pos/static/src/app/add_zatca_refund_reason_popup/add_zatca_refund_reason_popup.js`, `addons/l10n_sa_pos/static/src/app/utils/printer/generate_printer_data.js`, `addons/l10n_sa_pos/static/tests/unit/sa_pos_unit.test.js`, `addons/l10n_sa_pos/static/tests/tours/sa_pos_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_sa_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `pos.config` (addons/l10n_sa_pos/models/pos_config.py:8); `pos.order` (addons/l10n_sa_pos/models/pos_order.py:7); inherits `pos.order.receipt` (addons/l10n_sa_pos/receipt/pos_order_receipt.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_gcc_pos`, `l10n_sa`
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

- `addons/l10n_sa_pos/__init__.py`
- `addons/l10n_sa_pos/__manifest__.py`
- `addons/l10n_sa_pos/i18n/ar.po`
- `addons/l10n_sa_pos/i18n/l10n_sa_pos.pot`
- `addons/l10n_sa_pos/models/__init__.py`
- `addons/l10n_sa_pos/models/pos_config.py`
- `addons/l10n_sa_pos/models/pos_order.py`
- `addons/l10n_sa_pos/receipt/__init__.py`
- `addons/l10n_sa_pos/receipt/pos_order_receipt.py`
- `addons/l10n_sa_pos/receipt/pos_order_receipt.xml`
- `addons/l10n_sa_pos/static/src/app/add_zatca_refund_reason_popup/add_zatca_refund_reason_popup.js`
- `addons/l10n_sa_pos/static/src/app/add_zatca_refund_reason_popup/add_zatca_refund_reason_popup.xml`
- `addons/l10n_sa_pos/static/src/app/utils/printer/generate_printer_data.js`
- `addons/l10n_sa_pos/static/src/app/utils/qr.js`
- `addons/l10n_sa_pos/static/src/overrides/components/ticket_screen/ticket_screen.js`
- `addons/l10n_sa_pos/static/src/overrides/models/pos_order.js`
- `addons/l10n_sa_pos/static/tests/tours/sa_pos_tour.js`
- `addons/l10n_sa_pos/static/tests/unit/sa_pos_unit.test.js`
- `addons/l10n_sa_pos/tests/__init__.py`
- `addons/l10n_sa_pos/tests/test_order_receipt.py`
- `addons/l10n_sa_pos/tests/test_sa_pos.py`
