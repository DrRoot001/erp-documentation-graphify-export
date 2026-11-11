# Module: purchase_requisition

- **Module ID:** MOD-501
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_requisition`
- **Manifest:** `addons/purchase_requisition/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module allows you to manage your Purchase Agreements.
===========================================================

Manage calls for tenders and blanket orders. Calls for tenders are used to get
competing offers from different vendors and select the best ones. Blanket orders
are agreements you have with vendors to benefit from a predetermined pricing.

**Scope evidence:** The module contains 80 files, including 9 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `purchase`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase_requisition/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 45 methods, 2 constraint handlers, 2 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/purchase_requisition/models/purchase.py:7`, `addons/purchase_requisition/models/purchase.py:103`, `addons/purchase_requisition/models/product.py:7`, `addons/purchase_requisition/models/product.py:14`, `addons/purchase_requisition/models/purchase_requisition.py:8`, `addons/purchase_requisition/models/purchase_requisition.py:163`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 23 record/template/menu identifiers.
- **Evidence:** `addons/purchase_requisition/report/report_purchaserequisition.xml:4`, `addons/purchase_requisition/report/report_purchaserequisition.xml:155`, `addons/purchase_requisition/report/purchase_requisition_report.xml:3`, `addons/purchase_requisition/data/purchase_requisition_data.xml:4`, `addons/purchase_requisition/data/purchase_requisition_data.xml:11`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:5`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:11`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:21`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:27`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:38`, `addons/purchase_requisition/data/purchase_requisition_demo.xml:44`, `addons/purchase_requisition/views/purchase_requisition_views.xml:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/purchase_requisition/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/purchase_requisition/report/purchase_requisition_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/purchase_requisition/tests/common.py`, `addons/purchase_requisition/tests/test_purchase_requisition.py`, `addons/purchase_requisition/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `report_purchaserequisition_document`, `report_purchaserequisitions`, `action_report_purchase_requisitions`, `seq_blanket_order`, `seq_purchase_template`, `bo_requisition`, `bo_requisition_line`, `rfq1`, `rfq1_line`, `rfq2`, `rfq2_line`, `action_purchase_requisition_to_so`, `action_purchase_requisition_list`, `view_purchase_requisition_form`, `view_purchase_requisition_tree`, `view_purchase_requisition_kanban`, `view_purchase_requisition_filter`, `action_purchase_requisition`, `menu_purchase_requisition_pro_mgt`, `product_supplierinfo_tree_view_inherit`
- Menus: 1; representative evidence: `addons/purchase_requisition/views/purchase_requisition_views.xml:244`
- Templates: 2; representative evidence: `addons/purchase_requisition/report/report_purchaserequisition.xml:4`, `addons/purchase_requisition/report/report_purchaserequisition.xml:155`
- View/action field declarations: 23; representative evidence: `addons/purchase_requisition/report/purchase_requisition_report.xml:5`, `addons/purchase_requisition/views/purchase_requisition_views.xml:9`, `addons/purchase_requisition/views/purchase_requisition_views.xml:10`, `addons/purchase_requisition/views/purchase_requisition_views.xml:19`, `addons/purchase_requisition/views/purchase_requisition_views.xml:20`, `addons/purchase_requisition/views/purchase_requisition_views.xml:30`, `addons/purchase_requisition/views/purchase_requisition_views.xml:31`, `addons/purchase_requisition/views/purchase_requisition_views.xml:147`, `addons/purchase_requisition/views/purchase_requisition_views.xml:148`, `addons/purchase_requisition/views/purchase_requisition_views.xml:167`, `addons/purchase_requisition/views/purchase_requisition_views.xml:168`, `addons/purchase_requisition/views/purchase_requisition_views.xml:189`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_requisition/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/purchase_requisition/report/purchase_requisition_report.xml`

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `purchase.order` (addons/purchase_requisition/models/purchase.py:7); inherits `purchase.order.line` (addons/purchase_requisition/models/purchase.py:103); inherits `product.supplierinfo` (addons/purchase_requisition/models/product.py:7); inherits `product.product` (addons/purchase_requisition/models/product.py:14); `purchase.requisition` (addons/purchase_requisition/models/purchase_requisition.py:8); `purchase.requisition.line` (addons/purchase_requisition/models/purchase_requisition.py:163)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase`
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

- `addons/purchase_requisition/__init__.py`
- `addons/purchase_requisition/__manifest__.py`
- `addons/purchase_requisition/data/purchase_requisition_data.xml`
- `addons/purchase_requisition/data/purchase_requisition_demo.xml`
- `addons/purchase_requisition/i18n/af.po`
- `addons/purchase_requisition/i18n/am.po`
- `addons/purchase_requisition/i18n/ar.po`
- `addons/purchase_requisition/i18n/az.po`
- `addons/purchase_requisition/i18n/bg.po`
- `addons/purchase_requisition/i18n/bs.po`
- `addons/purchase_requisition/i18n/ca.po`
- `addons/purchase_requisition/i18n/cs.po`
- `addons/purchase_requisition/i18n/da.po`
- `addons/purchase_requisition/i18n/de.po`
- `addons/purchase_requisition/i18n/el.po`
- `addons/purchase_requisition/i18n/es.po`
- `addons/purchase_requisition/i18n/es_419.po`
- `addons/purchase_requisition/i18n/es_CL.po`
- `addons/purchase_requisition/i18n/et.po`
- `addons/purchase_requisition/i18n/eu.po`
- `addons/purchase_requisition/i18n/fa.po`
- `addons/purchase_requisition/i18n/fi.po`
- `addons/purchase_requisition/i18n/fo.po`
- `addons/purchase_requisition/i18n/fr.po`
- `addons/purchase_requisition/i18n/fr_BE.po`
- `addons/purchase_requisition/i18n/fr_CA.po`
- `addons/purchase_requisition/i18n/gl.po`
- `addons/purchase_requisition/i18n/gu.po`
- `addons/purchase_requisition/i18n/he.po`
- `addons/purchase_requisition/i18n/hi.po`
- `addons/purchase_requisition/i18n/hr.po`
- `addons/purchase_requisition/i18n/hu.po`
- `addons/purchase_requisition/i18n/id.po`
- `addons/purchase_requisition/i18n/is.po`
- `addons/purchase_requisition/i18n/it.po`
- `addons/purchase_requisition/i18n/ja.po`
- `addons/purchase_requisition/i18n/ka.po`
- `addons/purchase_requisition/i18n/kab.po`
- `addons/purchase_requisition/i18n/km.po`
- `addons/purchase_requisition/i18n/ko.po`
- `addons/purchase_requisition/i18n/ku.po`
- `addons/purchase_requisition/i18n/lo.po`
- `addons/purchase_requisition/i18n/lt.po`
- `addons/purchase_requisition/i18n/lv.po`
- `addons/purchase_requisition/i18n/mk.po`
- `addons/purchase_requisition/i18n/mn.po`
- `addons/purchase_requisition/i18n/my.po`
- `addons/purchase_requisition/i18n/nb.po`
- `addons/purchase_requisition/i18n/nl.po`
- `addons/purchase_requisition/i18n/pl.po`
- `addons/purchase_requisition/i18n/pt.po`
- `addons/purchase_requisition/i18n/pt_BR.po`
- `addons/purchase_requisition/i18n/purchase_requisition.pot`
- `addons/purchase_requisition/i18n/ro.po`
- `addons/purchase_requisition/i18n/ru.po`
- `addons/purchase_requisition/i18n/sk.po`
- `addons/purchase_requisition/i18n/sl.po`
- `addons/purchase_requisition/i18n/sq.po`
- `addons/purchase_requisition/i18n/sr@latin.po`
- `addons/purchase_requisition/i18n/sv.po`
- `addons/purchase_requisition/i18n/th.po`
- `addons/purchase_requisition/i18n/tr.po`
- `addons/purchase_requisition/i18n/uk.po`
- `addons/purchase_requisition/i18n/uz.po`
- `addons/purchase_requisition/i18n/vi.po`
- `addons/purchase_requisition/i18n/zh_CN.po`
- `addons/purchase_requisition/i18n/zh_TW.po`
- `addons/purchase_requisition/models/__init__.py`
- `addons/purchase_requisition/models/product.py`
- `addons/purchase_requisition/models/purchase.py`
- `addons/purchase_requisition/models/purchase_requisition.py`
- `addons/purchase_requisition/report/purchase_requisition_report.xml`
- `addons/purchase_requisition/report/report_purchaserequisition.xml`
- `addons/purchase_requisition/security/ir.access.csv`
- `addons/purchase_requisition/tests/__init__.py`
- `addons/purchase_requisition/tests/common.py`
- `addons/purchase_requisition/tests/test_purchase_requisition.py`
- `addons/purchase_requisition/views/product_views.xml`
- `addons/purchase_requisition/views/purchase_requisition_views.xml`
- `addons/purchase_requisition/views/purchase_views.xml`
