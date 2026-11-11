# Module: sale_pdf_quote_builder

- **Module ID:** MOD-522
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_pdf_quote_builder`
- **Manifest:** `addons/sale_pdf_quote_builder/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Build nice quotations

**Scope evidence:** The module contains 96 files, including 16 Python, 14 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `sale_management`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 2
- XML/data/view/template files: 14
- Browser asset files: 6
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 3
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_pdf_quote_builder/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 47 methods, 4 constraint handlers, 2 onchange handlers, and 5 dependency declarations.
- **Evidence:** `addons/sale_pdf_quote_builder/models/sale_order.py:8`, `addons/sale_pdf_quote_builder/models/quotation_document.py:8`, `addons/sale_pdf_quote_builder/models/ir_actions_report.py:18`, `addons/sale_pdf_quote_builder/models/sale_pdf_form_field.py:12`, `addons/sale_pdf_quote_builder/models/product_document.py:7`, `addons/sale_pdf_quote_builder/models/sale_order_template.py:6`, `addons/sale_pdf_quote_builder/models/sale_order_line.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/sale_pdf_quote_builder/controllers/quotation_document.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 6 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/sale_pdf_quote_builder/wizards/res_config_settings_views.xml:4`, `addons/sale_pdf_quote_builder/report/ir_actions_report.xml:4`, `addons/sale_pdf_quote_builder/report/ir_actions_report.xml:14`, `addons/sale_pdf_quote_builder/data/ir_cron.xml:4`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:4`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:12`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:20`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:28`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:36`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:44`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:53`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:57`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_pdf_quote_builder/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/sale_pdf_quote_builder/__manifest__.py`, `addons/sale_pdf_quote_builder/models/sale_pdf_form_field.py`, `addons/sale_pdf_quote_builder/data/ir_cron.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/sale_pdf_quote_builder/models/ir_actions_report.py`, `addons/sale_pdf_quote_builder/report/ir_actions_report.xml`, `addons/sale_pdf_quote_builder/tests/test_pdf_quote_builder.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/sale_pdf_quote_builder/tests/test_controllers.py`, `addons/sale_pdf_quote_builder/tests/test_pdf_quote_builder.py`, `addons/sale_pdf_quote_builder/tests/__init__.py`, `addons/sale_pdf_quote_builder/tests/files/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `res_config_settings_view_form`, `action_report_saleorder_raw`, `sale.action_report_saleorder`, `cron_post_upgrade_assign_missing_form_fields`, `sale_pdf_header_demo_page`, `sale_pdf_header_about_us_demo_page`, `sale_pdf_header_project_description_demo_page`, `sale_pdf_footer_testimonials_demo_page`, `sale_pdf_footer_terms_demo_page`, `consu_delivery_02_document`, `product.product_product_4_product_template_document`, `product.product_product_25_document`, `sale_management.sale_order_template_1`, `product_document_form`, `quotation_document_form`, `quotation_document_kanban`, `quotation_document_list`, `quotation_document_search_view`, `quotation_document_action`, `Headers/Footers`
- Menus: 1; representative evidence: `addons/sale_pdf_quote_builder/views/sale_pdf_quote_builder_menus.xml:4`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 24; representative evidence: `addons/sale_pdf_quote_builder/wizards/res_config_settings_views.xml:6`, `addons/sale_pdf_quote_builder/wizards/res_config_settings_views.xml:8`, `addons/sale_pdf_quote_builder/report/ir_actions_report.xml:6`, `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml:48`, `addons/sale_pdf_quote_builder/views/product_document_views.xml:6`, `addons/sale_pdf_quote_builder/views/product_document_views.xml:8`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:6`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:7`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:74`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:75`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:121`, `addons/sale_pdf_quote_builder/views/quotation_document_views.xml:122`
- Browser assets: 6; representative files: `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_widget.js`, `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_view.js`, `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_controller.js`, `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_content_kanban_like_widget.js`, `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_field_card/custom_field_card.js`, `addons/sale_pdf_quote_builder/static/tests/tours/custom_content_kanban_like_tests.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_pdf_quote_builder/__manifest__.py`
- **HTTP entry points:** `addons/sale_pdf_quote_builder/controllers/quotation_document.py:15`
- **Scheduled entry points:** `addons/sale_pdf_quote_builder/__manifest__.py`, `addons/sale_pdf_quote_builder/models/sale_pdf_form_field.py`, `addons/sale_pdf_quote_builder/data/ir_cron.xml`
- **Report entry points:** `addons/sale_pdf_quote_builder/models/ir_actions_report.py`, `addons/sale_pdf_quote_builder/report/ir_actions_report.xml`, `addons/sale_pdf_quote_builder/tests/test_pdf_quote_builder.py`

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `sale.order` (addons/sale_pdf_quote_builder/models/sale_order.py:8); `quotation.document` (addons/sale_pdf_quote_builder/models/quotation_document.py:8); inherits `ir.actions.report` (addons/sale_pdf_quote_builder/models/ir_actions_report.py:18); `sale.pdf.form.field` (addons/sale_pdf_quote_builder/models/sale_pdf_form_field.py:12); inherits `product.document` (addons/sale_pdf_quote_builder/models/product_document.py:7); inherits `sale.order.template` (addons/sale_pdf_quote_builder/models/sale_order_template.py:6); inherits `sale.order.line` (addons/sale_pdf_quote_builder/models/sale_order_line.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/sale_pdf_quote_builder/controllers/quotation_document.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_management`
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

- `addons/sale_pdf_quote_builder/__init__.py`
- `addons/sale_pdf_quote_builder/__manifest__.py`
- `addons/sale_pdf_quote_builder/controllers/__init__.py`
- `addons/sale_pdf_quote_builder/controllers/quotation_document.py`
- `addons/sale_pdf_quote_builder/data/ir_cron.xml`
- `addons/sale_pdf_quote_builder/data/sale_pdf_form_field.xml`
- `addons/sale_pdf_quote_builder/data/sale_pdf_quote_builder_demo.xml`
- `addons/sale_pdf_quote_builder/i18n/ar.po`
- `addons/sale_pdf_quote_builder/i18n/az.po`
- `addons/sale_pdf_quote_builder/i18n/bg.po`
- `addons/sale_pdf_quote_builder/i18n/bs.po`
- `addons/sale_pdf_quote_builder/i18n/ca.po`
- `addons/sale_pdf_quote_builder/i18n/cs.po`
- `addons/sale_pdf_quote_builder/i18n/da.po`
- `addons/sale_pdf_quote_builder/i18n/de.po`
- `addons/sale_pdf_quote_builder/i18n/el.po`
- `addons/sale_pdf_quote_builder/i18n/es.po`
- `addons/sale_pdf_quote_builder/i18n/es_419.po`
- `addons/sale_pdf_quote_builder/i18n/et.po`
- `addons/sale_pdf_quote_builder/i18n/fa.po`
- `addons/sale_pdf_quote_builder/i18n/fi.po`
- `addons/sale_pdf_quote_builder/i18n/fr.po`
- `addons/sale_pdf_quote_builder/i18n/he.po`
- `addons/sale_pdf_quote_builder/i18n/hi.po`
- `addons/sale_pdf_quote_builder/i18n/hr.po`
- `addons/sale_pdf_quote_builder/i18n/hu.po`
- `addons/sale_pdf_quote_builder/i18n/id.po`
- `addons/sale_pdf_quote_builder/i18n/it.po`
- `addons/sale_pdf_quote_builder/i18n/ja.po`
- `addons/sale_pdf_quote_builder/i18n/kab.po`
- `addons/sale_pdf_quote_builder/i18n/ko.po`
- `addons/sale_pdf_quote_builder/i18n/ku.po`
- `addons/sale_pdf_quote_builder/i18n/lo.po`
- `addons/sale_pdf_quote_builder/i18n/lt.po`
- `addons/sale_pdf_quote_builder/i18n/lv.po`
- `addons/sale_pdf_quote_builder/i18n/mn.po`
- `addons/sale_pdf_quote_builder/i18n/my.po`
- `addons/sale_pdf_quote_builder/i18n/nb.po`
- `addons/sale_pdf_quote_builder/i18n/nl.po`
- `addons/sale_pdf_quote_builder/i18n/pl.po`
- `addons/sale_pdf_quote_builder/i18n/pt.po`
- `addons/sale_pdf_quote_builder/i18n/pt_BR.po`
- `addons/sale_pdf_quote_builder/i18n/ro.po`
- `addons/sale_pdf_quote_builder/i18n/ru.po`
- `addons/sale_pdf_quote_builder/i18n/sale_pdf_quote_builder.pot`
- `addons/sale_pdf_quote_builder/i18n/sk.po`
- `addons/sale_pdf_quote_builder/i18n/sl.po`
- `addons/sale_pdf_quote_builder/i18n/sr@latin.po`
- `addons/sale_pdf_quote_builder/i18n/sv.po`
- `addons/sale_pdf_quote_builder/i18n/th.po`
- `addons/sale_pdf_quote_builder/i18n/tr.po`
- `addons/sale_pdf_quote_builder/i18n/uk.po`
- `addons/sale_pdf_quote_builder/i18n/uz.po`
- `addons/sale_pdf_quote_builder/i18n/vi.po`
- `addons/sale_pdf_quote_builder/i18n/zh_CN.po`
- `addons/sale_pdf_quote_builder/i18n/zh_TW.po`
- `addons/sale_pdf_quote_builder/models/__init__.py`
- `addons/sale_pdf_quote_builder/models/ir_actions_report.py`
- `addons/sale_pdf_quote_builder/models/product_document.py`
- `addons/sale_pdf_quote_builder/models/quotation_document.py`
- `addons/sale_pdf_quote_builder/models/sale_order.py`
- `addons/sale_pdf_quote_builder/models/sale_order_line.py`
- `addons/sale_pdf_quote_builder/models/sale_order_template.py`
- `addons/sale_pdf_quote_builder/models/sale_pdf_form_field.py`
- `addons/sale_pdf_quote_builder/report/ir_actions_report.xml`
- `addons/sale_pdf_quote_builder/security/ir.access.csv`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/large_meeting_table_with_form_fields.pdf`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/quote_footer_terms.pdf`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/quote_footer_testimonials.pdf`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/quote_header.pdf`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/quote_header_about_us.pdf`
- `addons/sale_pdf_quote_builder/static/quote_builder_pdf/quote_header_project_description.pdf`
- `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_content_kanban_like_widget.js`
- `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_content_kanban_like_widget.xml`
- `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_field_card/custom_field_card.js`
- `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_field_card/custom_field_card.scss`
- `addons/sale_pdf_quote_builder/static/src/js/custom_content_kanban_like_widget/custom_field_card/custom_field_card.xml`
- `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_controller.js`
- `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_view.js`
- `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_widget.js`
- `addons/sale_pdf_quote_builder/static/src/js/quotation_document_kanban/quotation_document_kanban_widget.xml`
- `addons/sale_pdf_quote_builder/static/tests/tours/custom_content_kanban_like_tests.js`
- `addons/sale_pdf_quote_builder/tests/__init__.py`
- `addons/sale_pdf_quote_builder/tests/files/__init__.py`
- `addons/sale_pdf_quote_builder/tests/files/test_AES.pdf`
- `addons/sale_pdf_quote_builder/tests/files/test_forms.pdf`
- `addons/sale_pdf_quote_builder/tests/files/test_plain.pdf`
- `addons/sale_pdf_quote_builder/tests/test_controllers.py`
- `addons/sale_pdf_quote_builder/tests/test_pdf_quote_builder.py`
- `addons/sale_pdf_quote_builder/views/product_document_views.xml`
- `addons/sale_pdf_quote_builder/views/quotation_document_views.xml`
- `addons/sale_pdf_quote_builder/views/sale_order_template_views.xml`
- `addons/sale_pdf_quote_builder/views/sale_order_views.xml`
- `addons/sale_pdf_quote_builder/views/sale_pdf_form_field_views.xml`
- `addons/sale_pdf_quote_builder/views/sale_pdf_quote_builder_menus.xml`
- `addons/sale_pdf_quote_builder/wizards/res_config_settings_views.xml`
