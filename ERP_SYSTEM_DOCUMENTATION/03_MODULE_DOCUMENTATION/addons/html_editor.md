# Module: html_editor

- **Module ID:** MOD-106
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/html_editor`
- **Manifest:** `addons/html_editor/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A Html Editor component and plugin system.

**Manifest description:**

Html Editor
==========================
This addon provides an extensible, maintainable editor.

**Scope evidence:** The module contains 638 files, including 26 Python, 75 XML, and 395 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `bus`, `web`.

## 2. Module structure

- Model/business logic files: 22
- Controller/API files: 3
- XML/data/view/template files: 75
- Browser asset files: 395
- Security files: 1
- Test files: 11
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/html_editor/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 22 model declarations, 125 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/html_editor/models/html_field_history_mixin.py:9`, `addons/html_editor/models/ir_ui_view.py:12`, `addons/html_editor/models/ir_websocket.py:8`, `addons/html_editor/models/test_models.py:6`, `addons/html_editor/models/test_models.py:32`, `addons/html_editor/models/ir_http.py:7`, `addons/html_editor/models/ir_qweb_fields.py:35`, `addons/html_editor/models/ir_qweb_fields.py:60`, `addons/html_editor/models/ir_qweb_fields.py:94`, `addons/html_editor/models/ir_qweb_fields.py:106`, `addons/html_editor/models/ir_qweb_fields.py:119`, `addons/html_editor/models/ir_qweb_fields.py:165`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 17 route declarations.
- **Evidence:** `addons/html_editor/controllers/main.py:232`, `addons/html_editor/controllers/main.py:270`, `addons/html_editor/controllers/main.py:366`, `addons/html_editor/controllers/main.py:391`, `addons/html_editor/controllers/main.py:397`, `addons/html_editor/controllers/main.py:519`, `addons/html_editor/controllers/main.py:570`, `addons/html_editor/controllers/main.py:626`, `addons/html_editor/controllers/main.py:645`, `addons/html_editor/controllers/main.py:675`, `addons/html_editor/controllers/main.py:699`, `addons/html_editor/controllers/main.py:721`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 75 XML files and 395 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/html_editor/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 11 test files are present.
- **Evidence:** `addons/html_editor/models/test_models.py`, `addons/html_editor/tests/test_html_field_pending_attachments.py`, `addons/html_editor/tests/test_controller.py`, `addons/html_editor/tests/test_diff_utils.py`, `addons/html_editor/tests/test_modify_image_no_data.py`, `addons/html_editor/tests/test_icons.py`, `addons/html_editor/tests/test_converter.py`, `addons/html_editor/tests/__init__.py`, `addons/html_editor/tests/test_views.py`, `addons/html_editor/tests/test_ir_attachment.py`, `addons/html_editor/tests/test_collaboration_bus.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 75; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 395; representative files: `addons/html_editor/static/src/editor.js`, `addons/html_editor/static/src/local_overlay_container.js`, `addons/html_editor/static/src/position_hook.js`, `addons/html_editor/static/src/wysiwyg.js`, `addons/html_editor/static/src/plugin.js`, `addons/html_editor/static/src/toolbar_dropdown_hook.js`, `addons/html_editor/static/src/plugin_sets.js`, `addons/html_editor/static/tests/file.test.js`, `addons/html_editor/static/tests/date.test.js`, `addons/html_editor/static/tests/initialization.test.js`, `addons/html_editor/static/tests/tabs.test.js`, `addons/html_editor/static/tests/html_migrations.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/html_editor/__manifest__.py`
- **HTTP entry points:** `addons/html_editor/controllers/main.py:232`, `addons/html_editor/controllers/main.py:270`, `addons/html_editor/controllers/main.py:366`, `addons/html_editor/controllers/main.py:391`, `addons/html_editor/controllers/main.py:397`, `addons/html_editor/controllers/main.py:519`, `addons/html_editor/controllers/main.py:570`, `addons/html_editor/controllers/main.py:626`, `addons/html_editor/controllers/main.py:645`, `addons/html_editor/controllers/main.py:675`, `addons/html_editor/controllers/main.py:699`, `addons/html_editor/controllers/main.py:721`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 22
- Representative model evidence: `html.field.history.mixin` (addons/html_editor/models/html_field_history_mixin.py:9); inherits `ir.ui.view` (addons/html_editor/models/ir_ui_view.py:12); inherits `ir.websocket` (addons/html_editor/models/ir_websocket.py:8); `html_editor.converter.test` (addons/html_editor/models/test_models.py:6); `html_editor.converter.test.sub` (addons/html_editor/models/test_models.py:32); inherits `ir.http` (addons/html_editor/models/ir_http.py:7); inherits `ir.qweb` (addons/html_editor/models/ir_qweb_fields.py:35); `ir.qweb.field` (addons/html_editor/models/ir_qweb_fields.py:60); `ir.qweb.field.integer` (addons/html_editor/models/ir_qweb_fields.py:94); `ir.qweb.field.float` (addons/html_editor/models/ir_qweb_fields.py:106); `ir.qweb.field.many2one` (addons/html_editor/models/ir_qweb_fields.py:119); `ir.qweb.field.contact` (addons/html_editor/models/ir_qweb_fields.py:165); `ir.qweb.field.date` (addons/html_editor/models/ir_qweb_fields.py:183); `ir.qweb.field.datetime` (addons/html_editor/models/ir_qweb_fields.py:221); `ir.qweb.field.text` (addons/html_editor/models/ir_qweb_fields.py:282); `ir.qweb.field.selection` (addons/html_editor/models/ir_qweb_fields.py:292); `ir.qweb.field.html` (addons/html_editor/models/ir_qweb_fields.py:309); `ir.qweb.field.image` (addons/html_editor/models/ir_qweb_fields.py:352); inherits `ir.qweb.field.monetary` (addons/html_editor/models/ir_qweb_fields.py:445); `ir.qweb.field.duration` (addons/html_editor/models/ir_qweb_fields.py:458); inherits `base` (addons/html_editor/models/models.py:6); inherits `ir.attachment` (addons/html_editor/models/ir_attachment.py:20)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 17
- Route evidence: `addons/html_editor/controllers/main.py:232`, `addons/html_editor/controllers/main.py:270`, `addons/html_editor/controllers/main.py:366`, `addons/html_editor/controllers/main.py:391`, `addons/html_editor/controllers/main.py:397`, `addons/html_editor/controllers/main.py:519`, `addons/html_editor/controllers/main.py:570`, `addons/html_editor/controllers/main.py:626`, `addons/html_editor/controllers/main.py:645`, `addons/html_editor/controllers/main.py:675`, `addons/html_editor/controllers/main.py:699`, `addons/html_editor/controllers/main.py:721`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `bus`, `web`
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

- `addons/html_editor/__init__.py`
- `addons/html_editor/__manifest__.py`
- `addons/html_editor/controllers/__init__.py`
- `addons/html_editor/controllers/main.py`
- `addons/html_editor/controllers/svg_utils.py`
- `addons/html_editor/i18n/ar.po`
- `addons/html_editor/i18n/az.po`
- `addons/html_editor/i18n/bg.po`
- `addons/html_editor/i18n/bs.po`
- `addons/html_editor/i18n/ca.po`
- `addons/html_editor/i18n/cs.po`
- `addons/html_editor/i18n/da.po`
- `addons/html_editor/i18n/de.po`
- `addons/html_editor/i18n/el.po`
- `addons/html_editor/i18n/es.po`
- `addons/html_editor/i18n/es_419.po`
- `addons/html_editor/i18n/et.po`
- `addons/html_editor/i18n/fa.po`
- `addons/html_editor/i18n/fi.po`
- `addons/html_editor/i18n/fr.po`
- `addons/html_editor/i18n/he.po`
- `addons/html_editor/i18n/hi.po`
- `addons/html_editor/i18n/hr.po`
- `addons/html_editor/i18n/html_editor.pot`
- `addons/html_editor/i18n/hu.po`
- `addons/html_editor/i18n/id.po`
- `addons/html_editor/i18n/it.po`
- `addons/html_editor/i18n/ja.po`
- `addons/html_editor/i18n/kab.po`
- `addons/html_editor/i18n/ko.po`
- `addons/html_editor/i18n/ku.po`
- `addons/html_editor/i18n/lo.po`
- `addons/html_editor/i18n/lt.po`
- `addons/html_editor/i18n/lv.po`
- `addons/html_editor/i18n/mn.po`
- `addons/html_editor/i18n/my.po`
- `addons/html_editor/i18n/nb.po`
- `addons/html_editor/i18n/nl.po`
- `addons/html_editor/i18n/pl.po`
- `addons/html_editor/i18n/pt.po`
- `addons/html_editor/i18n/pt_BR.po`
- `addons/html_editor/i18n/ro.po`
- `addons/html_editor/i18n/ru.po`
- `addons/html_editor/i18n/sk.po`
- `addons/html_editor/i18n/sl.po`
- `addons/html_editor/i18n/sr@latin.po`
- `addons/html_editor/i18n/sv.po`
- `addons/html_editor/i18n/th.po`
- `addons/html_editor/i18n/tr.po`
- `addons/html_editor/i18n/uk.po`
- `addons/html_editor/i18n/uz.po`
- `addons/html_editor/i18n/vi.po`
- `addons/html_editor/i18n/zh_CN.po`
- `addons/html_editor/i18n/zh_TW.po`
- `addons/html_editor/models/__init__.py`
- `addons/html_editor/models/diff_utils.py`
- `addons/html_editor/models/html_field_history_mixin.py`
- `addons/html_editor/models/ir_attachment.py`
- `addons/html_editor/models/ir_http.py`
- `addons/html_editor/models/ir_qweb_fields.py`
- `addons/html_editor/models/ir_ui_view.py`
- `addons/html_editor/models/ir_websocket.py`
- `addons/html_editor/models/models.py`
- `addons/html_editor/models/test_models.py`
- `addons/html_editor/security/ir.access.csv`
- `addons/html_editor/static/lib/cropperjs/LICENSE`
- `addons/html_editor/static/lib/cropperjs/cropper.css`
- `addons/html_editor/static/lib/cropperjs/cropper.js`
- `addons/html_editor/static/lib/diff2html/LICENSE`
- `addons/html_editor/static/lib/diff2html/diff2html.min.css`
- `addons/html_editor/static/lib/diff2html/diff2html.min.js`
- `addons/html_editor/static/lib/vkbeautify/vkbeautify.0.99.00.beta.js`
- `addons/html_editor/static/lib/webgl-image-filter/LICENSE`
- `addons/html_editor/static/lib/webgl-image-filter/webgl-image-filter.js`
- `addons/html_editor/static/src/@types/plugins.d.ts`
- `addons/html_editor/static/src/backend/dynamic_field/dynamic_field_plugin.js`
- `addons/html_editor/static/src/backend/dynamic_field/dynamic_field_plugin.scss`
- `addons/html_editor/static/src/backend/dynamic_field/field_selector_popover.js`
- `addons/html_editor/static/src/backend/dynamic_field/field_selector_popover.xml`
- `addons/html_editor/static/src/components/color_picker/color_picker.js`
- `addons/html_editor/static/src/components/color_picker/color_picker.scss`
- `addons/html_editor/static/src/components/color_picker/color_picker.xml`
- `addons/html_editor/static/src/components/color_picker/custom_color_picker/custom_color_picker.js`
- `addons/html_editor/static/src/components/color_picker/custom_color_picker/custom_color_picker.scss`
- `addons/html_editor/static/src/components/color_picker/custom_color_picker/custom_color_picker.xml`
- `addons/html_editor/static/src/components/color_picker/gradient_picker/gradient_picker.js`
- `addons/html_editor/static/src/components/color_picker/gradient_picker/gradient_picker.scss`
- `addons/html_editor/static/src/components/color_picker/gradient_picker/gradient_picker.xml`
- `addons/html_editor/static/src/components/color_picker/tabs/custom/color_picker_custom_tab.js`
- `addons/html_editor/static/src/components/color_picker/tabs/custom/color_picker_custom_tab.xml`
- `addons/html_editor/static/src/components/color_picker/tabs/gradient/color_picker_gradient_tab.js`
- `addons/html_editor/static/src/components/color_picker/tabs/gradient/color_picker_gradient_tab.scss`
- `addons/html_editor/static/src/components/color_picker/tabs/gradient/color_picker_gradient_tab.xml`
- `addons/html_editor/static/src/components/color_picker/tabs/solid/color_picker_solid_tab.js`
- `addons/html_editor/static/src/components/color_picker/tabs/solid/color_picker_solid_tab.xml`
- `addons/html_editor/static/src/components/history_dialog/history_dialog.dark.scss`
- `addons/html_editor/static/src/components/history_dialog/history_dialog.js`
- `addons/html_editor/static/src/components/history_dialog/history_dialog.scss`
- `addons/html_editor/static/src/components/history_dialog/history_dialog.xml`
- `addons/html_editor/static/src/components/html_viewer/html_viewer.js`
- `addons/html_editor/static/src/components/html_viewer/html_viewer.xml`
- `addons/html_editor/static/src/components/iframe_input/iframe_input.js`
- `addons/html_editor/static/src/components/iframe_input/iframe_input.xml`
- `addons/html_editor/static/src/components/suggestion/suggestion_list.js`
- `addons/html_editor/static/src/components/suggestion/suggestion_list.scss`
- `addons/html_editor/static/src/components/suggestion/suggestion_list.xml`
- `addons/html_editor/static/src/components/switch/switch.js`
- `addons/html_editor/static/src/components/switch/switch.scss`
- `addons/html_editor/static/src/core/base_container_plugin.js`
- `addons/html_editor/static/src/core/clipboard_plugin.js`
- `addons/html_editor/static/src/core/comment_plugin.js`
- `addons/html_editor/static/src/core/content_editable_plugin.js`
- `addons/html_editor/static/src/core/delete_plugin.js`
- `addons/html_editor/static/src/core/dialog_plugin.js`
- `addons/html_editor/static/src/core/dom_observer_plugin.js`
- `addons/html_editor/static/src/core/dom_plugin.js`
- `addons/html_editor/static/src/core/dom_reference_map_plugin.js`
- `addons/html_editor/static/src/core/editor_version_plugin.js`
- `addons/html_editor/static/src/core/format_plugin.js`
- `addons/html_editor/static/src/core/format_plugin.scss`
- `addons/html_editor/static/src/core/history_plugin.js`
- `addons/html_editor/static/src/core/input_plugin.js`
- `addons/html_editor/static/src/core/legacy_compatibility_plugin.js`
- `addons/html_editor/static/src/core/line_break_plugin.js`
- `addons/html_editor/static/src/core/no_inline_root_plugin.js`
- `addons/html_editor/static/src/core/overlay.js`
- `addons/html_editor/static/src/core/overlay_plugin.js`
- `addons/html_editor/static/src/core/protected_node_plugin.js`
- `addons/html_editor/static/src/core/sanitize_plugin.js`
- `addons/html_editor/static/src/core/selection_plugin.js`
- `addons/html_editor/static/src/core/shortcut_plugin.js`
- `addons/html_editor/static/src/core/split_plugin.js`
- `addons/html_editor/static/src/core/style_plugin.js`
- `addons/html_editor/static/src/core/user_command_plugin.js`
- `addons/html_editor/static/src/editor.js`
- `addons/html_editor/static/src/fields/html_field.js`
- `addons/html_editor/static/src/fields/html_field.scss`
- `addons/html_editor/static/src/fields/html_field.xml`
- `addons/html_editor/static/src/fields/image_field_with_media_dialog/image_field_with_media_dialog.js`
- `addons/html_editor/static/src/fields/image_field_with_media_dialog/image_field_with_media_dialog.xml`
- `addons/html_editor/static/src/fields/property_value.js`
- `addons/html_editor/static/src/fields/property_value.scss`
- `addons/html_editor/static/src/fields/property_value.xml`
- `addons/html_editor/static/src/fields/x2many_field/custom_media_dialog.js`
- `addons/html_editor/static/src/fields/x2many_field/x2many_image_field.js`
- `addons/html_editor/static/src/fields/x2many_field/x2many_image_field.xml`
- `addons/html_editor/static/src/fields/x2many_field/x2many_media_viewer.js`
- `addons/html_editor/static/src/fields/x2many_field/x2many_media_viewer.xml`
- `addons/html_editor/static/src/html_migrations/html_migrations_utils.js`
- `addons/html_editor/static/src/html_migrations/html_upgrade_manager.js`
- `addons/html_editor/static/src/html_migrations/manifest.js`
- `addons/html_editor/static/src/html_migrations/migration-1.1.js`
- `addons/html_editor/static/src/html_migrations/migration-1.2.js`
- `addons/html_editor/static/src/img/curved_arrow.svg`
- `addons/html_editor/static/src/img/gradient-closest-corner.svg`
- `addons/html_editor/static/src/img/gradient-closest-side.svg`
- `addons/html_editor/static/src/img/gradient-farthest-corner.svg`
- `addons/html_editor/static/src/img/gradient-farthest-side.svg`
- `addons/html_editor/static/src/img/placeholder_thumbnail.png`
- `addons/html_editor/static/src/img/signature-icon.svg`
- `addons/html_editor/static/src/local_overlay_container.js`
- `addons/html_editor/static/src/local_overlay_container.xml`
- `addons/html_editor/static/src/main/align/align_plugin.js`
- `addons/html_editor/static/src/main/align/align_selector.js`
- `addons/html_editor/static/src/main/align/align_selector.scss`
- `addons/html_editor/static/src/main/align/align_selector.xml`
- `addons/html_editor/static/src/main/banner.scss`
- `addons/html_editor/static/src/main/banner_plugin.js`
- `addons/html_editor/static/src/main/code_block_plugin.js`
- `addons/html_editor/static/src/main/column.scss`
- `addons/html_editor/static/src/main/column_plugin.js`
- `addons/html_editor/static/src/main/emoji_plugin.js`
- `addons/html_editor/static/src/main/feff_plugin.js`
- `addons/html_editor/static/src/main/font/color_plugin.js`
- `addons/html_editor/static/src/main/font/color_selector.js`
- `addons/html_editor/static/src/main/font/color_selector.scss`
- `addons/html_editor/static/src/main/font/color_selector.xml`
- `addons/html_editor/static/src/main/font/color_ui_plugin.js`
- `addons/html_editor/static/src/main/font/contrast_plugin.js`
- `addons/html_editor/static/src/main/font/font_family_plugin.js`
- `addons/html_editor/static/src/main/font/font_family_selector.js`
- `addons/html_editor/static/src/main/font/font_family_selector.xml`
- `addons/html_editor/static/src/main/font/font_size_plugin.js`
- `addons/html_editor/static/src/main/font/font_size_selector.dark.scss`
- `addons/html_editor/static/src/main/font/font_size_selector.js`
- `addons/html_editor/static/src/main/font/font_size_selector.scss`
- `addons/html_editor/static/src/main/font/font_size_selector.xml`
- `addons/html_editor/static/src/main/font/font_type.scss`
- `addons/html_editor/static/src/main/font/font_type_plugin.js`
- `addons/html_editor/static/src/main/font/font_type_selector.js`
- `addons/html_editor/static/src/main/font/font_type_selector.scss`
- `addons/html_editor/static/src/main/font/font_type_selector.xml`
- `addons/html_editor/static/src/main/hint.scss`
- `addons/html_editor/static/src/main/hint_plugin.js`
- `addons/html_editor/static/src/main/inline_code.js`
- `addons/html_editor/static/src/main/link/command_category.js`
- `addons/html_editor/static/src/main/link/link.scss`
- `addons/html_editor/static/src/main/link/link_paste_plugin.js`
- `addons/html_editor/static/src/main/link/link_plugin.js`
- `addons/html_editor/static/src/main/link/link_popover.dark.scss`
- `addons/html_editor/static/src/main/link/link_popover.js`
- `addons/html_editor/static/src/main/link/link_popover.scss`
- `addons/html_editor/static/src/main/link/link_popover.xml`
- `addons/html_editor/static/src/main/link/link_selection_odoo_plugin.js`
- `addons/html_editor/static/src/main/link/link_selection_plugin.js`
- `addons/html_editor/static/src/main/link/powerbox_url_paste_plugin.js`
- `addons/html_editor/static/src/main/link/utils.js`
- `addons/html_editor/static/src/main/list/list.scss`
- `addons/html_editor/static/src/main/list/list_plugin.js`
- `addons/html_editor/static/src/main/list/list_selector.js`
- `addons/html_editor/static/src/main/list/list_selector.xml`
- `addons/html_editor/static/src/main/list/utils.js`
- `addons/html_editor/static/src/main/local_overlay.scss`
- `addons/html_editor/static/src/main/local_overlay_plugin.js`
- `addons/html_editor/static/src/main/media/dblclick_image_preview_plugin.js`
- `addons/html_editor/static/src/main/media/file.scss`
- `addons/html_editor/static/src/main/media/file_plugin.js`
- `addons/html_editor/static/src/main/media/icon_color_plugin.js`
- `addons/html_editor/static/src/main/media/icon_plugin.js`
- `addons/html_editor/static/src/main/media/image_align_selector.js`
- `addons/html_editor/static/src/main/media/image_align_selector.xml`
- `addons/html_editor/static/src/main/media/image_crop.js`
- `addons/html_editor/static/src/main/media/image_crop.scss`
- `addons/html_editor/static/src/main/media/image_crop.xml`
- `addons/html_editor/static/src/main/media/image_crop_plugin.js`
- `addons/html_editor/static/src/main/media/image_plugin.js`
- `addons/html_editor/static/src/main/media/image_post_process_plugin.js`
- `addons/html_editor/static/src/main/media/image_save_plugin.js`
- `addons/html_editor/static/src/main/media/image_toolbar_dropdown.js`
- `addons/html_editor/static/src/main/media/image_toolbar_dropdown.xml`
- `addons/html_editor/static/src/main/media/image_transformation.js`
- `addons/html_editor/static/src/main/media/image_transformation.scss`
- `addons/html_editor/static/src/main/media/image_transformation.xml`
- `addons/html_editor/static/src/main/media/media_dialog/attachment_error.xml`
- `addons/html_editor/static/src/main/media/media_dialog/document_selector.js`
- `addons/html_editor/static/src/main/media/media_dialog/document_selector.xml`
- `addons/html_editor/static/src/main/media/media_dialog/file_selector.js`
- `addons/html_editor/static/src/main/media/media_dialog/file_selector.xml`
- `addons/html_editor/static/src/main/media/media_dialog/icon_selector.js`
- `addons/html_editor/static/src/main/media/media_dialog/icon_selector.xml`
- `addons/html_editor/static/src/main/media/media_dialog/image_selector.js`
- `addons/html_editor/static/src/main/media/media_dialog/image_selector.xml`
- `addons/html_editor/static/src/main/media/media_dialog/media_dialog.js`
- `addons/html_editor/static/src/main/media/media_dialog/media_dialog.scss`
- `addons/html_editor/static/src/main/media/media_dialog/media_dialog.xml`
- `addons/html_editor/static/src/main/media/media_dialog/media_dialog_utils.js`
- `addons/html_editor/static/src/main/media/media_dialog/search_media.js`
- `addons/html_editor/static/src/main/media/media_dialog/search_media.xml`
- `addons/html_editor/static/src/main/media/media_dialog/upload_progress_toast/upload_progress_toast.js`
- `addons/html_editor/static/src/main/media/media_dialog/upload_progress_toast/upload_progress_toast.scss`
- Additional source files not expanded in this page: 388; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
