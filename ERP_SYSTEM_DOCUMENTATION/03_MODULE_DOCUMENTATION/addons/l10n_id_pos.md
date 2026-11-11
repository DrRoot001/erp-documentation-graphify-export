# Module: l10n_id_pos

- **Module ID:** MOD-223
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_id_pos`
- **Manifest:** `addons/l10n_id_pos/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Indonesian Point of Sale

**Scope evidence:** The module contains 14 files, including 8 Python, 0 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_id`, `point_of_sale`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 4
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_id_pos/models/pos_order.py:5`, `addons/l10n_id_pos/models/pos_payment_method.py:6`, `addons/l10n_id_pos/models/qris_transaction.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 0 XML files and 4 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_id_pos/tests/test_qris_pos.py`, `addons/l10n_id_pos/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 4; representative files: `addons/l10n_id_pos/static/tests/test_pos_qris_payment.tour.js`, `addons/l10n_id_pos/static/src/app/services/pos_store.js`, `addons/l10n_id_pos/static/src/app/models/pos_payment.js`, `addons/l10n_id_pos/static/src/app/components/popups/qr_code_popup.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_id_pos/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `pos.order` (addons/l10n_id_pos/models/pos_order.py:5); inherits `pos.payment.method` (addons/l10n_id_pos/models/pos_payment_method.py:6); inherits `l10n_id.qris.transaction` (addons/l10n_id_pos/models/qris_transaction.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_id`, `point_of_sale`
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

- `addons/l10n_id_pos/__init__.py`
- `addons/l10n_id_pos/__manifest__.py`
- `addons/l10n_id_pos/i18n/id.po`
- `addons/l10n_id_pos/i18n/l10n_id_pos.pot`
- `addons/l10n_id_pos/models/__init__.py`
- `addons/l10n_id_pos/models/pos_order.py`
- `addons/l10n_id_pos/models/pos_payment_method.py`
- `addons/l10n_id_pos/models/qris_transaction.py`
- `addons/l10n_id_pos/static/src/app/components/popups/qr_code_popup.js`
- `addons/l10n_id_pos/static/src/app/models/pos_payment.js`
- `addons/l10n_id_pos/static/src/app/services/pos_store.js`
- `addons/l10n_id_pos/static/tests/test_pos_qris_payment.tour.js`
- `addons/l10n_id_pos/tests/__init__.py`
- `addons/l10n_id_pos/tests/test_qris_pos.py`
