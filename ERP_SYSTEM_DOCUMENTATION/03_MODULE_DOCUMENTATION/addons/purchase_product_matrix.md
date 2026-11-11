# Module: purchase_product_matrix

- **Module ID:** MOD-499
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_product_matrix`
- **Manifest:** `addons/purchase_product_matrix/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add variants to your purchase orders through an Order Grid Entry.

**Manifest description:**

This module allows to fill Purchase Orders rapidly
by choosing product variants quantity through a Grid Entry.

**Scope evidence:** The module contains 61 files, including 6 Python, 4 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `purchase`, `product_matrix`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 2
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 7 methods, 0 constraint handlers, 2 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/purchase_product_matrix/models/purchase.py:8`, `addons/purchase_product_matrix/models/purchase.py:157`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 2 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/purchase_product_matrix/report/purchase_quotation_templates.xml:3`, `addons/purchase_product_matrix/report/purchase_order_templates.xml:3`, `addons/purchase_product_matrix/views/purchase_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/purchase_product_matrix/tests/test_purchase_matrix.py`, `addons/purchase_product_matrix/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `grid_report_purchaseorder_template_inherit`, `grid_purchaseorder_inherit`, `purchase_order_form_matrix`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/purchase_product_matrix/report/purchase_quotation_templates.xml:3`, `addons/purchase_product_matrix/report/purchase_order_templates.xml:3`
- View/action field declarations: 2; representative evidence: `addons/purchase_product_matrix/views/purchase_views.xml:6`, `addons/purchase_product_matrix/views/purchase_views.xml:8`
- Browser assets: 2; representative files: `addons/purchase_product_matrix/static/src/js/purchase_product_field.js`, `addons/purchase_product_matrix/static/tests/tours/purchase_product_matrix_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_product_matrix/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `purchase.order` (addons/purchase_product_matrix/models/purchase.py:8); inherits `purchase.order.line` (addons/purchase_product_matrix/models/purchase.py:157)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase`, `product_matrix`
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

- `addons/purchase_product_matrix/__init__.py`
- `addons/purchase_product_matrix/__manifest__.py`
- `addons/purchase_product_matrix/i18n/ar.po`
- `addons/purchase_product_matrix/i18n/az.po`
- `addons/purchase_product_matrix/i18n/bg.po`
- `addons/purchase_product_matrix/i18n/bs.po`
- `addons/purchase_product_matrix/i18n/ca.po`
- `addons/purchase_product_matrix/i18n/cs.po`
- `addons/purchase_product_matrix/i18n/da.po`
- `addons/purchase_product_matrix/i18n/de.po`
- `addons/purchase_product_matrix/i18n/el.po`
- `addons/purchase_product_matrix/i18n/es.po`
- `addons/purchase_product_matrix/i18n/es_419.po`
- `addons/purchase_product_matrix/i18n/et.po`
- `addons/purchase_product_matrix/i18n/fa.po`
- `addons/purchase_product_matrix/i18n/fi.po`
- `addons/purchase_product_matrix/i18n/fr.po`
- `addons/purchase_product_matrix/i18n/he.po`
- `addons/purchase_product_matrix/i18n/hi.po`
- `addons/purchase_product_matrix/i18n/hr.po`
- `addons/purchase_product_matrix/i18n/hu.po`
- `addons/purchase_product_matrix/i18n/id.po`
- `addons/purchase_product_matrix/i18n/it.po`
- `addons/purchase_product_matrix/i18n/ja.po`
- `addons/purchase_product_matrix/i18n/kab.po`
- `addons/purchase_product_matrix/i18n/ko.po`
- `addons/purchase_product_matrix/i18n/ku.po`
- `addons/purchase_product_matrix/i18n/lo.po`
- `addons/purchase_product_matrix/i18n/lt.po`
- `addons/purchase_product_matrix/i18n/lv.po`
- `addons/purchase_product_matrix/i18n/mn.po`
- `addons/purchase_product_matrix/i18n/my.po`
- `addons/purchase_product_matrix/i18n/nb.po`
- `addons/purchase_product_matrix/i18n/nl.po`
- `addons/purchase_product_matrix/i18n/pl.po`
- `addons/purchase_product_matrix/i18n/pt.po`
- `addons/purchase_product_matrix/i18n/pt_BR.po`
- `addons/purchase_product_matrix/i18n/purchase_product_matrix.pot`
- `addons/purchase_product_matrix/i18n/ro.po`
- `addons/purchase_product_matrix/i18n/ru.po`
- `addons/purchase_product_matrix/i18n/sk.po`
- `addons/purchase_product_matrix/i18n/sl.po`
- `addons/purchase_product_matrix/i18n/sr@latin.po`
- `addons/purchase_product_matrix/i18n/sv.po`
- `addons/purchase_product_matrix/i18n/th.po`
- `addons/purchase_product_matrix/i18n/tr.po`
- `addons/purchase_product_matrix/i18n/uk.po`
- `addons/purchase_product_matrix/i18n/uz.po`
- `addons/purchase_product_matrix/i18n/vi.po`
- `addons/purchase_product_matrix/i18n/zh_CN.po`
- `addons/purchase_product_matrix/i18n/zh_TW.po`
- `addons/purchase_product_matrix/models/__init__.py`
- `addons/purchase_product_matrix/models/purchase.py`
- `addons/purchase_product_matrix/report/purchase_order_templates.xml`
- `addons/purchase_product_matrix/report/purchase_quotation_templates.xml`
- `addons/purchase_product_matrix/static/src/js/purchase_product_field.js`
- `addons/purchase_product_matrix/static/src/js/purchase_product_field.xml`
- `addons/purchase_product_matrix/static/tests/tours/purchase_product_matrix_tour.js`
- `addons/purchase_product_matrix/tests/__init__.py`
- `addons/purchase_product_matrix/tests/test_purchase_matrix.py`
- `addons/purchase_product_matrix/views/purchase_views.xml`
