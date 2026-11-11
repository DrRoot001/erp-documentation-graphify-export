# Module: sale_product_matrix

- **Module ID:** MOD-523
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_product_matrix`
- **Manifest:** `addons/sale_product_matrix/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add variants to Sales Order through a grid entry.

**Manifest description:**

This module allows to fill Sales Order rapidly
by choosing product variants quantity through a Grid Entry.

**Scope evidence:** The module contains 60 files, including 6 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `product_matrix`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 1
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 2 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/sale_product_matrix/models/sale_order.py:9`, `addons/sale_product_matrix/models/product_template.py:6`, `addons/sale_product_matrix/models/sale_order_line.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 5 record/template/menu identifiers.
- **Evidence:** `addons/sale_product_matrix/report/sale_report_templates.xml:3`, `addons/sale_product_matrix/data/product_matrix_demo.xml:3`, `addons/sale_product_matrix/views/sale_order_views.xml:4`, `addons/sale_product_matrix/views/product_template_views.xml:3`, `addons/sale_product_matrix/views/product_template_views.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `grid_report_saleorder_inherit`, `product_matrix.matrix_product_template_shirt`, `view_order_form_with_variant_grid`, `product_template_grid_view_form`, `product_template_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/sale_product_matrix/report/sale_report_templates.xml:3`
- View/action field declarations: 6; representative evidence: `addons/sale_product_matrix/views/sale_order_views.xml:6`, `addons/sale_product_matrix/views/sale_order_views.xml:8`, `addons/sale_product_matrix/views/product_template_views.xml:5`, `addons/sale_product_matrix/views/product_template_views.xml:7`, `addons/sale_product_matrix/views/product_template_views.xml:17`, `addons/sale_product_matrix/views/product_template_views.xml:19`
- Browser assets: 1; representative files: `addons/sale_product_matrix/static/src/js/sale_product_mixin.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_product_matrix/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `sale.order` (addons/sale_product_matrix/models/sale_order.py:9); inherits `product.template` (addons/sale_product_matrix/models/product_template.py:6); inherits `sale.order.line` (addons/sale_product_matrix/models/sale_order_line.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `product_matrix`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/sale_product_matrix/__init__.py`
- `addons/sale_product_matrix/__manifest__.py`
- `addons/sale_product_matrix/data/product_matrix_demo.xml`
- `addons/sale_product_matrix/i18n/ar.po`
- `addons/sale_product_matrix/i18n/az.po`
- `addons/sale_product_matrix/i18n/bg.po`
- `addons/sale_product_matrix/i18n/bs.po`
- `addons/sale_product_matrix/i18n/ca.po`
- `addons/sale_product_matrix/i18n/cs.po`
- `addons/sale_product_matrix/i18n/da.po`
- `addons/sale_product_matrix/i18n/de.po`
- `addons/sale_product_matrix/i18n/el.po`
- `addons/sale_product_matrix/i18n/es.po`
- `addons/sale_product_matrix/i18n/es_419.po`
- `addons/sale_product_matrix/i18n/et.po`
- `addons/sale_product_matrix/i18n/fa.po`
- `addons/sale_product_matrix/i18n/fi.po`
- `addons/sale_product_matrix/i18n/fr.po`
- `addons/sale_product_matrix/i18n/he.po`
- `addons/sale_product_matrix/i18n/hi.po`
- `addons/sale_product_matrix/i18n/hr.po`
- `addons/sale_product_matrix/i18n/hu.po`
- `addons/sale_product_matrix/i18n/id.po`
- `addons/sale_product_matrix/i18n/it.po`
- `addons/sale_product_matrix/i18n/ja.po`
- `addons/sale_product_matrix/i18n/kab.po`
- `addons/sale_product_matrix/i18n/ko.po`
- `addons/sale_product_matrix/i18n/ku.po`
- `addons/sale_product_matrix/i18n/lo.po`
- `addons/sale_product_matrix/i18n/lt.po`
- `addons/sale_product_matrix/i18n/lv.po`
- `addons/sale_product_matrix/i18n/mn.po`
- `addons/sale_product_matrix/i18n/my.po`
- `addons/sale_product_matrix/i18n/nb.po`
- `addons/sale_product_matrix/i18n/nl.po`
- `addons/sale_product_matrix/i18n/pl.po`
- `addons/sale_product_matrix/i18n/pt.po`
- `addons/sale_product_matrix/i18n/pt_BR.po`
- `addons/sale_product_matrix/i18n/ro.po`
- `addons/sale_product_matrix/i18n/ru.po`
- `addons/sale_product_matrix/i18n/sale_product_matrix.pot`
- `addons/sale_product_matrix/i18n/sk.po`
- `addons/sale_product_matrix/i18n/sl.po`
- `addons/sale_product_matrix/i18n/sr@latin.po`
- `addons/sale_product_matrix/i18n/sv.po`
- `addons/sale_product_matrix/i18n/th.po`
- `addons/sale_product_matrix/i18n/tr.po`
- `addons/sale_product_matrix/i18n/uk.po`
- `addons/sale_product_matrix/i18n/uz.po`
- `addons/sale_product_matrix/i18n/vi.po`
- `addons/sale_product_matrix/i18n/zh_CN.po`
- `addons/sale_product_matrix/i18n/zh_TW.po`
- `addons/sale_product_matrix/models/__init__.py`
- `addons/sale_product_matrix/models/product_template.py`
- `addons/sale_product_matrix/models/sale_order.py`
- `addons/sale_product_matrix/models/sale_order_line.py`
- `addons/sale_product_matrix/report/sale_report_templates.xml`
- `addons/sale_product_matrix/static/src/js/sale_product_mixin.js`
- `addons/sale_product_matrix/views/product_template_views.xml`
- `addons/sale_product_matrix/views/sale_order_views.xml`
