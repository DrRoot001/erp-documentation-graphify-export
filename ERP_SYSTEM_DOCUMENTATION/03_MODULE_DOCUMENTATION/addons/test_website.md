# Module: test_website

- **Module ID:** MOD-586
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/test_website`
- **Manifest:** `addons/test_website/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Website Test, mainly for module install/uninstall tests

**Manifest description:**

This module contains tests related to website. Those are
present in a separate module as we are testing module install/uninstall/upgrade
and we don't want to reload the website module every time, including it's possible
dependencies. Neither we want to add in website module some routes, views and
models which only purpose is to run tests.

**Scope evidence:** The module contains 64 files, including 35 Python, 8 XML, and 19 JavaScript/TypeScript files. The manifest declares dependencies: `web_unsplash`, `website`, `theme_default`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 2
- XML/data/view/template files: 8
- Browser asset files: 19
- Security files: 2
- Test files: 28
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/test_website/security/ir.access.csv`, `addons/test_website/security/test_website_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 150 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/test_website/models/model.py:8`, `addons/test_website/models/model.py:14`, `addons/test_website/models/model.py:71`, `addons/test_website/models/model.py:80`, `addons/test_website/models/model.py:87`, `addons/test_website/models/model.py:102`, `addons/test_website/models/website.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 37 route declarations.
- **Evidence:** `addons/test_website/controllers/main.py:15`, `addons/test_website/controllers/main.py:19`, `addons/test_website/controllers/main.py:25`, `addons/test_website/controllers/main.py:29`, `addons/test_website/controllers/main.py:33`, `addons/test_website/controllers/main.py:37`, `addons/test_website/controllers/main.py:41`, `addons/test_website/controllers/main.py:45`, `addons/test_website/controllers/main.py:49`, `addons/test_website/controllers/main.py:53`, `addons/test_website/controllers/main.py:59`, `addons/test_website/controllers/main.py:65`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 19 JavaScript/TypeScript files; static XML analysis found 44 record/template/menu identifiers.
- **Evidence:** `addons/test_website/security/test_website_security.xml:3`, `addons/test_website/security/test_website_security.xml:8`, `addons/test_website/security/test_website_security.xml:14`, `addons/test_website/data/test_website_data.xml:6`, `addons/test_website/data/test_website_data.xml:9`, `addons/test_website/data/test_website_data.xml:12`, `addons/test_website/data/test_website_data.xml:15`, `addons/test_website/data/test_website_data.xml:19`, `addons/test_website/data/test_website_data.xml:24`, `addons/test_website/data/test_website_data.xml:27`, `addons/test_website/data/test_website_data.xml:33`, `addons/test_website/data/test_website_data.xml:47`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/test_website/security/ir.access.csv`, `addons/test_website/security/test_website_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 28 test files are present.
- **Evidence:** `addons/test_website/tests/test_fuzzy.py`, `addons/test_website/tests/test_reset_views.py`, `addons/test_website/tests/test_menu.py`, `addons/test_website/tests/test_media.py`, `addons/test_website/tests/test_performance.py`, `addons/test_website/tests/test_snippet_background_video.py`, `addons/test_website/tests/test_multi_company.py`, `addons/test_website/tests/test_is_multilang.py`, `addons/test_website/tests/test_image_upload_progress.py`, `addons/test_website/tests/test_translation.py`, `addons/test_website/tests/test_form.py`, `addons/test_website/tests/test_views_during_module_operation.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `test_website.group_test_website_admin`, `group_test_website_tester`, `base.user_admin`, `test_tag_generic`, `test_tag_2`, `test_tag_3`, `test_model_generic`, `test_submodel_generic`, `test_model_multi_generic`, `test_model_multi_website_1`, `test_view`, `test_page_view`, `test_error_view`, `test_page`, `test_view_to_be_t_called`, `test_image_progress`, `test_model_record`, `test_model_exposed_record_published`, `test_model_exposed_record_not_published`, `test_view_child_broken`
- Menus: 1; representative evidence: `addons/test_website/views/test_model_views.xml:53`
- Templates: 12; representative evidence: `addons/test_website/data/test_website_data.xml:116`, `addons/test_website/data/test_website_data.xml:122`, `addons/test_website/data/test_website_data.xml:127`, `addons/test_website/data/test_website_data.xml:132`, `addons/test_website/data/test_website_data.xml:138`, `addons/test_website/views/templates.xml:23`, `addons/test_website/views/templates.xml:41`, `addons/test_website/views/templates.xml:81`, `addons/test_website/views/templates.xml:87`, `addons/test_website/views/templates.xml:95`, `addons/test_website/tests/template_qweb_test.xml:4`, `addons/test_website/tests/template_qweb_test.xml:24`
- View/action field declarations: 25; representative evidence: `addons/test_website/data/test_website_data.xml:38`, `addons/test_website/data/test_website_data.xml:52`, `addons/test_website/data/test_website_data.xml:66`, `addons/test_website/data/test_website_data.xml:109`, `addons/test_website/data/test_website_data.xml:147`, `addons/test_website/views/test_model_multi_website_views.xml:7`, `addons/test_website/views/test_model_multi_website_views.xml:8`, `addons/test_website/views/test_model_multi_website_views.xml:29`, `addons/test_website/views/test_model_multi_website_views.xml:31`, `addons/test_website/views/test_model_multi_website_views.xml:41`, `addons/test_website/views/test_model_multi_website_views.xml:42`, `addons/test_website/views/test_model_multi_website_views.xml:52`
- Browser assets: 19; representative files: `addons/test_website/static/src/interactions/test_error.js`, `addons/test_website/static/tests/tours/snippet_background_video.js`, `addons/test_website/static/tests/tours/translation.js`, `addons/test_website/static/tests/tours/json_auth.js`, `addons/test_website/static/tests/tours/image_upload_progress.js`, `addons/test_website/static/tests/tours/custom_snippets.js`, `addons/test_website/static/tests/tours/page_manager.js`, `addons/test_website/static/tests/tours/error_views.js`, `addons/test_website/static/tests/tours/reset_views.js`, `addons/test_website/static/tests/tours/restricted_editor.js`, `addons/test_website/static/tests/tours/replace_media.js`, `addons/test_website/static/tests/tours/website_page_properties.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/test_website/__manifest__.py`
- **HTTP entry points:** `addons/test_website/controllers/main.py:15`, `addons/test_website/controllers/main.py:19`, `addons/test_website/controllers/main.py:25`, `addons/test_website/controllers/main.py:29`, `addons/test_website/controllers/main.py:33`, `addons/test_website/controllers/main.py:37`, `addons/test_website/controllers/main.py:41`, `addons/test_website/controllers/main.py:45`, `addons/test_website/controllers/main.py:49`, `addons/test_website/controllers/main.py:53`, `addons/test_website/controllers/main.py:59`, `addons/test_website/controllers/main.py:65`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: inherits `website` (addons/test_website/models/model.py:8); `test.model` (addons/test_website/models/model.py:14); `test.submodel` (addons/test_website/models/model.py:71); `test.tag` (addons/test_website/models/model.py:80); `test.model.multi.website` (addons/test_website/models/model.py:87); `test.model.exposed` (addons/test_website/models/model.py:102); inherits `website` (addons/test_website/models/website.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 37
- Route evidence: `addons/test_website/controllers/main.py:15`, `addons/test_website/controllers/main.py:19`, `addons/test_website/controllers/main.py:25`, `addons/test_website/controllers/main.py:29`, `addons/test_website/controllers/main.py:33`, `addons/test_website/controllers/main.py:37`, `addons/test_website/controllers/main.py:41`, `addons/test_website/controllers/main.py:45`, `addons/test_website/controllers/main.py:49`, `addons/test_website/controllers/main.py:53`, `addons/test_website/controllers/main.py:59`, `addons/test_website/controllers/main.py:65`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web_unsplash`, `website`, `theme_default`
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

- `addons/test_website/__init__.py`
- `addons/test_website/__manifest__.py`
- `addons/test_website/controllers/__init__.py`
- `addons/test_website/controllers/main.py`
- `addons/test_website/data/test_website_data.xml`
- `addons/test_website/data/test_website_demo.xml`
- `addons/test_website/models/__init__.py`
- `addons/test_website/models/model.py`
- `addons/test_website/models/website.py`
- `addons/test_website/security/ir.access.csv`
- `addons/test_website/security/test_website_security.xml`
- `addons/test_website/static/src/interactions/test_error.js`
- `addons/test_website/static/src/website_builder/builder.scss`
- `addons/test_website/static/tests/builder/drag_and_drop.test.js`
- `addons/test_website/static/tests/tours/custom_snippets.js`
- `addons/test_website/static/tests/tours/error_views.js`
- `addons/test_website/static/tests/tours/form.js`
- `addons/test_website/static/tests/tours/image_link.js`
- `addons/test_website/static/tests/tours/image_upload_progress.js`
- `addons/test_website/static/tests/tours/json_auth.js`
- `addons/test_website/static/tests/tours/page_manager.js`
- `addons/test_website/static/tests/tours/replace_media.js`
- `addons/test_website/static/tests/tours/reset_views.js`
- `addons/test_website/static/tests/tours/restricted_editor.js`
- `addons/test_website/static/tests/tours/snippet_background_video.js`
- `addons/test_website/static/tests/tours/systray.js`
- `addons/test_website/static/tests/tours/translation.js`
- `addons/test_website/static/tests/tours/website_controller_page.js`
- `addons/test_website/static/tests/tours/website_field_sanitize.js`
- `addons/test_website/static/tests/tours/website_page_properties.js`
- `addons/test_website/static/tests/tours/website_settings.js`
- `addons/test_website/tests/__init__.py`
- `addons/test_website/tests/asset_tag.xml`
- `addons/test_website/tests/template_qweb_test.xml`
- `addons/test_website/tests/test_controller_args.py`
- `addons/test_website/tests/test_custom_snippet.py`
- `addons/test_website/tests/test_error.py`
- `addons/test_website/tests/test_form.py`
- `addons/test_website/tests/test_fuzzy.py`
- `addons/test_website/tests/test_image_upload_progress.py`
- `addons/test_website/tests/test_is_multilang.py`
- `addons/test_website/tests/test_media.py`
- `addons/test_website/tests/test_menu.py`
- `addons/test_website/tests/test_multi_company.py`
- `addons/test_website/tests/test_page.py`
- `addons/test_website/tests/test_page_manager.py`
- `addons/test_website/tests/test_performance.py`
- `addons/test_website/tests/test_qweb.py`
- `addons/test_website/tests/test_redirect.py`
- `addons/test_website/tests/test_reset_views.py`
- `addons/test_website/tests/test_restricted_editor.py`
- `addons/test_website/tests/test_session.py`
- `addons/test_website/tests/test_settings.py`
- `addons/test_website/tests/test_snippet_background_video.py`
- `addons/test_website/tests/test_systray.py`
- `addons/test_website/tests/test_theme_ir_asset.py`
- `addons/test_website/tests/test_translation.py`
- `addons/test_website/tests/test_views_during_module_operation.py`
- `addons/test_website/tests/test_website_controller_page.py`
- `addons/test_website/tests/test_website_field_sanitize.py`
- `addons/test_website/tests/test_website_page_properties.py`
- `addons/test_website/views/templates.xml`
- `addons/test_website/views/test_model_multi_website_views.xml`
- `addons/test_website/views/test_model_views.xml`
