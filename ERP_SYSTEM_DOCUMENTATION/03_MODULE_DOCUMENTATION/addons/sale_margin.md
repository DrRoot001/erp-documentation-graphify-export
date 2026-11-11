# Module: sale_margin

- **Module ID:** MOD-519
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_margin`
- **Manifest:** `addons/sale_margin/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module adds the 'Margin' on sales order.
=============================================

This gives the profitability by calculating the difference between the Unit
Price and Cost Price.

**Scope evidence:** The module contains 78 files, including 10 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `sale_management`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 26 methods, 0 constraint handlers, 2 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/sale_margin/models/sale_order.py:6`, `addons/sale_margin/models/sale_order_template_line.py:6`, `addons/sale_margin/models/sale_order_line.py:8`, `addons/sale_margin/report/sale_report.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/sale_margin/report/sale_report_views.xml:4`, `addons/sale_margin/report/sale_report_views.xml:25`, `addons/sale_margin/report/sale_report_views.xml:44`, `addons/sale_margin/report/sale_report_views.xml:55`, `addons/sale_margin/report/sale_report_views.xml:68`, `addons/sale_margin/report/sale_report_views.xml:82`, `addons/sale_margin/report/sale_report_views.xml:89`, `addons/sale_margin/report/sale_report_views.xml:96`, `addons/sale_margin/report/sale_report_views.xml:103`, `addons/sale_margin/data/sale_margin_demo.xml:4`, `addons/sale_margin/data/sale_margin_demo.xml:8`, `addons/sale_margin/data/sale_margin_demo.xml:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/sale_margin/tests/__init__.py`, `addons/sale_margin/tests/test_sale_margin.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `sale_report_projected_margins_list`, `sale_report_projected_margins_kanban`, `sale_report_view_projected_margins_graph`, `sale_report_view_projected_margins_pivot`, `action_order_report_projected_margins`, `action_order_report_projected_margins_view_list`, `action_order_report_projected_margins_view_pivot`, `action_order_report_projected_margins_view_graph`, `action_order_report_projected_margins_view_kanban`, `sale.sale_order_line_1`, `sale.sale_order_line_2`, `sale.sale_order_line_3`, `sale.sale_order_line_12`, `sale.sale_order_line_16`, `sale.sale_order_line_17`, `sale.sale_order_line_18`, `sale.sale_order_line_19`, `sale_margin_sale_order`, `sale_margin_sale_order_pivot`, `sale_margin_sale_order_graph`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 22; representative evidence: `addons/sale_margin/report/sale_report_views.xml:6`, `addons/sale_margin/report/sale_report_views.xml:7`, `addons/sale_margin/report/sale_report_views.xml:27`, `addons/sale_margin/report/sale_report_views.xml:28`, `addons/sale_margin/report/sale_report_views.xml:46`, `addons/sale_margin/report/sale_report_views.xml:47`, `addons/sale_margin/report/sale_report_views.xml:57`, `addons/sale_margin/report/sale_report_views.xml:58`, `addons/sale_margin/report/sale_report_views.xml:70`, `addons/sale_margin/report/sale_report_views.xml:72`, `addons/sale_margin/report/sale_report_views.xml:84`, `addons/sale_margin/report/sale_report_views.xml:91`
- Browser assets: 1; representative files: `addons/sale_margin/static/src/js/labeled_field_short_labels.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_margin/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `sale.order` (addons/sale_margin/models/sale_order.py:6); inherits `sale.order.template.line` (addons/sale_margin/models/sale_order_template_line.py:6); inherits `sale.order.line` (addons/sale_margin/models/sale_order_line.py:8); inherits `sale.report` (addons/sale_margin/report/sale_report.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_management`
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

- `addons/sale_margin/__init__.py`
- `addons/sale_margin/__manifest__.py`
- `addons/sale_margin/data/sale_margin_demo.xml`
- `addons/sale_margin/i18n/af.po`
- `addons/sale_margin/i18n/am.po`
- `addons/sale_margin/i18n/ar.po`
- `addons/sale_margin/i18n/az.po`
- `addons/sale_margin/i18n/bg.po`
- `addons/sale_margin/i18n/bs.po`
- `addons/sale_margin/i18n/ca.po`
- `addons/sale_margin/i18n/cs.po`
- `addons/sale_margin/i18n/da.po`
- `addons/sale_margin/i18n/de.po`
- `addons/sale_margin/i18n/el.po`
- `addons/sale_margin/i18n/es.po`
- `addons/sale_margin/i18n/es_419.po`
- `addons/sale_margin/i18n/es_CL.po`
- `addons/sale_margin/i18n/et.po`
- `addons/sale_margin/i18n/eu.po`
- `addons/sale_margin/i18n/fa.po`
- `addons/sale_margin/i18n/fi.po`
- `addons/sale_margin/i18n/fo.po`
- `addons/sale_margin/i18n/fr.po`
- `addons/sale_margin/i18n/fr_BE.po`
- `addons/sale_margin/i18n/fr_CA.po`
- `addons/sale_margin/i18n/gl.po`
- `addons/sale_margin/i18n/gu.po`
- `addons/sale_margin/i18n/he.po`
- `addons/sale_margin/i18n/hi.po`
- `addons/sale_margin/i18n/hr.po`
- `addons/sale_margin/i18n/hu.po`
- `addons/sale_margin/i18n/id.po`
- `addons/sale_margin/i18n/is.po`
- `addons/sale_margin/i18n/it.po`
- `addons/sale_margin/i18n/ja.po`
- `addons/sale_margin/i18n/ka.po`
- `addons/sale_margin/i18n/kab.po`
- `addons/sale_margin/i18n/km.po`
- `addons/sale_margin/i18n/ko.po`
- `addons/sale_margin/i18n/ku.po`
- `addons/sale_margin/i18n/lo.po`
- `addons/sale_margin/i18n/lt.po`
- `addons/sale_margin/i18n/lv.po`
- `addons/sale_margin/i18n/mk.po`
- `addons/sale_margin/i18n/mn.po`
- `addons/sale_margin/i18n/my.po`
- `addons/sale_margin/i18n/nb.po`
- `addons/sale_margin/i18n/nl.po`
- `addons/sale_margin/i18n/pl.po`
- `addons/sale_margin/i18n/pt.po`
- `addons/sale_margin/i18n/pt_BR.po`
- `addons/sale_margin/i18n/ro.po`
- `addons/sale_margin/i18n/ru.po`
- `addons/sale_margin/i18n/sale_margin.pot`
- `addons/sale_margin/i18n/sk.po`
- `addons/sale_margin/i18n/sl.po`
- `addons/sale_margin/i18n/sr@latin.po`
- `addons/sale_margin/i18n/sv.po`
- `addons/sale_margin/i18n/ta.po`
- `addons/sale_margin/i18n/th.po`
- `addons/sale_margin/i18n/tr.po`
- `addons/sale_margin/i18n/uk.po`
- `addons/sale_margin/i18n/uz.po`
- `addons/sale_margin/i18n/vi.po`
- `addons/sale_margin/i18n/zh_CN.po`
- `addons/sale_margin/i18n/zh_TW.po`
- `addons/sale_margin/models/__init__.py`
- `addons/sale_margin/models/sale_order.py`
- `addons/sale_margin/models/sale_order_line.py`
- `addons/sale_margin/models/sale_order_template_line.py`
- `addons/sale_margin/report/__init__.py`
- `addons/sale_margin/report/sale_report.py`
- `addons/sale_margin/report/sale_report_views.xml`
- `addons/sale_margin/static/src/js/labeled_field_short_labels.js`
- `addons/sale_margin/tests/__init__.py`
- `addons/sale_margin/tests/test_sale_margin.py`
- `addons/sale_margin/views/sale_order_template_views.xml`
- `addons/sale_margin/views/sale_order_views.xml`
