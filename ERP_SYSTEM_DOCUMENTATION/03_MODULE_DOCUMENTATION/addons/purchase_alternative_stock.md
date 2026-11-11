# Module: purchase_alternative_stock

- **Module ID:** MOD-496
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_alternative_stock`
- **Manifest:** `addons/purchase_alternative_stock/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 58 files, including 8 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `purchase_alternative`, `purchase_stock`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 1
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

- **Description:** 3 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/purchase_alternative_stock/models/purchase.py:6`, `addons/purchase_alternative_stock/models/purchase.py:20`, `addons/purchase_alternative_stock/wizard/purchase_alternative_create.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/purchase_alternative_stock/views/purchase_views.xml:3`, `addons/purchase_alternative_stock/views/purchase_views.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/purchase_alternative_stock/tests/__init__.py`, `addons/purchase_alternative_stock/tests/test_purchase_alternative_stock.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `purchase_order_form`, `purchase_order_line_view_compare_list`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/purchase_alternative_stock/views/purchase_views.xml:5`, `addons/purchase_alternative_stock/views/purchase_views.xml:7`, `addons/purchase_alternative_stock/views/purchase_views.xml:16`, `addons/purchase_alternative_stock/views/purchase_views.xml:18`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_alternative_stock/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `purchase.order` (addons/purchase_alternative_stock/models/purchase.py:6); inherits `purchase.order.line` (addons/purchase_alternative_stock/models/purchase.py:20); inherits `purchase.alternative.create` (addons/purchase_alternative_stock/wizard/purchase_alternative_create.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase_alternative`, `purchase_stock`
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

- `addons/purchase_alternative_stock/__init__.py`
- `addons/purchase_alternative_stock/__manifest__.py`
- `addons/purchase_alternative_stock/i18n/ar.po`
- `addons/purchase_alternative_stock/i18n/az.po`
- `addons/purchase_alternative_stock/i18n/bg.po`
- `addons/purchase_alternative_stock/i18n/bs.po`
- `addons/purchase_alternative_stock/i18n/ca.po`
- `addons/purchase_alternative_stock/i18n/cs.po`
- `addons/purchase_alternative_stock/i18n/da.po`
- `addons/purchase_alternative_stock/i18n/de.po`
- `addons/purchase_alternative_stock/i18n/el.po`
- `addons/purchase_alternative_stock/i18n/es.po`
- `addons/purchase_alternative_stock/i18n/es_419.po`
- `addons/purchase_alternative_stock/i18n/et.po`
- `addons/purchase_alternative_stock/i18n/fa.po`
- `addons/purchase_alternative_stock/i18n/fi.po`
- `addons/purchase_alternative_stock/i18n/fr.po`
- `addons/purchase_alternative_stock/i18n/he.po`
- `addons/purchase_alternative_stock/i18n/hi.po`
- `addons/purchase_alternative_stock/i18n/hr.po`
- `addons/purchase_alternative_stock/i18n/hu.po`
- `addons/purchase_alternative_stock/i18n/id.po`
- `addons/purchase_alternative_stock/i18n/it.po`
- `addons/purchase_alternative_stock/i18n/ja.po`
- `addons/purchase_alternative_stock/i18n/kab.po`
- `addons/purchase_alternative_stock/i18n/ko.po`
- `addons/purchase_alternative_stock/i18n/ku.po`
- `addons/purchase_alternative_stock/i18n/lo.po`
- `addons/purchase_alternative_stock/i18n/lt.po`
- `addons/purchase_alternative_stock/i18n/lv.po`
- `addons/purchase_alternative_stock/i18n/mn.po`
- `addons/purchase_alternative_stock/i18n/my.po`
- `addons/purchase_alternative_stock/i18n/nb.po`
- `addons/purchase_alternative_stock/i18n/nl.po`
- `addons/purchase_alternative_stock/i18n/pl.po`
- `addons/purchase_alternative_stock/i18n/pt.po`
- `addons/purchase_alternative_stock/i18n/pt_BR.po`
- `addons/purchase_alternative_stock/i18n/purchase_alternative_stock.pot`
- `addons/purchase_alternative_stock/i18n/ro.po`
- `addons/purchase_alternative_stock/i18n/ru.po`
- `addons/purchase_alternative_stock/i18n/sk.po`
- `addons/purchase_alternative_stock/i18n/sl.po`
- `addons/purchase_alternative_stock/i18n/sr@latin.po`
- `addons/purchase_alternative_stock/i18n/sv.po`
- `addons/purchase_alternative_stock/i18n/th.po`
- `addons/purchase_alternative_stock/i18n/tr.po`
- `addons/purchase_alternative_stock/i18n/uk.po`
- `addons/purchase_alternative_stock/i18n/uz.po`
- `addons/purchase_alternative_stock/i18n/vi.po`
- `addons/purchase_alternative_stock/i18n/zh_CN.po`
- `addons/purchase_alternative_stock/i18n/zh_TW.po`
- `addons/purchase_alternative_stock/models/__init__.py`
- `addons/purchase_alternative_stock/models/purchase.py`
- `addons/purchase_alternative_stock/tests/__init__.py`
- `addons/purchase_alternative_stock/tests/test_purchase_alternative_stock.py`
- `addons/purchase_alternative_stock/views/purchase_views.xml`
- `addons/purchase_alternative_stock/wizard/__init__.py`
- `addons/purchase_alternative_stock/wizard/purchase_alternative_create.py`
