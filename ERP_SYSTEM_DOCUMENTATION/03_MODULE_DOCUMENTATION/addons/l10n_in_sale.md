# Module: l10n_in_sale

- **Module ID:** MOD-236
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_in_sale`
- **Manifest:** `addons/l10n_in_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

GST Sale Report

**Scope evidence:** The module contains 14 files, including 10 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_in`, `sale`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 12 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_in_sale/models/sale_order.py:7`, `addons/l10n_in_sale/models/sale_order_line.py:6`, `addons/l10n_in_sale/wizard/sale_make_invoice_advance.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_in_sale/data/product_demo.xml:3`, `addons/l10n_in_sale/views/sale_order_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_in_sale/tests/test_l10n_in_sale_fiscal_position.py`, `addons/l10n_in_sale/tests/test_l10n_in_sale_qty_invoiced.py`, `addons/l10n_in_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `sale.advance_product_0`, `view_order_form_inherit_l10n_in_sale`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_in_sale/views/sale_order_views.xml:6`, `addons/l10n_in_sale/views/sale_order_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_in_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `sale.order` (addons/l10n_in_sale/models/sale_order.py:7); inherits `sale.order.line` (addons/l10n_in_sale/models/sale_order_line.py:6); inherits `sale.advance.payment.inv` (addons/l10n_in_sale/wizard/sale_make_invoice_advance.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_in`, `sale`
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

- `addons/l10n_in_sale/__init__.py`
- `addons/l10n_in_sale/__manifest__.py`
- `addons/l10n_in_sale/data/product_demo.xml`
- `addons/l10n_in_sale/i18n/hi.po`
- `addons/l10n_in_sale/i18n/l10n_in_sale.pot`
- `addons/l10n_in_sale/models/__init__.py`
- `addons/l10n_in_sale/models/sale_order.py`
- `addons/l10n_in_sale/models/sale_order_line.py`
- `addons/l10n_in_sale/tests/__init__.py`
- `addons/l10n_in_sale/tests/test_l10n_in_sale_fiscal_position.py`
- `addons/l10n_in_sale/tests/test_l10n_in_sale_qty_invoiced.py`
- `addons/l10n_in_sale/views/sale_order_views.xml`
- `addons/l10n_in_sale/wizard/__init__.py`
- `addons/l10n_in_sale/wizard/sale_make_invoice_advance.py`
