# Module: product_margin

- **Module ID:** MOD-473
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/product_margin`
- **Manifest:** `addons/product_margin/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Adds a reporting menu in products that computes sales, purchases, margins and other interesting indicators based on invoices.
=============================================================================================================================

The wizard to launch the report has several options to help you get the data you need.

**Scope evidence:** The module contains 75 files, including 8 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/product_margin/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 11 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/product_margin/models/product_product.py:11`, `addons/product_margin/wizard/product_margin.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/product_margin/wizard/product_margin_view.xml:3`, `addons/product_margin/wizard/product_margin_view.xml:21`, `addons/product_margin/views/product_product_views.xml:3`, `addons/product_margin/views/product_product_views.xml:15`, `addons/product_margin/views/product_product_views.xml:61`, `addons/product_margin/views/product_product_views.xml:87`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/product_margin/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/product_margin/tests/test_product_margin.py`, `addons/product_margin/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `product_margin_form_view`, `product_margin_act_window`, `view_product_margin_graph`, `view_product_margin_form`, `view_product_margin_tree`, `Product Margins…`
- Menus: 1; representative evidence: `addons/product_margin/views/product_product_views.xml:87`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/product_margin/wizard/product_margin_view.xml:5`, `addons/product_margin/wizard/product_margin_view.xml:6`, `addons/product_margin/wizard/product_margin_view.xml:23`, `addons/product_margin/wizard/product_margin_view.xml:24`, `addons/product_margin/views/product_product_views.xml:5`, `addons/product_margin/views/product_product_views.xml:7`, `addons/product_margin/views/product_product_views.xml:17`, `addons/product_margin/views/product_product_views.xml:19`, `addons/product_margin/views/product_product_views.xml:63`, `addons/product_margin/views/product_product_views.xml:65`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/product_margin/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `product.product` (addons/product_margin/models/product_product.py:11); `product.margin` (addons/product_margin/wizard/product_margin.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`
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

- `addons/product_margin/__init__.py`
- `addons/product_margin/__manifest__.py`
- `addons/product_margin/i18n/af.po`
- `addons/product_margin/i18n/am.po`
- `addons/product_margin/i18n/ar.po`
- `addons/product_margin/i18n/az.po`
- `addons/product_margin/i18n/bg.po`
- `addons/product_margin/i18n/bs.po`
- `addons/product_margin/i18n/ca.po`
- `addons/product_margin/i18n/cs.po`
- `addons/product_margin/i18n/da.po`
- `addons/product_margin/i18n/de.po`
- `addons/product_margin/i18n/el.po`
- `addons/product_margin/i18n/es.po`
- `addons/product_margin/i18n/es_419.po`
- `addons/product_margin/i18n/es_CL.po`
- `addons/product_margin/i18n/et.po`
- `addons/product_margin/i18n/eu.po`
- `addons/product_margin/i18n/fa.po`
- `addons/product_margin/i18n/fi.po`
- `addons/product_margin/i18n/fo.po`
- `addons/product_margin/i18n/fr.po`
- `addons/product_margin/i18n/fr_BE.po`
- `addons/product_margin/i18n/fr_CA.po`
- `addons/product_margin/i18n/gl.po`
- `addons/product_margin/i18n/gu.po`
- `addons/product_margin/i18n/he.po`
- `addons/product_margin/i18n/hi.po`
- `addons/product_margin/i18n/hr.po`
- `addons/product_margin/i18n/hu.po`
- `addons/product_margin/i18n/id.po`
- `addons/product_margin/i18n/is.po`
- `addons/product_margin/i18n/it.po`
- `addons/product_margin/i18n/ja.po`
- `addons/product_margin/i18n/ka.po`
- `addons/product_margin/i18n/kab.po`
- `addons/product_margin/i18n/km.po`
- `addons/product_margin/i18n/ko.po`
- `addons/product_margin/i18n/ku.po`
- `addons/product_margin/i18n/lo.po`
- `addons/product_margin/i18n/lt.po`
- `addons/product_margin/i18n/lv.po`
- `addons/product_margin/i18n/mk.po`
- `addons/product_margin/i18n/mn.po`
- `addons/product_margin/i18n/my.po`
- `addons/product_margin/i18n/nb.po`
- `addons/product_margin/i18n/nl.po`
- `addons/product_margin/i18n/pl.po`
- `addons/product_margin/i18n/product_margin.pot`
- `addons/product_margin/i18n/pt.po`
- `addons/product_margin/i18n/pt_BR.po`
- `addons/product_margin/i18n/ro.po`
- `addons/product_margin/i18n/ru.po`
- `addons/product_margin/i18n/sk.po`
- `addons/product_margin/i18n/sl.po`
- `addons/product_margin/i18n/sq.po`
- `addons/product_margin/i18n/sr@latin.po`
- `addons/product_margin/i18n/sv.po`
- `addons/product_margin/i18n/ta.po`
- `addons/product_margin/i18n/th.po`
- `addons/product_margin/i18n/tr.po`
- `addons/product_margin/i18n/uk.po`
- `addons/product_margin/i18n/uz.po`
- `addons/product_margin/i18n/vi.po`
- `addons/product_margin/i18n/zh_CN.po`
- `addons/product_margin/i18n/zh_TW.po`
- `addons/product_margin/models/__init__.py`
- `addons/product_margin/models/product_product.py`
- `addons/product_margin/security/ir.access.csv`
- `addons/product_margin/tests/__init__.py`
- `addons/product_margin/tests/test_product_margin.py`
- `addons/product_margin/views/product_product_views.xml`
- `addons/product_margin/wizard/__init__.py`
- `addons/product_margin/wizard/product_margin.py`
- `addons/product_margin/wizard/product_margin_view.xml`
