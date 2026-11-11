# Module: product

- **Module ID:** MOD-470
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/product`
- **Manifest:** `addons/product/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module for managing products and pricelists in Odoo.
========================================================================

Products support variants, different pricing methods, vendors information,
make to stock/order, different units of measure, packaging and properties.

Pricelists support:
-------------------
    * Multiple-level of discount (by product, category, quantities)
    * Compute price based on different criteria:
        * Other pricelist
        * Cost price
        * List price
        * Vendor price

Pricelists preferences by product and/or partners.

Print product labels with barcode.

**Scope evidence:** The module contains 257 files, including 57 Python, 44 XML, and 22 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `mail`, `uom`.

## 2. Module structure

- Model/business logic files: 34
- Controller/API files: 4
- XML/data/view/template files: 44
- Browser asset files: 22
- Security files: 2
- Test files: 17
- Scheduled/automation evidence files: 3
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/product/security/product_security.xml`, `addons/product/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 34 model declarations, 647 methods, 18 constraint handlers, 20 onchange handlers, and 78 dependency declarations.
- **Evidence:** `addons/product/models/product_category.py:8`, `addons/product/models/res_partner.py:6`, `addons/product/models/product_product.py:15`, `addons/product/models/product_combo.py:8`, `addons/product/models/product_attribute.py:7`, `addons/product/models/uom_uom.py:8`, `addons/product/models/product_template.py:19`, `addons/product/models/product_catalog_mixin.py:8`, `addons/product/models/res_groups.py:6`, `addons/product/models/product_attribute_value.py:9`, `addons/product/models/product_uom.py:8`, `addons/product/models/res_config_settings.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 4 controller files and 4 route declarations.
- **Evidence:** `addons/product/controllers/product_document.py:14`, `addons/product/controllers/pricelist_report.py:13`, `addons/product/controllers/catalog.py:7`, `addons/product/controllers/catalog.py:36`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 44 XML files and 22 JavaScript/TypeScript files; static XML analysis found 347 record/template/menu identifiers.
- **Evidence:** `addons/product/security/product_security.xml:4`, `addons/product/security/product_security.xml:12`, `addons/product/security/product_security.xml:16`, `addons/product/security/product_security.xml:20`, `addons/product/security/product_security.xml:28`, `addons/product/security/product_security.xml:32`, `addons/product/report/product_pricelist_report_templates.xml:4`, `addons/product/report/product_pricelist_report_templates.xml:136`, `addons/product/report/product_template_templates.xml:4`, `addons/product/report/product_template_templates.xml:12`, `addons/product/report/product_template_templates.xml:20`, `addons/product/report/product_reports.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/product/security/product_security.xml`, `addons/product/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/product/views/product_views.xml`, `addons/product/views/uom_views.xml`, `addons/product/views/product_template_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/product/report/product_reports.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 17 test files are present.
- **Evidence:** `addons/product/tests/test_product_pricelist.py`, `addons/product/tests/test_import_files.py`, `addons/product/tests/test_pricelist_auto_creation.py`, `addons/product/tests/test_name.py`, `addons/product/tests/test_common.py`, `addons/product/tests/test_product_rounding.py`, `addons/product/tests/common.py`, `addons/product/tests/test_product_attribute_value_config.py`, `addons/product/tests/test_pricelist_report.py`, `addons/product/tests/test_barcode.py`, `addons/product/tests/test_pricelist.py`, `addons/product/tests/test_seller.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 44; representative identifiers: `res_groups_privilege_product`, `group_product_pricelist`, `group_product_variant`, `group_product_manager`, `base.user_admin`, `group_show_uom_price`, `report_pricelist_page`, `report_pricelist`, `report_product_label_pdf`, `report_product_label_dymo`, `report_product_label_zpl`, `paperformat_label_sheet`, `action_report_product_label_pdf`, `action_report_pricelist`, `paperformat_label_sheet_dymo`, `action_report_product_label_dymo`, `report_product_template_label_zpl`, `report_label_contour_marks`, `report_label_barcode`, `report_label_value_block`
- Menus: 0; representative evidence: Not found in module
- Templates: 27; representative evidence: `addons/product/report/product_pricelist_report_templates.xml:4`, `addons/product/report/product_pricelist_report_templates.xml:136`, `addons/product/report/product_template_templates.xml:4`, `addons/product/report/product_template_templates.xml:12`, `addons/product/report/product_template_templates.xml:20`, `addons/product/report/product_product_templates.xml:4`, `addons/product/report/product_product_templates.xml:23`, `addons/product/report/product_product_templates.xml:37`, `addons/product/report/product_product_templates.xml:48`, `addons/product/report/product_product_templates.xml:88`, `addons/product/report/product_product_templates.xml:130`, `addons/product/report/product_product_templates.xml:172`
- View/action field declarations: 159; representative evidence: `addons/product/report/product_reports.xml:20`, `addons/product/report/product_reports.xml:31`, `addons/product/report/product_reports.xml:53`, `addons/product/report/product_reports.xml:64`, `addons/product/wizard/update_product_attribute_value_views.xml:6`, `addons/product/wizard/update_product_attribute_value_views.xml:7`, `addons/product/wizard/product_label_layout_views.xml:5`, `addons/product/wizard/product_label_layout_views.xml:7`, `addons/product/wizard/product_label_layout_views.xml:43`, `addons/product/data/product_document_demo.xml:8`, `addons/product/data/product_document_demo.xml:16`, `addons/product/views/product_document_views.xml:6`
- Browser assets: 22; representative files: `addons/product/static/tests/product_combo_test_helpers.js`, `addons/product/static/tests/product_test_helpers.js`, `addons/product/static/tests/product_pricelist_report.test.js`, `addons/product/static/src/js/product_attribute_value_list.js`, `addons/product/static/src/product_catalog/kanban_model.js`, `addons/product/static/src/product_catalog/kanban_renderer.js`, `addons/product/static/src/product_catalog/kanban_record.js`, `addons/product/static/src/product_catalog/kanban_view.js`, `addons/product/static/src/product_catalog/product_catalog_search_panel.js`, `addons/product/static/src/product_catalog/kanban_controller.js`, `addons/product/static/src/js/daily_rates_calendar/daily_rates_calendar.js`, `addons/product/static/src/js/product_document_kanban/product_document_kanban_view.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/product/__manifest__.py`
- **HTTP entry points:** `addons/product/controllers/product_document.py:14`, `addons/product/controllers/pricelist_report.py:13`, `addons/product/controllers/catalog.py:7`, `addons/product/controllers/catalog.py:36`
- **Scheduled entry points:** `addons/product/views/product_views.xml`, `addons/product/views/uom_views.xml`, `addons/product/views/product_template_views.xml`
- **Report entry points:** `addons/product/report/product_reports.xml`

## 7. Database interactions

- Model declarations: 34
- Representative model evidence: `product.category` (addons/product/models/product_category.py:8); inherits `res.partner` (addons/product/models/res_partner.py:6); `product.product` (addons/product/models/product_product.py:15); `product.combo` (addons/product/models/product_combo.py:8); `product.attribute` (addons/product/models/product_attribute.py:7); inherits `uom.uom` (addons/product/models/uom_uom.py:8); `product.template` (addons/product/models/product_template.py:19); `product.catalog.mixin` (addons/product/models/product_catalog_mixin.py:8); inherits `res.groups` (addons/product/models/res_groups.py:6); `product.attribute.value` (addons/product/models/product_attribute_value.py:9); `product.uom` (addons/product/models/product_uom.py:8); inherits `res.config.settings` (addons/product/models/res_config_settings.py:6); `product.combo.item` (addons/product/models/product_combo_item.py:7); inherits `res.currency` (addons/product/models/res_currency.py:7); `product.pricelist` (addons/product/models/product_pricelist.py:10); `product.template.attribute.value` (addons/product/models/product_template_attribute_value.py:11); `product.template.attribute.line` (addons/product/models/product_template_attribute_line.py:8); `product.pricelist.item` (addons/product/models/product_pricelist_item.py:9); `product.document` (addons/product/models/product_document.py:8); `product.supplierinfo` (addons/product/models/product_supplierinfo.py:8); `product.base.unit` (addons/product/models/product_base_unit.py:4); `product.attribute.custom.value` (addons/product/models/product_attribute_custom_value.py:6); inherits `res.country.group` (addons/product/models/res_country_group.py:7); `product.catalog.line.mixin` (addons/product/models/product_catalog_line_mixin.py:6); `product.tag` (addons/product/models/product_tag.py:7); inherits `ir.attachment` (addons/product/models/ir_attachment.py:6); inherits `res.company` (addons/product/models/res_company.py:6); `report.product.report_pricelist` (addons/product/report/product_pricelist_report.py:7); `report.product.label.base` (addons/product/report/product_label_report.py:9); `report.product.report_product_label_pdf` (addons/product/report/product_label_report.py:79)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 4
- Route declarations: 4
- Route evidence: `addons/product/controllers/product_document.py:14`, `addons/product/controllers/pricelist_report.py:13`, `addons/product/controllers/catalog.py:7`, `addons/product/controllers/catalog.py:36`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `mail`, `uom`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/product/__init__.py`
- `addons/product/__manifest__.py`
- `addons/product/controllers/__init__.py`
- `addons/product/controllers/catalog.py`
- `addons/product/controllers/pricelist_report.py`
- `addons/product/controllers/product_document.py`
- `addons/product/data/product_attribute_data.xml`
- `addons/product/data/product_attribute_demo.xml`
- `addons/product/data/product_category_demo.xml`
- `addons/product/data/product_data.xml`
- `addons/product/data/product_demo.xml`
- `addons/product/data/product_document_demo.xml`
- `addons/product/data/product_supplierinfo_demo.xml`
- `addons/product/i18n/af.po`
- `addons/product/i18n/am.po`
- `addons/product/i18n/ar.po`
- `addons/product/i18n/az.po`
- `addons/product/i18n/bg.po`
- `addons/product/i18n/bs.po`
- `addons/product/i18n/ca.po`
- `addons/product/i18n/cs.po`
- `addons/product/i18n/da.po`
- `addons/product/i18n/de.po`
- `addons/product/i18n/el.po`
- `addons/product/i18n/es.po`
- `addons/product/i18n/es_419.po`
- `addons/product/i18n/es_CL.po`
- `addons/product/i18n/et.po`
- `addons/product/i18n/eu.po`
- `addons/product/i18n/fa.po`
- `addons/product/i18n/fi.po`
- `addons/product/i18n/fr.po`
- `addons/product/i18n/gl.po`
- `addons/product/i18n/gu.po`
- `addons/product/i18n/he.po`
- `addons/product/i18n/hi.po`
- `addons/product/i18n/hr.po`
- `addons/product/i18n/hu.po`
- `addons/product/i18n/id.po`
- `addons/product/i18n/is.po`
- `addons/product/i18n/it.po`
- `addons/product/i18n/ja.po`
- `addons/product/i18n/kab.po`
- `addons/product/i18n/km.po`
- `addons/product/i18n/ko.po`
- `addons/product/i18n/ku.po`
- `addons/product/i18n/lb.po`
- `addons/product/i18n/lo.po`
- `addons/product/i18n/lt.po`
- `addons/product/i18n/lv.po`
- `addons/product/i18n/mk.po`
- `addons/product/i18n/mn.po`
- `addons/product/i18n/my.po`
- `addons/product/i18n/nb.po`
- `addons/product/i18n/nl.po`
- `addons/product/i18n/pl.po`
- `addons/product/i18n/product.pot`
- `addons/product/i18n/pt.po`
- `addons/product/i18n/pt_BR.po`
- `addons/product/i18n/ro.po`
- `addons/product/i18n/ru.po`
- `addons/product/i18n/sk.po`
- `addons/product/i18n/sl.po`
- `addons/product/i18n/sr@latin.po`
- `addons/product/i18n/sv.po`
- `addons/product/i18n/th.po`
- `addons/product/i18n/tr.po`
- `addons/product/i18n/uk.po`
- `addons/product/i18n/uz.po`
- `addons/product/i18n/vi.po`
- `addons/product/i18n/zh_CN.po`
- `addons/product/i18n/zh_TW.po`
- `addons/product/models/__init__.py`
- `addons/product/models/ir_attachment.py`
- `addons/product/models/product_attribute.py`
- `addons/product/models/product_attribute_custom_value.py`
- `addons/product/models/product_attribute_value.py`
- `addons/product/models/product_base_unit.py`
- `addons/product/models/product_catalog_line_mixin.py`
- `addons/product/models/product_catalog_mixin.py`
- `addons/product/models/product_category.py`
- `addons/product/models/product_combo.py`
- `addons/product/models/product_combo_item.py`
- `addons/product/models/product_document.py`
- `addons/product/models/product_pricelist.py`
- `addons/product/models/product_pricelist_item.py`
- `addons/product/models/product_product.py`
- `addons/product/models/product_supplierinfo.py`
- `addons/product/models/product_tag.py`
- `addons/product/models/product_template.py`
- `addons/product/models/product_template_attribute_line.py`
- `addons/product/models/product_template_attribute_value.py`
- `addons/product/models/product_uom.py`
- `addons/product/models/res_company.py`
- `addons/product/models/res_config_settings.py`
- `addons/product/models/res_country_group.py`
- `addons/product/models/res_currency.py`
- `addons/product/models/res_groups.py`
- `addons/product/models/res_partner.py`
- `addons/product/models/uom_uom.py`
- `addons/product/populate/benchmarks.xml`
- `addons/product/populate/common.xml`
- `addons/product/populate/config_parameter.xml`
- `addons/product/populate/populate_demo.xml`
- `addons/product/report/__init__.py`
- `addons/product/report/product_label_report.py`
- `addons/product/report/product_pricelist_report.py`
- `addons/product/report/product_pricelist_report_templates.xml`
- `addons/product/report/product_product_templates.xml`
- `addons/product/report/product_reports.xml`
- `addons/product/report/product_template_templates.xml`
- `addons/product/security/ir.access.csv`
- `addons/product/security/product_security.xml`
- `addons/product/static/demo/acoustic_bloc_screen_document.pdf`
- `addons/product/static/demo/customizable_desk_document.pdf`
- `addons/product/static/description/icon.png`
- `addons/product/static/description/icon.svg`
- `addons/product/static/description/icon_hi.png`
- `addons/product/static/img/desk_organizer.jpg`
- `addons/product/static/img/desk_pad.jpg`
- `addons/product/static/img/dining_table.png`
- `addons/product/static/img/glass.png`
- `addons/product/static/img/leather.png`
- `addons/product/static/img/linen.png`
- `addons/product/static/img/maroon.png`
- `addons/product/static/img/membership_0-image.jpg`
- `addons/product/static/img/membership_1-image.jpg`
- `addons/product/static/img/membership_2-image.jpg`
- `addons/product/static/img/metal.png`
- `addons/product/static/img/monitor_stand.jpg`
- `addons/product/static/img/office_combo.jpg`
- `addons/product/static/img/placeholder.png`
- `addons/product/static/img/placeholder_thumbnail.png`
- `addons/product/static/img/product_chair.jpg`
- `addons/product/static/img/product_lamp.png`
- `addons/product/static/img/product_product_10-image.jpg`
- `addons/product/static/img/product_product_11-image.jpg`
- `addons/product/static/img/product_product_11b-image.jpg`
- `addons/product/static/img/product_product_12-image.jpg`
- `addons/product/static/img/product_product_13-image.jpg`
- `addons/product/static/img/product_product_16-image.jpg`
- `addons/product/static/img/product_product_20-image.png`
- `addons/product/static/img/product_product_22-image.png`
- `addons/product/static/img/product_product_24-image.jpg`
- `addons/product/static/img/product_product_25-image.jpg`
- `addons/product/static/img/product_product_25_black-image.jpg`
- `addons/product/static/img/product_product_27-image.jpg`
- `addons/product/static/img/product_product_3-image.jpg`
- `addons/product/static/img/product_product_43-image.jpg`
- `addons/product/static/img/product_product_46-image.jpg`
- `addons/product/static/img/product_product_5-image.jpg`
- `addons/product/static/img/product_product_6-image.jpg`
- `addons/product/static/img/product_product_7-image.png`
- `addons/product/static/img/product_product_8-image.jpg`
- `addons/product/static/img/product_product_8_glass-image.jpg`
- `addons/product/static/img/product_product_8_metal-image.jpg`
- `addons/product/static/img/product_product_9-image.jpg`
- `addons/product/static/img/product_product_d01-image.jpg`
- `addons/product/static/img/product_product_d01b-image.jpg`
- `addons/product/static/img/product_product_d01c-image.jpg`
- `addons/product/static/img/product_product_d03-image.png`
- `addons/product/static/img/purple.png`
- `addons/product/static/img/table02.jpg`
- `addons/product/static/img/table03.jpg`
- `addons/product/static/img/table04.jpg`
- `addons/product/static/img/velvet.png`
- `addons/product/static/img/wood.png`
- `addons/product/static/img/zpl_label_placeholder.png`
- `addons/product/static/src/js/daily_rates_calendar/daily_rates_calendar.js`
- `addons/product/static/src/js/daily_rates_calendar/daily_rates_calendar.scss`
- `addons/product/static/src/js/pricelist_report/product_pricelist_report.js`
- `addons/product/static/src/js/pricelist_report/product_pricelist_report.xml`
- `addons/product/static/src/js/product_attribute_value_list.js`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_controller.js`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_controller.xml`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_record.js`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_renderer.js`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_renderer.xml`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_view.js`
- `addons/product/static/src/js/product_document_kanban/product_document_kanban_view.scss`
- `addons/product/static/src/js/product_document_kanban/upload_button/upload_button.js`
- `addons/product/static/src/js/product_document_kanban/upload_button/upload_button.xml`
- `addons/product/static/src/product_catalog/kanban_controller.js`
- `addons/product/static/src/product_catalog/kanban_controller.xml`
- `addons/product/static/src/product_catalog/kanban_model.js`
- `addons/product/static/src/product_catalog/kanban_record.js`
- `addons/product/static/src/product_catalog/kanban_record.scss`
- `addons/product/static/src/product_catalog/kanban_record.xml`
- `addons/product/static/src/product_catalog/kanban_renderer.js`
- `addons/product/static/src/product_catalog/kanban_renderer.xml`
- `addons/product/static/src/product_catalog/kanban_view.js`
- `addons/product/static/src/product_catalog/order_line/order_line.js`
- `addons/product/static/src/product_catalog/order_line/order_line.scss`
- `addons/product/static/src/product_catalog/order_line/order_line.xml`
- `addons/product/static/src/product_catalog/product_catalog_search_panel.js`
- `addons/product/static/src/product_catalog/product_catalog_search_panel.scss`
- `addons/product/static/src/product_catalog/product_catalog_search_panel.xml`
- `addons/product/static/src/scss/product_template_views.scss`
- `addons/product/static/src/scss/report_label_sheet.scss`
- `addons/product/static/tests/mock_server/mock_models/product_combo.js`
- `addons/product/static/tests/mock_server/mock_models/product_product.js`
- `addons/product/static/tests/mock_server/mock_models/product_template.js`
- `addons/product/static/tests/mock_server/mock_models/uom_uom.js`
- `addons/product/static/tests/product_combo_test_helpers.js`
- `addons/product/static/tests/product_pricelist_report.test.js`
- `addons/product/static/tests/product_test_helpers.js`
- `addons/product/static/xls/product_category.xls`
- `addons/product/static/xls/product_pricelist.xls`
- `addons/product/static/xls/product_product.xls`
- `addons/product/static/xls/product_supplierinfo.xls`
- `addons/product/static/xls/product_template.xls`
- `addons/product/static/xls/products_import_template.xlsx`
- `addons/product/static/xls/test_import_product_without_values.xls`
- `addons/product/static/xls/test_import_product_without_values_stock.xls`
- `addons/product/static/xls/test_import_template.xls`
- `addons/product/static/xls/test_import_update_error.xls`
- `addons/product/static/xls/test_import_update_error_2.xls`
- `addons/product/static/xls/test_import_update_product_price.xls`
- `addons/product/tests/__init__.py`
- `addons/product/tests/common.py`
- `addons/product/tests/test_barcode.py`
- `addons/product/tests/test_common.py`
- `addons/product/tests/test_import_files.py`
- `addons/product/tests/test_name.py`
- `addons/product/tests/test_pricelist.py`
- `addons/product/tests/test_pricelist_auto_creation.py`
- `addons/product/tests/test_pricelist_report.py`
- `addons/product/tests/test_product_attribute_value_config.py`
- `addons/product/tests/test_product_combo.py`
- `addons/product/tests/test_product_document.py`
- `addons/product/tests/test_product_pricelist.py`
- `addons/product/tests/test_product_rounding.py`
- `addons/product/tests/test_seller.py`
- `addons/product/tests/test_update_pav_wizard.py`
- `addons/product/tests/test_variants.py`
- `addons/product/views/product_attribute_value_views.xml`
- `addons/product/views/product_attribute_views.xml`
- `addons/product/views/product_base_unit_views.xml`
- `addons/product/views/product_category_views.xml`
- `addons/product/views/product_combo_views.xml`
- `addons/product/views/product_document_views.xml`
- `addons/product/views/product_pricelist_item_views.xml`
- `addons/product/views/product_pricelist_views.xml`
- `addons/product/views/product_supplierinfo_views.xml`
- `addons/product/views/product_tag_views.xml`
- `addons/product/views/product_template_attribute_line_views.xml`
- `addons/product/views/product_template_views.xml`
- `addons/product/views/product_views.xml`
- `addons/product/views/res_config_settings_views.xml`
- `addons/product/views/res_country_group_views.xml`
- Additional source files not expanded in this page: 7; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
