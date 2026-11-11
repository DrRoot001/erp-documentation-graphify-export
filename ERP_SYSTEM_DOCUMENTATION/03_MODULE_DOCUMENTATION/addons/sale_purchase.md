# Module: sale_purchase

- **Module ID:** MOD-528
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_purchase`
- **Manifest:** `addons/sale_purchase/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sale based on service outsourcing.

**Manifest description:**

Allows the outsourcing of services. This module allows one to sell services provided
by external providers and will automatically generate purchase orders directed to the service seller.

**Scope evidence:** The module contains 66 files, including 11 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `purchase`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 58 methods, 0 constraint handlers, 1 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/sale_purchase/models/sale_order.py:7`, `addons/sale_purchase/models/product_template.py:8`, `addons/sale_purchase/models/purchase_order.py:7`, `addons/sale_purchase/models/purchase_order.py:89`, `addons/sale_purchase/models/sale_order_line.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/sale_purchase/data/mail_templates.xml:4`, `addons/sale_purchase/data/mail_templates.xml:28`, `addons/sale_purchase/data/mail_templates.xml:48`, `addons/sale_purchase/views/sale_order_views.xml:4`, `addons/sale_purchase/views/product_views.xml:4`, `addons/sale_purchase/views/purchase_order_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/sale_purchase/tests/test_access_rights.py`, `addons/sale_purchase/tests/test_sale_purchase.py`, `addons/sale_purchase/tests/common.py`, `addons/sale_purchase/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `Message: Alert on purchase orders when ordered quantity decreased on Sales Orders`, `Message: Alert on purchase orders when sales orders are cancelled`, `Message: Alert on sale orders when purchase orders are cancelled`, `sale_order_inherited_form_purchase`, `product_template_form_view`, `purchase_order_inherited_form_sale`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/sale_purchase/data/mail_templates.xml:4`, `addons/sale_purchase/data/mail_templates.xml:28`, `addons/sale_purchase/data/mail_templates.xml:48`
- View/action field declarations: 6; representative evidence: `addons/sale_purchase/views/sale_order_views.xml:6`, `addons/sale_purchase/views/sale_order_views.xml:8`, `addons/sale_purchase/views/product_views.xml:6`, `addons/sale_purchase/views/product_views.xml:8`, `addons/sale_purchase/views/purchase_order_views.xml:5`, `addons/sale_purchase/views/purchase_order_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_purchase/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `sale.order` (addons/sale_purchase/models/sale_order.py:7); inherits `product.template` (addons/sale_purchase/models/product_template.py:8); inherits `purchase.order` (addons/sale_purchase/models/purchase_order.py:7); inherits `purchase.order.line` (addons/sale_purchase/models/purchase_order.py:89); inherits `sale.order.line` (addons/sale_purchase/models/sale_order_line.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `purchase`
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

- `addons/sale_purchase/__init__.py`
- `addons/sale_purchase/__manifest__.py`
- `addons/sale_purchase/data/mail_templates.xml`
- `addons/sale_purchase/i18n/ar.po`
- `addons/sale_purchase/i18n/az.po`
- `addons/sale_purchase/i18n/bg.po`
- `addons/sale_purchase/i18n/bs.po`
- `addons/sale_purchase/i18n/ca.po`
- `addons/sale_purchase/i18n/cs.po`
- `addons/sale_purchase/i18n/da.po`
- `addons/sale_purchase/i18n/de.po`
- `addons/sale_purchase/i18n/el.po`
- `addons/sale_purchase/i18n/es.po`
- `addons/sale_purchase/i18n/es_419.po`
- `addons/sale_purchase/i18n/et.po`
- `addons/sale_purchase/i18n/fa.po`
- `addons/sale_purchase/i18n/fi.po`
- `addons/sale_purchase/i18n/fr.po`
- `addons/sale_purchase/i18n/gu.po`
- `addons/sale_purchase/i18n/he.po`
- `addons/sale_purchase/i18n/hi.po`
- `addons/sale_purchase/i18n/hr.po`
- `addons/sale_purchase/i18n/hu.po`
- `addons/sale_purchase/i18n/id.po`
- `addons/sale_purchase/i18n/is.po`
- `addons/sale_purchase/i18n/it.po`
- `addons/sale_purchase/i18n/ja.po`
- `addons/sale_purchase/i18n/kab.po`
- `addons/sale_purchase/i18n/ko.po`
- `addons/sale_purchase/i18n/ku.po`
- `addons/sale_purchase/i18n/lo.po`
- `addons/sale_purchase/i18n/lt.po`
- `addons/sale_purchase/i18n/lv.po`
- `addons/sale_purchase/i18n/mn.po`
- `addons/sale_purchase/i18n/my.po`
- `addons/sale_purchase/i18n/nb.po`
- `addons/sale_purchase/i18n/nl.po`
- `addons/sale_purchase/i18n/pl.po`
- `addons/sale_purchase/i18n/pt.po`
- `addons/sale_purchase/i18n/pt_BR.po`
- `addons/sale_purchase/i18n/ro.po`
- `addons/sale_purchase/i18n/ru.po`
- `addons/sale_purchase/i18n/sale_purchase.pot`
- `addons/sale_purchase/i18n/sk.po`
- `addons/sale_purchase/i18n/sl.po`
- `addons/sale_purchase/i18n/sr@latin.po`
- `addons/sale_purchase/i18n/sv.po`
- `addons/sale_purchase/i18n/th.po`
- `addons/sale_purchase/i18n/tr.po`
- `addons/sale_purchase/i18n/uk.po`
- `addons/sale_purchase/i18n/uz.po`
- `addons/sale_purchase/i18n/vi.po`
- `addons/sale_purchase/i18n/zh_CN.po`
- `addons/sale_purchase/i18n/zh_TW.po`
- `addons/sale_purchase/models/__init__.py`
- `addons/sale_purchase/models/product_template.py`
- `addons/sale_purchase/models/purchase_order.py`
- `addons/sale_purchase/models/sale_order.py`
- `addons/sale_purchase/models/sale_order_line.py`
- `addons/sale_purchase/tests/__init__.py`
- `addons/sale_purchase/tests/common.py`
- `addons/sale_purchase/tests/test_access_rights.py`
- `addons/sale_purchase/tests/test_sale_purchase.py`
- `addons/sale_purchase/views/product_views.xml`
- `addons/sale_purchase/views/purchase_order_views.xml`
- `addons/sale_purchase/views/sale_order_views.xml`
