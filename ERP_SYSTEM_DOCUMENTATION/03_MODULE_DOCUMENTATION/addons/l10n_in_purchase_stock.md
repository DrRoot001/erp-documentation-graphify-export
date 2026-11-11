# Module: l10n_in_purchase_stock

- **Module ID:** MOD-235
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_purchase_stock`
- **Manifest:** `addons/l10n_in_purchase_stock/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Get warehouse address if the bill is created from Purchase Order

**Manifest description:**

Get the warehouse address if the bill is created from the Purchase Order

So this module is to get the warehouse address if the bill is created from Purchase Order

**Scope evidence:** The module contains 10 files, including 8 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in_stock`, `purchase_stock`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_in_purchase_stock/models/stock_move.py:6`, `addons/l10n_in_purchase_stock/models/stock_picking.py:6`, `addons/l10n_in_purchase_stock/models/account_move.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_in_purchase_stock/tests/test_purchase_stock_fiscal_position.py`, `addons/l10n_in_purchase_stock/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_purchase_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `stock.move` (addons/l10n_in_purchase_stock/models/stock_move.py:6); inherits `stock.picking` (addons/l10n_in_purchase_stock/models/stock_picking.py:6); inherits `account.move` (addons/l10n_in_purchase_stock/models/account_move.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in_stock`, `purchase_stock`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_in_purchase_stock/__init__.py`
- `addons/l10n_in_purchase_stock/__manifest__.py`
- `addons/l10n_in_purchase_stock/i18n/hi.po`
- `addons/l10n_in_purchase_stock/i18n/l10n_in_purchase_stock.pot`
- `addons/l10n_in_purchase_stock/models/__init__.py`
- `addons/l10n_in_purchase_stock/models/account_move.py`
- `addons/l10n_in_purchase_stock/models/stock_move.py`
- `addons/l10n_in_purchase_stock/models/stock_picking.py`
- `addons/l10n_in_purchase_stock/tests/__init__.py`
- `addons/l10n_in_purchase_stock/tests/test_purchase_stock_fiscal_position.py`
