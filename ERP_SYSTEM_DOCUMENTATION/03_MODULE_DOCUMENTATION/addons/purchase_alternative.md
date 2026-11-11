# Module: purchase_alternative

- **Module ID:** MOD-494
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_alternative`
- **Manifest:** `addons/purchase_alternative/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module allows you to manage your Purchase Alternative.
===========================================================

It helps users compare product lines across RFQs and decide to order specific products
from different vendors, enabling more flexible and cost-effective purchasing decisions.
create a call for tender by adding alternative requests for quotation to different vendors.
Make your choice by selecting the best combination of lead time, OTD and/or total amount.
By comparing product lines you can also decide to order some products from
one vendor and others from another vendor.

**Scope evidence:** The module contains 69 files, including 10 Python, 5 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `purchase`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 3
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/purchase_alternative/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 33 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/purchase_alternative/models/purchase.py:8`, `addons/purchase_alternative/models/purchase.py:21`, `addons/purchase_alternative/models/purchase.py:172`, `addons/purchase_alternative/wizard/purchase_alternative_warning.py:6`, `addons/purchase_alternative/wizard/purchase_alternative_create.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 3 JavaScript/TypeScript files; static XML analysis found 9 record/template/menu identifiers.
- **Evidence:** `addons/purchase_alternative/wizard/purchase_alternative_create.xml:4`, `addons/purchase_alternative/wizard/purchase_alternative_warning.xml:4`, `addons/purchase_alternative/data/purchase_alternative_demo.xml:8`, `addons/purchase_alternative/data/purchase_alternative_demo.xml:12`, `addons/purchase_alternative/data/purchase_alternative_demo.xml:21`, `addons/purchase_alternative/data/purchase_alternative_demo.xml:25`, `addons/purchase_alternative/data/purchase_alternative_demo.xml:33`, `addons/purchase_alternative/views/purchase_views.xml:3`, `addons/purchase_alternative/views/purchase_views.xml:38`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/purchase_alternative/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/purchase_alternative/tests/test_purchase_alternative.py`, `addons/purchase_alternative/tests/common.py`, `addons/purchase_alternative/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `purchase_alternative_create_form`, `purchase_alternative_warning_form`, `rfq3`, `rfq3_line`, `rfq4`, `rfq4_line`, `rfq_group`, `purchase_order_form`, `purchase_order_line_view_compare_list`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/purchase_alternative/wizard/purchase_alternative_create.xml:6`, `addons/purchase_alternative/wizard/purchase_alternative_create.xml:7`, `addons/purchase_alternative/wizard/purchase_alternative_warning.xml:6`, `addons/purchase_alternative/wizard/purchase_alternative_warning.xml:7`, `addons/purchase_alternative/views/purchase_views.xml:5`, `addons/purchase_alternative/views/purchase_views.xml:7`, `addons/purchase_alternative/views/purchase_views.xml:40`, `addons/purchase_alternative/views/purchase_views.xml:42`
- Browser assets: 3; representative files: `addons/purchase_alternative/static/src/widgets/purchase_order_alternatives_widget.js`, `addons/purchase_alternative/static/src/views/purchase_order_line_compare_list_renderer.js`, `addons/purchase_alternative/static/src/views/purchase_order_line_compare_list_view.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_alternative/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `purchase.order.group` (addons/purchase_alternative/models/purchase.py:8); inherits `purchase.order` (addons/purchase_alternative/models/purchase.py:21); inherits `purchase.order.line` (addons/purchase_alternative/models/purchase.py:172); `purchase.alternative.warning` (addons/purchase_alternative/wizard/purchase_alternative_warning.py:6); `purchase.alternative.create` (addons/purchase_alternative/wizard/purchase_alternative_create.py:6)
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

- `addons/purchase_alternative/__init__.py`
- `addons/purchase_alternative/__manifest__.py`
- `addons/purchase_alternative/data/purchase_alternative_demo.xml`
- `addons/purchase_alternative/i18n/ar.po`
- `addons/purchase_alternative/i18n/az.po`
- `addons/purchase_alternative/i18n/bg.po`
- `addons/purchase_alternative/i18n/bs.po`
- `addons/purchase_alternative/i18n/ca.po`
- `addons/purchase_alternative/i18n/cs.po`
- `addons/purchase_alternative/i18n/da.po`
- `addons/purchase_alternative/i18n/de.po`
- `addons/purchase_alternative/i18n/el.po`
- `addons/purchase_alternative/i18n/es.po`
- `addons/purchase_alternative/i18n/es_419.po`
- `addons/purchase_alternative/i18n/et.po`
- `addons/purchase_alternative/i18n/fa.po`
- `addons/purchase_alternative/i18n/fi.po`
- `addons/purchase_alternative/i18n/fr.po`
- `addons/purchase_alternative/i18n/he.po`
- `addons/purchase_alternative/i18n/hi.po`
- `addons/purchase_alternative/i18n/hr.po`
- `addons/purchase_alternative/i18n/hu.po`
- `addons/purchase_alternative/i18n/id.po`
- `addons/purchase_alternative/i18n/it.po`
- `addons/purchase_alternative/i18n/ja.po`
- `addons/purchase_alternative/i18n/kab.po`
- `addons/purchase_alternative/i18n/ko.po`
- `addons/purchase_alternative/i18n/ku.po`
- `addons/purchase_alternative/i18n/lo.po`
- `addons/purchase_alternative/i18n/lt.po`
- `addons/purchase_alternative/i18n/lv.po`
- `addons/purchase_alternative/i18n/mn.po`
- `addons/purchase_alternative/i18n/my.po`
- `addons/purchase_alternative/i18n/nb.po`
- `addons/purchase_alternative/i18n/nl.po`
- `addons/purchase_alternative/i18n/pl.po`
- `addons/purchase_alternative/i18n/pt.po`
- `addons/purchase_alternative/i18n/pt_BR.po`
- `addons/purchase_alternative/i18n/purchase_alternative.pot`
- `addons/purchase_alternative/i18n/ro.po`
- `addons/purchase_alternative/i18n/ru.po`
- `addons/purchase_alternative/i18n/sk.po`
- `addons/purchase_alternative/i18n/sl.po`
- `addons/purchase_alternative/i18n/sr@latin.po`
- `addons/purchase_alternative/i18n/sv.po`
- `addons/purchase_alternative/i18n/th.po`
- `addons/purchase_alternative/i18n/tr.po`
- `addons/purchase_alternative/i18n/uk.po`
- `addons/purchase_alternative/i18n/uz.po`
- `addons/purchase_alternative/i18n/vi.po`
- `addons/purchase_alternative/i18n/zh_CN.po`
- `addons/purchase_alternative/i18n/zh_TW.po`
- `addons/purchase_alternative/models/__init__.py`
- `addons/purchase_alternative/models/purchase.py`
- `addons/purchase_alternative/security/ir.access.csv`
- `addons/purchase_alternative/static/src/views/purchase_order_line_compare_list_renderer.js`
- `addons/purchase_alternative/static/src/views/purchase_order_line_compare_list_view.js`
- `addons/purchase_alternative/static/src/widgets/purchase_order_alternatives_widget.js`
- `addons/purchase_alternative/static/src/widgets/purchase_order_alternatives_widget.scss`
- `addons/purchase_alternative/static/src/widgets/purchase_order_alternatives_widget.xml`
- `addons/purchase_alternative/tests/__init__.py`
- `addons/purchase_alternative/tests/common.py`
- `addons/purchase_alternative/tests/test_purchase_alternative.py`
- `addons/purchase_alternative/views/purchase_views.xml`
- `addons/purchase_alternative/wizard/__init__.py`
- `addons/purchase_alternative/wizard/purchase_alternative_create.py`
- `addons/purchase_alternative/wizard/purchase_alternative_create.xml`
- `addons/purchase_alternative/wizard/purchase_alternative_warning.py`
- `addons/purchase_alternative/wizard/purchase_alternative_warning.xml`
