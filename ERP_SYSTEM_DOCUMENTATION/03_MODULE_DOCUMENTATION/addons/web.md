# Module: web

- **Module ID:** MOD-592
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/web`
- **Manifest:** `addons/web/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Odoo Web core module.
========================

This module provides the core of the Odoo Web Client.

**Scope evidence:** The module contains 2430 files, including 70 Python, 287 XML, and 1083 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 16
- Controller/API files: 20
- XML/data/view/template files: 287
- Browser asset files: 1083
- Security files: 1
- Test files: 31
- Scheduled/automation evidence files: 5
- Reporting evidence files: 3

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/web/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 16 model declarations, 394 methods, 2 constraint handlers, 4 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/web/models/res_partner.py:40`, `addons/web/models/ir_ui_view.py:6`, `addons/web/models/base_document_layout.py:19`, `addons/web/models/res_config_settings.py:7`, `addons/web/models/ir_model.py:7`, `addons/web/models/res_users_settings.py:4`, `addons/web/models/ir_http.py:11`, `addons/web/models/ir_qweb_fields.py:14`, `addons/web/models/ir_qweb_fields.py:161`, `addons/web/models/properties_base_definition.py:5`, `addons/web/models/res_users.py:10`, `addons/web/models/models.py:42`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 20 controller files and 73 route declarations.
- **Evidence:** `addons/web/controllers/json.py:31`, `addons/web/controllers/json.py:39`, `addons/web/controllers/export.py:309`, `addons/web/controllers/export.py:326`, `addons/web/controllers/export.py:404`, `addons/web/controllers/export.py:533`, `addons/web/controllers/export.py:582`, `addons/web/controllers/action.py:22`, `addons/web/controllers/action.py:51`, `addons/web/controllers/action.py:59`, `addons/web/controllers/profiling.py:14`, `addons/web/controllers/profiling.py:27`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 287 XML files and 1083 JavaScript/TypeScript files; static XML analysis found 60 record/template/menu identifiers.
- **Evidence:** `addons/web/data/ir_attachment.xml:3`, `addons/web/data/report_layout.xml:5`, `addons/web/data/report_layout.xml:11`, `addons/web/data/report_layout.xml:17`, `addons/web/data/report_layout.xml:23`, `addons/web/data/report_layout.xml:30`, `addons/web/data/report_layout.xml:36`, `addons/web/data/report_layout.xml:42`, `addons/web/data/report_layout.xml:48`, `addons/web/data/report_layout.xml:54`, `addons/web/views/neutralize_views.xml:3`, `addons/web/views/report_templates.xml:1081`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/web/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/web/controllers/action.py`, `addons/web/views/partner_view.xml`, `addons/web/tests/test_router.py`, `addons/web/tests/test_health.py`, `addons/web/tests/test_action.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 3 files contain report-action/template indicators.
- **Evidence:** `addons/web/controllers/report.py`, `addons/web/views/report_templates.xml`, `addons/web/tests/test_reports.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 31 test files are present.
- **Evidence:** `addons/web/tests/test_router.py`, `addons/web/tests/test_res_users_settings.py`, `addons/web/tests/test_login.py`, `addons/web/tests/test_ir_model.py`, `addons/web/tests/test_domain.py`, `addons/web/tests/test_assets.py`, `addons/web/tests/test_pivot_export.py`, `addons/web/tests/test_base_document_layout.py`, `addons/web/tests/test_res_users.py`, `addons/web/tests/test_favorite.py`, `addons/web/tests/test_perf_load_menu.py`, `addons/web/tests/test_web_unlink.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 287; representative identifiers: `image_placeholder`, `report_layout_standard`, `report_layout_bubble`, `report_layout_wave`, `report_layout_folder`, `report_layout_center`, `report_layout_dual`, `report_layout_lines`, `report_layout_compact`, `asset_styles_company_report`, `Neutralize Banner`, `action_report_internalpreview`, `action_report_externalpreview`, `action_report_layout_preview`, `Report layout`, `Report layout`, `html_container`, `html_preview_container`, `report_invoice_wizard_preview`, `minimal_layout`
- Menus: 0; representative evidence: Not found in module
- Templates: 43; representative evidence: `addons/web/views/neutralize_views.xml:3`, `addons/web/views/report_templates.xml:6`, `addons/web/views/report_templates.xml:39`, `addons/web/views/report_templates.xml:93`, `addons/web/views/report_templates.xml:100`, `addons/web/views/report_templates.xml:107`, `addons/web/views/report_templates.xml:287`, `addons/web/views/report_templates.xml:336`, `addons/web/views/report_templates.xml:369`, `addons/web/views/report_templates.xml:400`, `addons/web/views/report_templates.xml:443`, `addons/web/views/report_templates.xml:473`
- View/action field declarations: 9; representative evidence: `addons/web/views/report_templates.xml:1083`, `addons/web/views/report_templates.xml:1091`, `addons/web/views/report_templates.xml:1099`, `addons/web/views/ir_ui_view_views.xml:5`, `addons/web/views/ir_ui_view_views.xml:7`, `addons/web/views/base_document_layout_views.xml:6`, `addons/web/views/base_document_layout_views.xml:7`, `addons/web/views/base_document_layout_views.xml:49`, `addons/web/views/base_document_layout_views.xml:51`
- Browser assets: 1083; representative files: `addons/web/static/src/service_worker.js`, `addons/web/static/src/main.js`, `addons/web/static/src/env.js`, `addons/web/static/src/start.js`, `addons/web/static/src/session.js`, `addons/web/static/src/module_loader.js`, `addons/web/static/tests/env.test.js`, `addons/web/static/tests/t_custom_click.test.js`, `addons/web/static/tests/web_test_helpers.js`, `addons/web/static/tests/reactivity.test.js`, `addons/web/static/lib/chartjs-adapter-luxon/chartjs-adapter-luxon.js`, `addons/web/static/lib/zxing-library/zxing-library.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/web/__manifest__.py`
- **HTTP entry points:** `addons/web/controllers/json.py:31`, `addons/web/controllers/json.py:39`, `addons/web/controllers/export.py:309`, `addons/web/controllers/export.py:326`, `addons/web/controllers/export.py:404`, `addons/web/controllers/export.py:533`, `addons/web/controllers/export.py:582`, `addons/web/controllers/action.py:22`, `addons/web/controllers/action.py:51`, `addons/web/controllers/action.py:59`, `addons/web/controllers/profiling.py:14`, `addons/web/controllers/profiling.py:27`
- **Scheduled entry points:** `addons/web/controllers/action.py`, `addons/web/views/partner_view.xml`, `addons/web/tests/test_router.py`, `addons/web/tests/test_health.py`, `addons/web/tests/test_action.py`
- **Report entry points:** `addons/web/controllers/report.py`, `addons/web/views/report_templates.xml`, `addons/web/tests/test_reports.py`

## 7. Database interactions

- Model declarations: 16
- Representative model evidence: inherits `res.partner` (addons/web/models/res_partner.py:40); inherits `ir.ui.view` (addons/web/models/ir_ui_view.py:6); `base.document.layout` (addons/web/models/base_document_layout.py:19); inherits `res.config.settings` (addons/web/models/res_config_settings.py:7); inherits `ir.model` (addons/web/models/ir_model.py:7); inherits `res.users.settings` (addons/web/models/res_users_settings.py:4); inherits `ir.http` (addons/web/models/ir_http.py:11); inherits `ir.qweb.field.image` (addons/web/models/ir_qweb_fields.py:14); inherits `ir.qweb.field.image_url` (addons/web/models/ir_qweb_fields.py:161); inherits `properties.base.definition` (addons/web/models/properties_base_definition.py:5); inherits `res.users` (addons/web/models/res_users.py:10); inherits `base` (addons/web/models/models.py:42); inherits `res.company` (addons/web/models/models.py:2426); `res.users.settings.embedded.action` (addons/web/models/res_users_settings_embedded_action.py:5); inherits `ir.ui.menu` (addons/web/models/ir_ui_menu.py:9); inherits `ir.attachment` (addons/web/models/ir_attachment.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 20
- Route declarations: 73
- Route evidence: `addons/web/controllers/json.py:31`, `addons/web/controllers/json.py:39`, `addons/web/controllers/export.py:309`, `addons/web/controllers/export.py:326`, `addons/web/controllers/export.py:404`, `addons/web/controllers/export.py:533`, `addons/web/controllers/export.py:582`, `addons/web/controllers/action.py:22`, `addons/web/controllers/action.py:51`, `addons/web/controllers/action.py:59`, `addons/web/controllers/profiling.py:14`, `addons/web/controllers/profiling.py:27`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
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

- `addons/web/__init__.py`
- `addons/web/__manifest__.py`
- `addons/web/controllers/__init__.py`
- `addons/web/controllers/action.py`
- `addons/web/controllers/binary.py`
- `addons/web/controllers/database.py`
- `addons/web/controllers/dataset.py`
- `addons/web/controllers/domain.py`
- `addons/web/controllers/export.py`
- `addons/web/controllers/home.py`
- `addons/web/controllers/json.py`
- `addons/web/controllers/main.py`
- `addons/web/controllers/model.py`
- `addons/web/controllers/pivot.py`
- `addons/web/controllers/profiling.py`
- `addons/web/controllers/report.py`
- `addons/web/controllers/session.py`
- `addons/web/controllers/utils.py`
- `addons/web/controllers/vcard.py`
- `addons/web/controllers/view.py`
- `addons/web/controllers/webclient.py`
- `addons/web/controllers/webmanifest.py`
- `addons/web/data/ir_attachment.xml`
- `addons/web/data/neutralize.sql`
- `addons/web/data/report_layout.xml`
- `addons/web/i18n/af.po`
- `addons/web/i18n/ar.po`
- `addons/web/i18n/az.po`
- `addons/web/i18n/bg.po`
- `addons/web/i18n/bn.po`
- `addons/web/i18n/bs.po`
- `addons/web/i18n/ca.po`
- `addons/web/i18n/cs.po`
- `addons/web/i18n/da.po`
- `addons/web/i18n/de.po`
- `addons/web/i18n/el.po`
- `addons/web/i18n/es.po`
- `addons/web/i18n/es_419.po`
- `addons/web/i18n/es_CL.po`
- `addons/web/i18n/et.po`
- `addons/web/i18n/eu.po`
- `addons/web/i18n/fa.po`
- `addons/web/i18n/fi.po`
- `addons/web/i18n/fr.po`
- `addons/web/i18n/gl.po`
- `addons/web/i18n/gu.po`
- `addons/web/i18n/he.po`
- `addons/web/i18n/hi.po`
- `addons/web/i18n/hr.po`
- `addons/web/i18n/hu.po`
- `addons/web/i18n/id.po`
- `addons/web/i18n/is.po`
- `addons/web/i18n/it.po`
- `addons/web/i18n/ja.po`
- `addons/web/i18n/ka.po`
- `addons/web/i18n/kab.po`
- `addons/web/i18n/km.po`
- `addons/web/i18n/ko.po`
- `addons/web/i18n/ku.po`
- `addons/web/i18n/lo.po`
- `addons/web/i18n/lt.po`
- `addons/web/i18n/lv.po`
- `addons/web/i18n/mk.po`
- `addons/web/i18n/mn.po`
- `addons/web/i18n/my.po`
- `addons/web/i18n/nb.po`
- `addons/web/i18n/nl.po`
- `addons/web/i18n/pl.po`
- `addons/web/i18n/pt.po`
- `addons/web/i18n/pt_BR.po`
- `addons/web/i18n/ro.po`
- `addons/web/i18n/ru.po`
- `addons/web/i18n/sk.po`
- `addons/web/i18n/sl.po`
- `addons/web/i18n/sr@latin.po`
- `addons/web/i18n/sv.po`
- `addons/web/i18n/th.po`
- `addons/web/i18n/tr.po`
- `addons/web/i18n/uk.po`
- `addons/web/i18n/uz.po`
- `addons/web/i18n/vi.po`
- `addons/web/i18n/web.pot`
- `addons/web/i18n/zh_CN.po`
- `addons/web/i18n/zh_TW.po`
- `addons/web/icons.py`
- `addons/web/models/__init__.py`
- `addons/web/models/base_document_layout.py`
- `addons/web/models/ir_attachment.py`
- `addons/web/models/ir_http.py`
- `addons/web/models/ir_model.py`
- `addons/web/models/ir_qweb_fields.py`
- `addons/web/models/ir_ui_menu.py`
- `addons/web/models/ir_ui_view.py`
- `addons/web/models/models.py`
- `addons/web/models/properties_base_definition.py`
- `addons/web/models/res_config_settings.py`
- `addons/web/models/res_partner.py`
- `addons/web/models/res_users.py`
- `addons/web/models/res_users_settings.py`
- `addons/web/models/res_users_settings_embedded_action.py`
- `addons/web/security/ir.access.csv`
- `addons/web/static/fonts/fonts.scss`
- `addons/web/static/fonts/google/Fira_Mono/Fira_Mono-Bold.ttf`
- `addons/web/static/fonts/google/Fira_Mono/Fira_Mono-Medium.ttf`
- `addons/web/static/fonts/google/Fira_Mono/Fira_Mono-Regular.ttf`
- `addons/web/static/fonts/google/Fira_Mono/OFL.txt`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Black.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-BlackItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Bold.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-BoldItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-ExtraBold.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-ExtraBoldItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-ExtraLight.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-ExtraLightItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Italic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Light.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-LightItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Medium.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-MediumItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Regular.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-SemiBold.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-SemiBoldItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-Thin.ttf`
- `addons/web/static/fonts/google/Montserrat/Montserrat-ThinItalic.ttf`
- `addons/web/static/fonts/google/Montserrat/OFL.txt`
- `addons/web/static/fonts/google/Noto_Sans_Mono/Noto_Sans_Mono-Bold.woff`
- `addons/web/static/fonts/google/Noto_Sans_Mono/Noto_Sans_Mono-Medium.woff`
- `addons/web/static/fonts/google/Noto_Sans_Mono/Noto_Sans_Mono-Regular.woff`
- `addons/web/static/fonts/google/Noto_Sans_Mono/OFL.txt`
- `addons/web/static/fonts/google/Open_Sans/LICENSE.txt`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-Bold.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-BoldItalic.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-ExtraBold.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-ExtraBoldItalic.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-Italic.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-Light.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-LightItalic.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-Regular.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-SemiBold.ttf`
- `addons/web/static/fonts/google/Open_Sans/Open_Sans-SemiBoldItalic.ttf`
- `addons/web/static/fonts/google/Oswald/OFL.txt`
- `addons/web/static/fonts/google/Oswald/Oswald-Bold.ttf`
- `addons/web/static/fonts/google/Oswald/Oswald-ExtraLight.ttf`
- `addons/web/static/fonts/google/Oswald/Oswald-Light.ttf`
- `addons/web/static/fonts/google/Oswald/Oswald-Medium.ttf`
- `addons/web/static/fonts/google/Oswald/Oswald-Regular.ttf`
- `addons/web/static/fonts/google/Oswald/Oswald-SemiBold.ttf`
- `addons/web/static/fonts/google/Playball/OFL.txt`
- `addons/web/static/fonts/google/Playball/Playball-Regular.ttf`
- `addons/web/static/fonts/google/Raleway/OFL.txt`
- `addons/web/static/fonts/google/Raleway/Raleway-Black.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-BlackItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Bold.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-BoldItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-ExtraBold.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-ExtraBoldItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-ExtraLight.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-ExtraLightItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Italic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Light.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-LightItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Medium.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-MediumItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Regular.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-SemiBold.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-SemiBoldItalic.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-Thin.ttf`
- `addons/web/static/fonts/google/Raleway/Raleway-ThinItalic.ttf`
- `addons/web/static/fonts/google/Roboto/LICENSE.txt`
- `addons/web/static/fonts/google/Roboto/Roboto-Black.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-BlackItalic.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Bold.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-BoldItalic.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Italic.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Light.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-LightItalic.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Medium.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-MediumItalic.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Regular.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-Thin.ttf`
- `addons/web/static/fonts/google/Roboto/Roboto-ThinItalic.ttf`
- `addons/web/static/fonts/google/Roboto/roboto.b64`
- `addons/web/static/fonts/google/Tajawal/OFL.txt`
- `addons/web/static/fonts/google/Tajawal/Tajawal-Black.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-Bold.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-ExtraBold.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-ExtraLight.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-Light.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-Medium.ttf`
- `addons/web/static/fonts/google/Tajawal/Tajawal-Regular.ttf`
- `addons/web/static/fonts/lato/Lato-Bla-webfont.eot`
- `addons/web/static/fonts/lato/Lato-Bla-webfont.svg`
- `addons/web/static/fonts/lato/Lato-Bla-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-Bla-webfont.woff`
- `addons/web/static/fonts/lato/Lato-BlaIta-webfont.eot`
- `addons/web/static/fonts/lato/Lato-BlaIta-webfont.svg`
- `addons/web/static/fonts/lato/Lato-BlaIta-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-BlaIta-webfont.woff`
- `addons/web/static/fonts/lato/Lato-Bol-webfont.eot`
- `addons/web/static/fonts/lato/Lato-Bol-webfont.svg`
- `addons/web/static/fonts/lato/Lato-Bol-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-Bol-webfont.woff`
- `addons/web/static/fonts/lato/Lato-BolIta-webfont.eot`
- `addons/web/static/fonts/lato/Lato-BolIta-webfont.svg`
- `addons/web/static/fonts/lato/Lato-BolIta-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-BolIta-webfont.woff`
- `addons/web/static/fonts/lato/Lato-Hai-webfont.eot`
- `addons/web/static/fonts/lato/Lato-Hai-webfont.svg`
- `addons/web/static/fonts/lato/Lato-Hai-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-Hai-webfont.woff`
- `addons/web/static/fonts/lato/Lato-HaiIta-webfont.eot`
- `addons/web/static/fonts/lato/Lato-HaiIta-webfont.svg`
- `addons/web/static/fonts/lato/Lato-HaiIta-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-HaiIta-webfont.woff`
- `addons/web/static/fonts/lato/Lato-Lig-webfont.eot`
- `addons/web/static/fonts/lato/Lato-Lig-webfont.svg`
- `addons/web/static/fonts/lato/Lato-Lig-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-Lig-webfont.woff`
- `addons/web/static/fonts/lato/Lato-LigIta-webfont.eot`
- `addons/web/static/fonts/lato/Lato-LigIta-webfont.svg`
- `addons/web/static/fonts/lato/Lato-LigIta-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-LigIta-webfont.woff`
- `addons/web/static/fonts/lato/Lato-Reg-webfont.eot`
- `addons/web/static/fonts/lato/Lato-Reg-webfont.svg`
- `addons/web/static/fonts/lato/Lato-Reg-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-Reg-webfont.woff`
- `addons/web/static/fonts/lato/Lato-RegIta-webfont.eot`
- `addons/web/static/fonts/lato/Lato-RegIta-webfont.svg`
- `addons/web/static/fonts/lato/Lato-RegIta-webfont.ttf`
- `addons/web/static/fonts/lato/Lato-RegIta-webfont.woff`
- `addons/web/static/fonts/lato/SIL-Open-Font-License-1.1.txt`
- `addons/web/static/fonts/sign/LaBelleAurore-Regular.ttf`
- `addons/web/static/fonts/sign/LaBelleAurore-ofl.txt`
- `addons/web/static/fonts/sign/MarckScript-Regular-ofl.txt`
- `addons/web/static/fonts/sign/MarckScript-Regular.ttf`
- `addons/web/static/fonts/sign/NotoSans-Reg.ttf`
- `addons/web/static/fonts/sign/NotoSans-Regular-ofl.txt`
- `addons/web/static/fonts/sign/NotoSans-Regular.ttf`
- `addons/web/static/fonts/sign/NotoSansArabic-Regular-ofl.txt`
- `addons/web/static/fonts/sign/NotoSansArabic-Regular.ttf`
- `addons/web/static/fonts/sign/NotoSansBengali-Regular-ofl.txt`
- `addons/web/static/fonts/sign/NotoSansBengali-Regular.ttf`
- `addons/web/static/fonts/sign/NotoSansDevanagari-Regular-ofl.txt`
- `addons/web/static/fonts/sign/NotoSansDevanagari-Regular.ttf`
- `addons/web/static/fonts/sign/NotoSansGurmukhi-Regular-ofl.txt`
- `addons/web/static/fonts/sign/NotoSansGurmukhi-Regular.ttf`
- `addons/web/static/fonts/sign/OoohBaby-Regular-ofl.txt`
- `addons/web/static/fonts/sign/OoohBaby-Regular.ttf`
- `addons/web/static/fonts/sign/ReenieBeanie-Regular.ttf`
- `addons/web/static/fonts/sign/ReenieBeanie-ofl.txt`
- Additional source files not expanded in this page: 2180; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
