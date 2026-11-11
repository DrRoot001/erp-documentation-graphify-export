# Module: l10n_ph_sale

- **Module ID:** MOD-294
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_ph_sale`
- **Manifest:** `addons/l10n_ph_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Apply Philippine SC/PWD discount privileges on quotations and sale orders.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 14 files, including 10 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_ph_invoice`, `sale`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/l10n_ph_sale/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 33 methods, 0 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/l10n_ph_sale/models/sale_order.py:6`, `addons/l10n_ph_sale/models/sale_order_line.py:7`, `addons/l10n_ph_sale/wizard/l10n_ph_discount_privilege_wizard.py:8`, `addons/l10n_ph_sale/wizard/l10n_ph_discount_privilege_wizard.py:59`, `addons/l10n_ph_sale/wizard/sale_order_discount.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/l10n_ph_sale/views/sale_order_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/l10n_ph_sale/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_ph_sale/tests/test_discount_privilege_wizard.py`, `addons/l10n_ph_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_order_form_l10n_ph_discount_privilege`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_ph_sale/views/sale_order_views.xml:5`, `addons/l10n_ph_sale/views/sale_order_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_ph_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `sale.order` (addons/l10n_ph_sale/models/sale_order.py:6); `sale.order.line` (addons/l10n_ph_sale/models/sale_order_line.py:7); inherits `l10n_ph.discount.privilege.wizard` (addons/l10n_ph_sale/wizard/l10n_ph_discount_privilege_wizard.py:8); inherits `l10n_ph.discount.privilege.wizard.line` (addons/l10n_ph_sale/wizard/l10n_ph_discount_privilege_wizard.py:59); inherits `sale.order.discount` (addons/l10n_ph_sale/wizard/sale_order_discount.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_ph_invoice`, `sale`
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

- `addons/l10n_ph_sale/__init__.py`
- `addons/l10n_ph_sale/__manifest__.py`
- `addons/l10n_ph_sale/i18n/l10n_ph_sale.pot`
- `addons/l10n_ph_sale/i18n/tl.po`
- `addons/l10n_ph_sale/models/__init__.py`
- `addons/l10n_ph_sale/models/sale_order.py`
- `addons/l10n_ph_sale/models/sale_order_line.py`
- `addons/l10n_ph_sale/security/ir.access.csv`
- `addons/l10n_ph_sale/tests/__init__.py`
- `addons/l10n_ph_sale/tests/test_discount_privilege_wizard.py`
- `addons/l10n_ph_sale/views/sale_order_views.xml`
- `addons/l10n_ph_sale/wizard/__init__.py`
- `addons/l10n_ph_sale/wizard/l10n_ph_discount_privilege_wizard.py`
- `addons/l10n_ph_sale/wizard/sale_order_discount.py`
