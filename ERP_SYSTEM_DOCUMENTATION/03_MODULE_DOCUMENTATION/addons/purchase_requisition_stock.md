# Module: purchase_requisition_stock

- **Module ID:** MOD-502
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_requisition_stock`
- **Manifest:** `addons/purchase_requisition_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 60 files, including 8 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `purchase_requisition`, `purchase_stock`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase_requisition_stock/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 9 methods, 0 constraint handlers, 1 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/purchase_requisition_stock/models/purchase.py:6`, `addons/purchase_requisition_stock/models/stock.py:7`, `addons/purchase_requisition_stock/models/stock.py:35`, `addons/purchase_requisition_stock/models/purchase_requisition.py:7`, `addons/purchase_requisition_stock/models/purchase_requisition.py:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/purchase_requisition_stock/views/purchase_requisition_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/purchase_requisition_stock/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/purchase_requisition_stock/tests/test_purchase_requisition_stock.py`, `addons/purchase_requisition_stock/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `view_purchase_requisition_form_inherit`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/purchase_requisition_stock/views/purchase_requisition_views.xml:6`, `addons/purchase_requisition_stock/views/purchase_requisition_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_requisition_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `purchase.order` (addons/purchase_requisition_stock/models/purchase.py:6); inherits `stock.rule` (addons/purchase_requisition_stock/models/stock.py:7); inherits `stock.move` (addons/purchase_requisition_stock/models/stock.py:35); inherits `purchase.requisition` (addons/purchase_requisition_stock/models/purchase_requisition.py:7); inherits `purchase.requisition.line` (addons/purchase_requisition_stock/models/purchase_requisition.py:22)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase_requisition`, `purchase_stock`
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

- `addons/purchase_requisition_stock/__init__.py`
- `addons/purchase_requisition_stock/__manifest__.py`
- `addons/purchase_requisition_stock/data/purchase_requisition_stock_data.xml`
- `addons/purchase_requisition_stock/i18n/ar.po`
- `addons/purchase_requisition_stock/i18n/az.po`
- `addons/purchase_requisition_stock/i18n/bg.po`
- `addons/purchase_requisition_stock/i18n/bs.po`
- `addons/purchase_requisition_stock/i18n/ca.po`
- `addons/purchase_requisition_stock/i18n/cs.po`
- `addons/purchase_requisition_stock/i18n/da.po`
- `addons/purchase_requisition_stock/i18n/de.po`
- `addons/purchase_requisition_stock/i18n/el.po`
- `addons/purchase_requisition_stock/i18n/es.po`
- `addons/purchase_requisition_stock/i18n/es_419.po`
- `addons/purchase_requisition_stock/i18n/et.po`
- `addons/purchase_requisition_stock/i18n/fa.po`
- `addons/purchase_requisition_stock/i18n/fi.po`
- `addons/purchase_requisition_stock/i18n/fr.po`
- `addons/purchase_requisition_stock/i18n/he.po`
- `addons/purchase_requisition_stock/i18n/hi.po`
- `addons/purchase_requisition_stock/i18n/hr.po`
- `addons/purchase_requisition_stock/i18n/hu.po`
- `addons/purchase_requisition_stock/i18n/id.po`
- `addons/purchase_requisition_stock/i18n/it.po`
- `addons/purchase_requisition_stock/i18n/ja.po`
- `addons/purchase_requisition_stock/i18n/kab.po`
- `addons/purchase_requisition_stock/i18n/ko.po`
- `addons/purchase_requisition_stock/i18n/ku.po`
- `addons/purchase_requisition_stock/i18n/lo.po`
- `addons/purchase_requisition_stock/i18n/lt.po`
- `addons/purchase_requisition_stock/i18n/lv.po`
- `addons/purchase_requisition_stock/i18n/mn.po`
- `addons/purchase_requisition_stock/i18n/my.po`
- `addons/purchase_requisition_stock/i18n/nb.po`
- `addons/purchase_requisition_stock/i18n/nl.po`
- `addons/purchase_requisition_stock/i18n/pl.po`
- `addons/purchase_requisition_stock/i18n/pt.po`
- `addons/purchase_requisition_stock/i18n/pt_BR.po`
- `addons/purchase_requisition_stock/i18n/purchase_requisition_stock.pot`
- `addons/purchase_requisition_stock/i18n/ro.po`
- `addons/purchase_requisition_stock/i18n/ru.po`
- `addons/purchase_requisition_stock/i18n/sk.po`
- `addons/purchase_requisition_stock/i18n/sl.po`
- `addons/purchase_requisition_stock/i18n/sr@latin.po`
- `addons/purchase_requisition_stock/i18n/sv.po`
- `addons/purchase_requisition_stock/i18n/th.po`
- `addons/purchase_requisition_stock/i18n/tr.po`
- `addons/purchase_requisition_stock/i18n/uk.po`
- `addons/purchase_requisition_stock/i18n/uz.po`
- `addons/purchase_requisition_stock/i18n/vi.po`
- `addons/purchase_requisition_stock/i18n/zh_CN.po`
- `addons/purchase_requisition_stock/i18n/zh_TW.po`
- `addons/purchase_requisition_stock/models/__init__.py`
- `addons/purchase_requisition_stock/models/purchase.py`
- `addons/purchase_requisition_stock/models/purchase_requisition.py`
- `addons/purchase_requisition_stock/models/stock.py`
- `addons/purchase_requisition_stock/security/ir.access.csv`
- `addons/purchase_requisition_stock/tests/__init__.py`
- `addons/purchase_requisition_stock/tests/test_purchase_requisition_stock.py`
- `addons/purchase_requisition_stock/views/purchase_requisition_views.xml`
