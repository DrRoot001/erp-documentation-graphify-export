# Module: product_expiry

- **Module ID:** MOD-472
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/product_expiry`
- **Manifest:** `addons/product_expiry/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Track different dates on products and production lots.
======================================================

Following dates can be tracked:
-------------------------------
    - end of life
    - best before date
    - removal date
    - alert date

Also implements the removal strategy First Expiry First Out (FEFO) widely used, for example, in food industries.

**Scope evidence:** The module contains 104 files, including 22 Python, 15 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `stock`.

## 2. Module structure

- Model/business logic files: 15
- Controller/API files: 0
- XML/data/view/template files: 15
- Browser asset files: 4
- Security files: 2
- Test files: 3
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/product_expiry/security/ir.access.csv`, `addons/product_expiry/security/stock_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 15 model declarations, 71 methods, 0 constraint handlers, 3 onchange handlers, and 8 dependency declarations.
- **Evidence:** `addons/product_expiry/models/product_product.py:8`, `addons/product_expiry/models/product_product.py:35`, `addons/product_expiry/models/stock_move_line.py:8`, `addons/product_expiry/models/res_groups.py:6`, `addons/product_expiry/models/res_config_settings.py:7`, `addons/product_expiry/models/production_lot.py:7`, `addons/product_expiry/models/stock_move.py:12`, `addons/product_expiry/models/stock_quant.py:7`, `addons/product_expiry/models/stock_picking.py:8`, `addons/product_expiry/models/stock_rule.py:5`, `addons/product_expiry/report/stock_traceability.py:7`, `addons/product_expiry/report/report_stock_quantity.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 15 XML files and 4 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/product_expiry/security/stock_security.xml:4`, `addons/product_expiry/report/report_stock_traceability.xml:4`, `addons/product_expiry/report/report_lot_barcode.xml:3`, `addons/product_expiry/report/report_lot_barcode.xml:16`, `addons/product_expiry/report/report_lot_barcode.xml:29`, `addons/product_expiry/report/report_lot_barcode.xml:48`, `addons/product_expiry/report/report_deliveryslip.xml:3`, `addons/product_expiry/report/report_deliveryslip.xml:15`, `addons/product_expiry/report/report_package_barcode.xml:3`, `addons/product_expiry/wizard/confirm_expiry_view.xml:3`, `addons/product_expiry/data/product_expiry_data.xml:3`, `addons/product_expiry/views/stock_move_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/product_expiry/security/ir.access.csv`, `addons/product_expiry/security/stock_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/product_expiry/models/stock_rule.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/product_expiry/tests/test_generate_serial_numbers.py`, `addons/product_expiry/tests/__init__.py`, `addons/product_expiry/tests/test_stock_lot.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 15; representative identifiers: `group_expiry_date_on_delivery_slip`, `report_stock_body_print`, `report_lot_label_expiry`, `report_lot_qr_label_expiry`, `report_lot_label_zpl_expiry`, `alternative_zpl_lot_label_qr_expiry`, `stock_report_delivery_document_inherit_product_expiry`, `stock_report_delivery_has_serial_move_line_inherit_product_expiry`, `report_package_barcode_content_inherit_expiry`, `confirm_expiry_view`, `removal_fefo`, `view_stock_move_operations_expiry`, `view_stock_move_line_operation_tree_expiry`, `view_stock_move_line_detailed_operation_tree_expiry`, `res_config_settings_view_form_stock`, `view_move_form_expiry`, `search_product_lot_filter_inherit_product_expiry`, `view_production_lot_view_tree`, `view_production_lot_view_kanban`, `view_stock_quant_tree`
- Menus: 0; representative evidence: Not found in module
- Templates: 8; representative evidence: `addons/product_expiry/report/report_stock_traceability.xml:4`, `addons/product_expiry/report/report_lot_barcode.xml:3`, `addons/product_expiry/report/report_lot_barcode.xml:16`, `addons/product_expiry/report/report_lot_barcode.xml:29`, `addons/product_expiry/report/report_lot_barcode.xml:48`, `addons/product_expiry/report/report_deliveryslip.xml:3`, `addons/product_expiry/report/report_deliveryslip.xml:15`, `addons/product_expiry/report/report_package_barcode.xml:3`
- View/action field declarations: 28; representative evidence: `addons/product_expiry/wizard/confirm_expiry_view.xml:5`, `addons/product_expiry/wizard/confirm_expiry_view.xml:6`, `addons/product_expiry/views/stock_move_views.xml:5`, `addons/product_expiry/views/stock_move_views.xml:7`, `addons/product_expiry/views/stock_move_views.xml:17`, `addons/product_expiry/views/stock_move_views.xml:19`, `addons/product_expiry/views/stock_move_views.xml:37`, `addons/product_expiry/views/stock_move_views.xml:39`, `addons/product_expiry/views/res_config_settings_views.xml:5`, `addons/product_expiry/views/res_config_settings_views.xml:7`, `addons/product_expiry/views/production_lot_views.xml:5`, `addons/product_expiry/views/production_lot_views.xml:7`
- Browser assets: 4; representative files: `addons/product_expiry/static/src/stock_traceability_report_backend.js`, `addons/product_expiry/static/src/forecasted_header.js`, `addons/product_expiry/static/src/forecasted_details.js`, `addons/product_expiry/static/tests/tours/stock_picking_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/product_expiry/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/product_expiry/models/stock_rule.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 15
- Representative model evidence: inherits `product.product` (addons/product_expiry/models/product_product.py:8); inherits `product.template` (addons/product_expiry/models/product_product.py:35); inherits `stock.move.line` (addons/product_expiry/models/stock_move_line.py:8); inherits `res.groups` (addons/product_expiry/models/res_groups.py:6); inherits `res.config.settings` (addons/product_expiry/models/res_config_settings.py:7); inherits `stock.lot` (addons/product_expiry/models/production_lot.py:7); inherits `stock.move` (addons/product_expiry/models/stock_move.py:12); inherits `stock.quant` (addons/product_expiry/models/stock_quant.py:7); inherits `stock.picking` (addons/product_expiry/models/stock_picking.py:8); inherits `stock.rule` (addons/product_expiry/models/stock_rule.py:5); inherits `stock.traceability.report` (addons/product_expiry/report/stock_traceability.py:7); inherits `report.stock.quantity` (addons/product_expiry/report/report_stock_quantity.py:7); inherits `stock.forecasted_product_product` (addons/product_expiry/report/stock_forecasted.py:8); inherits `lot.label.layout` (addons/product_expiry/wizard/stock_lot_label_layout.py:7); `expiry.picking.confirmation` (addons/product_expiry/wizard/confirm_expiry.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `stock`
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

- `addons/product_expiry/__init__.py`
- `addons/product_expiry/__manifest__.py`
- `addons/product_expiry/data/product_expiry_data.xml`
- `addons/product_expiry/i18n/am.po`
- `addons/product_expiry/i18n/ar.po`
- `addons/product_expiry/i18n/az.po`
- `addons/product_expiry/i18n/bg.po`
- `addons/product_expiry/i18n/bs.po`
- `addons/product_expiry/i18n/ca.po`
- `addons/product_expiry/i18n/cs.po`
- `addons/product_expiry/i18n/da.po`
- `addons/product_expiry/i18n/de.po`
- `addons/product_expiry/i18n/el.po`
- `addons/product_expiry/i18n/es.po`
- `addons/product_expiry/i18n/es_419.po`
- `addons/product_expiry/i18n/et.po`
- `addons/product_expiry/i18n/eu.po`
- `addons/product_expiry/i18n/fa.po`
- `addons/product_expiry/i18n/fi.po`
- `addons/product_expiry/i18n/fr.po`
- `addons/product_expiry/i18n/gl.po`
- `addons/product_expiry/i18n/gu.po`
- `addons/product_expiry/i18n/he.po`
- `addons/product_expiry/i18n/hi.po`
- `addons/product_expiry/i18n/hr.po`
- `addons/product_expiry/i18n/hu.po`
- `addons/product_expiry/i18n/id.po`
- `addons/product_expiry/i18n/is.po`
- `addons/product_expiry/i18n/it.po`
- `addons/product_expiry/i18n/ja.po`
- `addons/product_expiry/i18n/kab.po`
- `addons/product_expiry/i18n/km.po`
- `addons/product_expiry/i18n/ko.po`
- `addons/product_expiry/i18n/ku.po`
- `addons/product_expiry/i18n/lo.po`
- `addons/product_expiry/i18n/lt.po`
- `addons/product_expiry/i18n/lv.po`
- `addons/product_expiry/i18n/mk.po`
- `addons/product_expiry/i18n/mn.po`
- `addons/product_expiry/i18n/my.po`
- `addons/product_expiry/i18n/nb.po`
- `addons/product_expiry/i18n/nl.po`
- `addons/product_expiry/i18n/pl.po`
- `addons/product_expiry/i18n/product_expiry.pot`
- `addons/product_expiry/i18n/pt.po`
- `addons/product_expiry/i18n/pt_BR.po`
- `addons/product_expiry/i18n/ro.po`
- `addons/product_expiry/i18n/ru.po`
- `addons/product_expiry/i18n/sk.po`
- `addons/product_expiry/i18n/sl.po`
- `addons/product_expiry/i18n/sr@latin.po`
- `addons/product_expiry/i18n/sv.po`
- `addons/product_expiry/i18n/th.po`
- `addons/product_expiry/i18n/tr.po`
- `addons/product_expiry/i18n/uk.po`
- `addons/product_expiry/i18n/uz.po`
- `addons/product_expiry/i18n/vi.po`
- `addons/product_expiry/i18n/zh_CN.po`
- `addons/product_expiry/i18n/zh_TW.po`
- `addons/product_expiry/models/__init__.py`
- `addons/product_expiry/models/product_product.py`
- `addons/product_expiry/models/production_lot.py`
- `addons/product_expiry/models/res_config_settings.py`
- `addons/product_expiry/models/res_groups.py`
- `addons/product_expiry/models/stock_move.py`
- `addons/product_expiry/models/stock_move_line.py`
- `addons/product_expiry/models/stock_picking.py`
- `addons/product_expiry/models/stock_quant.py`
- `addons/product_expiry/models/stock_rule.py`
- `addons/product_expiry/report/__init__.py`
- `addons/product_expiry/report/report_deliveryslip.xml`
- `addons/product_expiry/report/report_lot_barcode.xml`
- `addons/product_expiry/report/report_package_barcode.xml`
- `addons/product_expiry/report/report_stock_quantity.py`
- `addons/product_expiry/report/report_stock_traceability.xml`
- `addons/product_expiry/report/stock_forecasted.py`
- `addons/product_expiry/report/stock_traceability.py`
- `addons/product_expiry/security/ir.access.csv`
- `addons/product_expiry/security/stock_security.xml`
- `addons/product_expiry/static/description/icon.png`
- `addons/product_expiry/static/description/icon.svg`
- `addons/product_expiry/static/img/product_product_from-image.jpg`
- `addons/product_expiry/static/img/product_product_jambon-image.jpg`
- `addons/product_expiry/static/img/product_product_lait-image.jpg`
- `addons/product_expiry/static/img/product_product_pain-image.jpg`
- `addons/product_expiry/static/src/forecasted_details.js`
- `addons/product_expiry/static/src/forecasted_details.xml`
- `addons/product_expiry/static/src/forecasted_header.js`
- `addons/product_expiry/static/src/forecasted_header.xml`
- `addons/product_expiry/static/src/stock_traceability_report_backend.js`
- `addons/product_expiry/static/src/stock_traceability_report_backend.xml`
- `addons/product_expiry/static/tests/tours/stock_picking_tour.js`
- `addons/product_expiry/tests/__init__.py`
- `addons/product_expiry/tests/test_generate_serial_numbers.py`
- `addons/product_expiry/tests/test_stock_lot.py`
- `addons/product_expiry/views/product_template_views.xml`
- `addons/product_expiry/views/production_lot_views.xml`
- `addons/product_expiry/views/res_config_settings_views.xml`
- `addons/product_expiry/views/stock_move_views.xml`
- `addons/product_expiry/views/stock_quant_views.xml`
- `addons/product_expiry/wizard/__init__.py`
- `addons/product_expiry/wizard/confirm_expiry.py`
- `addons/product_expiry/wizard/confirm_expiry_view.xml`
- `addons/product_expiry/wizard/stock_lot_label_layout.py`
