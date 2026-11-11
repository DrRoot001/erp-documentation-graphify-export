# Module: sale_gelato

- **Module ID:** MOD-514
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_gelato`
- **Manifest:** `addons/sale_gelato/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Place orders through Gelato's print-on-demand service

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 82 files, including 22 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `delivery`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 2
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 59 methods, 0 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/sale_gelato/models/res_partner.py:10`, `addons/sale_gelato/models/sale_order.py:16`, `addons/sale_gelato/models/product_product.py:7`, `addons/sale_gelato/models/product_template.py:10`, `addons/sale_gelato/models/delivery_carrier.py:9`, `addons/sale_gelato/models/product_document.py:7`, `addons/sale_gelato/models/sale_order_line.py:7`, `addons/sale_gelato/models/res_company.py:6`, `addons/sale_gelato/wizards/res_config_settings.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/sale_gelato/controllers/main.py:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/sale_gelato/wizards/res_config_settings_views.xml:4`, `addons/sale_gelato/data/mail_template_data.xml:4`, `addons/sale_gelato/data/product_data.xml:4`, `addons/sale_gelato/data/product_data.xml:14`, `addons/sale_gelato/data/delivery_carrier_data.xml:4`, `addons/sale_gelato/data/delivery_carrier_data.xml:13`, `addons/sale_gelato/views/product_document_views.xml:4`, `addons/sale_gelato/views/delivery_carrier_views.xml:4`, `addons/sale_gelato/views/product_product_views.xml:4`, `addons/sale_gelato/views/product_template_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/sale_gelato/tests/test_sale_order.py`, `addons/sale_gelato/tests/common.py`, `addons/sale_gelato/tests/test_product_template.py`, `addons/sale_gelato/tests/__init__.py`, `addons/sale_gelato/tests/test_delivery_carrier.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `res_config_settings_form`, `order_status_update`, `standard_delivery_product`, `express_delivery_product`, `standard_delivery`, `express_delivery`, `product_document_form`, `delivery_carrier_form`, `product_product_normal_form`, `product_template_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/sale_gelato/wizards/res_config_settings_views.xml:6`, `addons/sale_gelato/wizards/res_config_settings_views.xml:8`, `addons/sale_gelato/views/product_document_views.xml:6`, `addons/sale_gelato/views/product_document_views.xml:8`, `addons/sale_gelato/views/delivery_carrier_views.xml:6`, `addons/sale_gelato/views/delivery_carrier_views.xml:8`, `addons/sale_gelato/views/product_product_views.xml:6`, `addons/sale_gelato/views/product_product_views.xml:8`, `addons/sale_gelato/views/product_template_views.xml:6`, `addons/sale_gelato/views/product_template_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_gelato/__manifest__.py`
- **HTTP entry points:** `addons/sale_gelato/controllers/main.py:18`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `res.partner` (addons/sale_gelato/models/res_partner.py:10); inherits `sale.order` (addons/sale_gelato/models/sale_order.py:16); inherits `product.product` (addons/sale_gelato/models/product_product.py:7); inherits `product.template` (addons/sale_gelato/models/product_template.py:10); inherits `delivery.carrier` (addons/sale_gelato/models/delivery_carrier.py:9); inherits `product.document` (addons/sale_gelato/models/product_document.py:7); inherits `sale.order.line` (addons/sale_gelato/models/sale_order_line.py:7); inherits `res.company` (addons/sale_gelato/models/res_company.py:6); inherits `res.config.settings` (addons/sale_gelato/wizards/res_config_settings.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/sale_gelato/controllers/main.py:18`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `delivery`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/sale_gelato/__init__.py`
- `addons/sale_gelato/__manifest__.py`
- `addons/sale_gelato/const.py`
- `addons/sale_gelato/controllers/__init__.py`
- `addons/sale_gelato/controllers/main.py`
- `addons/sale_gelato/data/delivery_carrier_data.xml`
- `addons/sale_gelato/data/mail_template_data.xml`
- `addons/sale_gelato/data/neutralize.sql`
- `addons/sale_gelato/data/product_data.xml`
- `addons/sale_gelato/i18n/ar.po`
- `addons/sale_gelato/i18n/az.po`
- `addons/sale_gelato/i18n/bg.po`
- `addons/sale_gelato/i18n/bs.po`
- `addons/sale_gelato/i18n/ca.po`
- `addons/sale_gelato/i18n/cs.po`
- `addons/sale_gelato/i18n/da.po`
- `addons/sale_gelato/i18n/de.po`
- `addons/sale_gelato/i18n/el.po`
- `addons/sale_gelato/i18n/es.po`
- `addons/sale_gelato/i18n/es_419.po`
- `addons/sale_gelato/i18n/et.po`
- `addons/sale_gelato/i18n/fa.po`
- `addons/sale_gelato/i18n/fi.po`
- `addons/sale_gelato/i18n/fr.po`
- `addons/sale_gelato/i18n/he.po`
- `addons/sale_gelato/i18n/hi.po`
- `addons/sale_gelato/i18n/hr.po`
- `addons/sale_gelato/i18n/hu.po`
- `addons/sale_gelato/i18n/id.po`
- `addons/sale_gelato/i18n/it.po`
- `addons/sale_gelato/i18n/ja.po`
- `addons/sale_gelato/i18n/kab.po`
- `addons/sale_gelato/i18n/ko.po`
- `addons/sale_gelato/i18n/ku.po`
- `addons/sale_gelato/i18n/lo.po`
- `addons/sale_gelato/i18n/lt.po`
- `addons/sale_gelato/i18n/lv.po`
- `addons/sale_gelato/i18n/mn.po`
- `addons/sale_gelato/i18n/my.po`
- `addons/sale_gelato/i18n/nb.po`
- `addons/sale_gelato/i18n/nl.po`
- `addons/sale_gelato/i18n/pl.po`
- `addons/sale_gelato/i18n/pt.po`
- `addons/sale_gelato/i18n/pt_BR.po`
- `addons/sale_gelato/i18n/ro.po`
- `addons/sale_gelato/i18n/ru.po`
- `addons/sale_gelato/i18n/sale_gelato.pot`
- `addons/sale_gelato/i18n/sk.po`
- `addons/sale_gelato/i18n/sl.po`
- `addons/sale_gelato/i18n/sr@latin.po`
- `addons/sale_gelato/i18n/sv.po`
- `addons/sale_gelato/i18n/th.po`
- `addons/sale_gelato/i18n/tr.po`
- `addons/sale_gelato/i18n/uk.po`
- `addons/sale_gelato/i18n/uz.po`
- `addons/sale_gelato/i18n/vi.po`
- `addons/sale_gelato/i18n/zh_CN.po`
- `addons/sale_gelato/i18n/zh_TW.po`
- `addons/sale_gelato/models/__init__.py`
- `addons/sale_gelato/models/delivery_carrier.py`
- `addons/sale_gelato/models/product_document.py`
- `addons/sale_gelato/models/product_product.py`
- `addons/sale_gelato/models/product_template.py`
- `addons/sale_gelato/models/res_company.py`
- `addons/sale_gelato/models/res_partner.py`
- `addons/sale_gelato/models/sale_order.py`
- `addons/sale_gelato/models/sale_order_line.py`
- `addons/sale_gelato/static/description/icon.png`
- `addons/sale_gelato/static/description/icon.svg`
- `addons/sale_gelato/tests/__init__.py`
- `addons/sale_gelato/tests/common.py`
- `addons/sale_gelato/tests/test_delivery_carrier.py`
- `addons/sale_gelato/tests/test_product_template.py`
- `addons/sale_gelato/tests/test_sale_order.py`
- `addons/sale_gelato/utils.py`
- `addons/sale_gelato/views/delivery_carrier_views.xml`
- `addons/sale_gelato/views/product_document_views.xml`
- `addons/sale_gelato/views/product_product_views.xml`
- `addons/sale_gelato/views/product_template_views.xml`
- `addons/sale_gelato/wizards/__init__.py`
- `addons/sale_gelato/wizards/res_config_settings.py`
- `addons/sale_gelato/wizards/res_config_settings_views.xml`
