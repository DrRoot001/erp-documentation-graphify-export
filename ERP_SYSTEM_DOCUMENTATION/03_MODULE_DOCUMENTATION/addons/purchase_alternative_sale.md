# Module: purchase_alternative_sale

- **Module ID:** MOD-495
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_alternative_sale`
- **Manifest:** `addons/purchase_alternative_sale/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Bridge module for Purchase Alternative and Sales.

**Scope evidence:** The module contains 55 files, including 6 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `purchase_alternative`, `sale_purchase`.

## 2. Module structure

- Model/business logic files: 1
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

- **Description:** 1 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/purchase_alternative_sale/wizard/purchase_alternative_create.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/purchase_alternative_sale/tests/test_purchase_alternative_sale.py`, `addons/purchase_alternative_sale/tests/__init__.py`
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

- **Entry point evidence:** `addons/purchase_alternative_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `purchase.alternative.create` (addons/purchase_alternative_sale/wizard/purchase_alternative_create.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase_alternative`, `sale_purchase`
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

- `addons/purchase_alternative_sale/__init__.py`
- `addons/purchase_alternative_sale/__manifest__.py`
- `addons/purchase_alternative_sale/i18n/ar.po`
- `addons/purchase_alternative_sale/i18n/az.po`
- `addons/purchase_alternative_sale/i18n/bg.po`
- `addons/purchase_alternative_sale/i18n/bs.po`
- `addons/purchase_alternative_sale/i18n/ca.po`
- `addons/purchase_alternative_sale/i18n/cs.po`
- `addons/purchase_alternative_sale/i18n/da.po`
- `addons/purchase_alternative_sale/i18n/de.po`
- `addons/purchase_alternative_sale/i18n/el.po`
- `addons/purchase_alternative_sale/i18n/es.po`
- `addons/purchase_alternative_sale/i18n/es_419.po`
- `addons/purchase_alternative_sale/i18n/et.po`
- `addons/purchase_alternative_sale/i18n/fa.po`
- `addons/purchase_alternative_sale/i18n/fi.po`
- `addons/purchase_alternative_sale/i18n/fr.po`
- `addons/purchase_alternative_sale/i18n/he.po`
- `addons/purchase_alternative_sale/i18n/hi.po`
- `addons/purchase_alternative_sale/i18n/hr.po`
- `addons/purchase_alternative_sale/i18n/hu.po`
- `addons/purchase_alternative_sale/i18n/id.po`
- `addons/purchase_alternative_sale/i18n/it.po`
- `addons/purchase_alternative_sale/i18n/ja.po`
- `addons/purchase_alternative_sale/i18n/kab.po`
- `addons/purchase_alternative_sale/i18n/ko.po`
- `addons/purchase_alternative_sale/i18n/ku.po`
- `addons/purchase_alternative_sale/i18n/lo.po`
- `addons/purchase_alternative_sale/i18n/lt.po`
- `addons/purchase_alternative_sale/i18n/lv.po`
- `addons/purchase_alternative_sale/i18n/mn.po`
- `addons/purchase_alternative_sale/i18n/my.po`
- `addons/purchase_alternative_sale/i18n/nb.po`
- `addons/purchase_alternative_sale/i18n/nl.po`
- `addons/purchase_alternative_sale/i18n/pl.po`
- `addons/purchase_alternative_sale/i18n/pt.po`
- `addons/purchase_alternative_sale/i18n/pt_BR.po`
- `addons/purchase_alternative_sale/i18n/purchase_alternative_sale.pot`
- `addons/purchase_alternative_sale/i18n/ro.po`
- `addons/purchase_alternative_sale/i18n/ru.po`
- `addons/purchase_alternative_sale/i18n/sk.po`
- `addons/purchase_alternative_sale/i18n/sl.po`
- `addons/purchase_alternative_sale/i18n/sr@latin.po`
- `addons/purchase_alternative_sale/i18n/sv.po`
- `addons/purchase_alternative_sale/i18n/th.po`
- `addons/purchase_alternative_sale/i18n/tr.po`
- `addons/purchase_alternative_sale/i18n/uk.po`
- `addons/purchase_alternative_sale/i18n/uz.po`
- `addons/purchase_alternative_sale/i18n/vi.po`
- `addons/purchase_alternative_sale/i18n/zh_CN.po`
- `addons/purchase_alternative_sale/i18n/zh_TW.po`
- `addons/purchase_alternative_sale/tests/__init__.py`
- `addons/purchase_alternative_sale/tests/test_purchase_alternative_sale.py`
- `addons/purchase_alternative_sale/wizard/__init__.py`
- `addons/purchase_alternative_sale/wizard/purchase_alternative_create.py`
