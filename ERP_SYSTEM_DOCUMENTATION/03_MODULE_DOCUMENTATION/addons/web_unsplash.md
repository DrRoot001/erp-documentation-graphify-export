# Module: web_unsplash

- **Module ID:** MOD-595
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/web_unsplash`
- **Manifest:** `addons/web_unsplash/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Find free high-resolution images from Unsplash

**Manifest description:**

Explore the free high-resolution image library of Unsplash.com and find images to use in Odoo. An Unsplash search bar is added to the image library modal.

**Scope evidence:** The module contains 82 files, including 12 Python, 4 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`, `html_editor`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 7
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 12 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/web_unsplash/models/res_config_settings.py:6`, `addons/web_unsplash/models/ir_qweb_fields.py:6`, `addons/web_unsplash/models/res_users.py:6`, `addons/web_unsplash/models/ir_attachment.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 4 route declarations.
- **Evidence:** `addons/web_unsplash/controllers/main.py:48`, `addons/web_unsplash/controllers/main.py:134`, `addons/web_unsplash/controllers/main.py:138`, `addons/web_unsplash/controllers/main.py:142`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 7 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/web_unsplash/views/res_config_settings_view.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/web_unsplash/tests/test_unsplash.py`, `addons/web_unsplash/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/web_unsplash/views/res_config_settings_view.xml:5`, `addons/web_unsplash/views/res_config_settings_view.xml:7`
- Browser assets: 7; representative files: `addons/web_unsplash/static/src/unsplash_service.js`, `addons/web_unsplash/static/tests/unsplash.test.js`, `addons/web_unsplash/static/src/unsplash_error/unsplash_error.js`, `addons/web_unsplash/static/src/unsplash_credentials/unsplash_credentials.js`, `addons/web_unsplash/static/src/media_dialog/image_selector_patch.js`, `addons/web_unsplash/static/src/media_dialog/media_dialog_patch.js`, `addons/web_unsplash/static/src/frontend/unsplash_beacon.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/web_unsplash/__manifest__.py`
- **HTTP entry points:** `addons/web_unsplash/controllers/main.py:48`, `addons/web_unsplash/controllers/main.py:134`, `addons/web_unsplash/controllers/main.py:138`, `addons/web_unsplash/controllers/main.py:142`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.config.settings` (addons/web_unsplash/models/res_config_settings.py:6); inherits `ir.qweb.field.image` (addons/web_unsplash/models/ir_qweb_fields.py:6); inherits `res.users` (addons/web_unsplash/models/res_users.py:6); inherits `ir.attachment` (addons/web_unsplash/models/ir_attachment.py:12)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 4
- Route evidence: `addons/web_unsplash/controllers/main.py:48`, `addons/web_unsplash/controllers/main.py:134`, `addons/web_unsplash/controllers/main.py:138`, `addons/web_unsplash/controllers/main.py:142`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`, `html_editor`
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

- `addons/web_unsplash/__init__.py`
- `addons/web_unsplash/__manifest__.py`
- `addons/web_unsplash/controllers/__init__.py`
- `addons/web_unsplash/controllers/main.py`
- `addons/web_unsplash/i18n/ar.po`
- `addons/web_unsplash/i18n/az.po`
- `addons/web_unsplash/i18n/bg.po`
- `addons/web_unsplash/i18n/bs.po`
- `addons/web_unsplash/i18n/ca.po`
- `addons/web_unsplash/i18n/cs.po`
- `addons/web_unsplash/i18n/da.po`
- `addons/web_unsplash/i18n/de.po`
- `addons/web_unsplash/i18n/el.po`
- `addons/web_unsplash/i18n/es.po`
- `addons/web_unsplash/i18n/es_419.po`
- `addons/web_unsplash/i18n/et.po`
- `addons/web_unsplash/i18n/fa.po`
- `addons/web_unsplash/i18n/fi.po`
- `addons/web_unsplash/i18n/fr.po`
- `addons/web_unsplash/i18n/gu.po`
- `addons/web_unsplash/i18n/he.po`
- `addons/web_unsplash/i18n/hi.po`
- `addons/web_unsplash/i18n/hr.po`
- `addons/web_unsplash/i18n/hu.po`
- `addons/web_unsplash/i18n/id.po`
- `addons/web_unsplash/i18n/is.po`
- `addons/web_unsplash/i18n/it.po`
- `addons/web_unsplash/i18n/ja.po`
- `addons/web_unsplash/i18n/kab.po`
- `addons/web_unsplash/i18n/km.po`
- `addons/web_unsplash/i18n/ko.po`
- `addons/web_unsplash/i18n/ku.po`
- `addons/web_unsplash/i18n/lo.po`
- `addons/web_unsplash/i18n/lt.po`
- `addons/web_unsplash/i18n/lv.po`
- `addons/web_unsplash/i18n/mn.po`
- `addons/web_unsplash/i18n/my.po`
- `addons/web_unsplash/i18n/nb.po`
- `addons/web_unsplash/i18n/nl.po`
- `addons/web_unsplash/i18n/pl.po`
- `addons/web_unsplash/i18n/pt.po`
- `addons/web_unsplash/i18n/pt_BR.po`
- `addons/web_unsplash/i18n/ro.po`
- `addons/web_unsplash/i18n/ru.po`
- `addons/web_unsplash/i18n/sk.po`
- `addons/web_unsplash/i18n/sl.po`
- `addons/web_unsplash/i18n/sr@latin.po`
- `addons/web_unsplash/i18n/sv.po`
- `addons/web_unsplash/i18n/th.po`
- `addons/web_unsplash/i18n/tr.po`
- `addons/web_unsplash/i18n/uk.po`
- `addons/web_unsplash/i18n/uz.po`
- `addons/web_unsplash/i18n/vi.po`
- `addons/web_unsplash/i18n/web_unsplash.pot`
- `addons/web_unsplash/i18n/zh_CN.po`
- `addons/web_unsplash/i18n/zh_TW.po`
- `addons/web_unsplash/models/__init__.py`
- `addons/web_unsplash/models/ir_attachment.py`
- `addons/web_unsplash/models/ir_qweb_fields.py`
- `addons/web_unsplash/models/res_config_settings.py`
- `addons/web_unsplash/models/res_users.py`
- `addons/web_unsplash/static/description/icon.png`
- `addons/web_unsplash/static/description/icon.svg`
- `addons/web_unsplash/static/description/icon2.png`
- `addons/web_unsplash/static/description/icon_hi.png`
- `addons/web_unsplash/static/description/index.html`
- `addons/web_unsplash/static/description/unsplash_interface.png`
- `addons/web_unsplash/static/description/unsplash_interface_bar.png`
- `addons/web_unsplash/static/src/frontend/unsplash_beacon.js`
- `addons/web_unsplash/static/src/media_dialog/image_selector_patch.js`
- `addons/web_unsplash/static/src/media_dialog/media_dialog.xml`
- `addons/web_unsplash/static/src/media_dialog/media_dialog_patch.js`
- `addons/web_unsplash/static/src/unsplash_credentials/unsplash_credentials.js`
- `addons/web_unsplash/static/src/unsplash_credentials/unsplash_credentials.xml`
- `addons/web_unsplash/static/src/unsplash_error/unsplash_error.js`
- `addons/web_unsplash/static/src/unsplash_error/unsplash_error.xml`
- `addons/web_unsplash/static/src/unsplash_service.js`
- `addons/web_unsplash/static/tests/unsplash.test.js`
- `addons/web_unsplash/tests/__init__.py`
- `addons/web_unsplash/tests/test_unsplash.py`
- `addons/web_unsplash/utils.py`
- `addons/web_unsplash/views/res_config_settings_view.xml`
