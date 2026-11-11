# Module: l10n_test_pos_qr_payment

- **Module ID:** MOD-322
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_test_pos_qr_payment`
- **Manifest:** `addons/l10n_test_pos_qr_payment/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module contains tests related to point of sale QR code payment.
        It tests all the supported qr codes: SEPA, Swiss QR and EMV QR (using the hk and br implementation)

**Scope evidence:** The module contains 9 files, including 5 Python, 0 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `point_of_sale`, `account_qr_code_sepa`, `l10n_be`, `l10n_ch`, `l10n_hk`, `l10n_br`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 4
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### User interface and data

- **Description:** 0 XML files and 4 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_test_pos_qr_payment/tests/common.py`, `addons/l10n_test_pos_qr_payment/tests/__init__.py`, `addons/l10n_test_pos_qr_payment/tests/test_pos_qr_payment.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 4; representative files: `addons/l10n_test_pos_qr_payment/static/tests/tours/test_pos_payment_tour.js`, `addons/l10n_test_pos_qr_payment/static/tests/unit/service/pos_store.test.js`, `addons/l10n_test_pos_qr_payment/static/tests/unit/data/pos_config.data.js`, `addons/l10n_test_pos_qr_payment/static/tests/unit/data/pos_payment_method.data.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_test_pos_qr_payment/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `point_of_sale`, `account_qr_code_sepa`, `l10n_be`, `l10n_ch`, `l10n_hk`, `l10n_br`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_test_pos_qr_payment/__init__.py`
- `addons/l10n_test_pos_qr_payment/__manifest__.py`
- `addons/l10n_test_pos_qr_payment/static/tests/tours/test_pos_payment_tour.js`
- `addons/l10n_test_pos_qr_payment/static/tests/unit/data/pos_config.data.js`
- `addons/l10n_test_pos_qr_payment/static/tests/unit/data/pos_payment_method.data.js`
- `addons/l10n_test_pos_qr_payment/static/tests/unit/service/pos_store.test.js`
- `addons/l10n_test_pos_qr_payment/tests/__init__.py`
- `addons/l10n_test_pos_qr_payment/tests/common.py`
- `addons/l10n_test_pos_qr_payment/tests/test_pos_qr_payment.py`
