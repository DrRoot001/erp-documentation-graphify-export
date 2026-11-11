# Module: portal_rating

- **Module ID:** MOD-421
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/portal_rating`
- **Manifest:** `addons/portal_rating/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Bridge module adding rating capabilities on portal. It includes notably
inclusion of rating directly within the customer portal discuss widget.

**Scope evidence:** The module contains 91 files, including 9 Python, 10 XML, and 19 JavaScript/TypeScript files. The manifest declares dependencies: `portal`, `rating`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 10
- Browser asset files: 19
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/portal_rating/models/mail_message.py:8`, `addons/portal_rating/models/ir_http.py:7`, `addons/portal_rating/models/rating_rating.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 1 route declarations.
- **Evidence:** `addons/portal_rating/controllers/portal_rating.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 19 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/portal_rating/views/portal_templates.xml:3`, `addons/portal_rating/views/rating_rating_views.xml:3`, `addons/portal_rating/views/rating_templates.xml:6`, `addons/portal_rating/views/rating_templates.xml:53`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `message_thread`, `rating_rating_view_form`, `Rating: static star widget`, `Rating: rating composer in popup`
- Menus: 0; representative evidence: Not found in module
- Templates: 3; representative evidence: `addons/portal_rating/views/portal_templates.xml:3`, `addons/portal_rating/views/rating_templates.xml:6`, `addons/portal_rating/views/rating_templates.xml:53`
- View/action field declarations: 2; representative evidence: `addons/portal_rating/views/rating_rating_views.xml:5`, `addons/portal_rating/views/rating_rating_views.xml:7`
- Browser assets: 19; representative files: `addons/portal_rating/static/src/interactions/portal_composer.js`, `addons/portal_rating/static/src/interactions/portal_rating_composer.js`, `addons/portal_rating/static/src/chatter/portal/suggestion_service_patch.js`, `addons/portal_rating/static/src/chatter/portal/thread_model_patch.js`, `addons/portal_rating/static/src/chatter/portal/portal_chatter_patch.js`, `addons/portal_rating/static/src/chatter/portal/composer_model_patch.js`, `addons/portal_rating/static/src/chatter/portal/composer_patch.js`, `addons/portal_rating/static/src/chatter/portal/chatter_patch.js`, `addons/portal_rating/static/src/chatter/portal/message_patch.js`, `addons/portal_rating/static/src/chatter/portal/thread_patch.js`, `addons/portal_rating/static/src/chatter/portal/store_service_patch.js`, `addons/portal_rating/static/src/chatter/portal/portal_chatter_service_patch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/portal_rating/__manifest__.py`
- **HTTP entry points:** `addons/portal_rating/controllers/portal_rating.py:10`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `mail.message` (addons/portal_rating/models/mail_message.py:8); inherits `ir.http` (addons/portal_rating/models/ir_http.py:7); inherits `rating.rating` (addons/portal_rating/models/rating_rating.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 1
- Route evidence: `addons/portal_rating/controllers/portal_rating.py:10`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `portal`, `rating`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/portal_rating/__init__.py`
- `addons/portal_rating/__manifest__.py`
- `addons/portal_rating/controllers/__init__.py`
- `addons/portal_rating/controllers/portal_rating.py`
- `addons/portal_rating/controllers/thread.py`
- `addons/portal_rating/i18n/ar.po`
- `addons/portal_rating/i18n/az.po`
- `addons/portal_rating/i18n/bg.po`
- `addons/portal_rating/i18n/bs.po`
- `addons/portal_rating/i18n/ca.po`
- `addons/portal_rating/i18n/cs.po`
- `addons/portal_rating/i18n/da.po`
- `addons/portal_rating/i18n/de.po`
- `addons/portal_rating/i18n/el.po`
- `addons/portal_rating/i18n/es.po`
- `addons/portal_rating/i18n/es_419.po`
- `addons/portal_rating/i18n/et.po`
- `addons/portal_rating/i18n/fa.po`
- `addons/portal_rating/i18n/fi.po`
- `addons/portal_rating/i18n/fr.po`
- `addons/portal_rating/i18n/gu.po`
- `addons/portal_rating/i18n/he.po`
- `addons/portal_rating/i18n/hi.po`
- `addons/portal_rating/i18n/hr.po`
- `addons/portal_rating/i18n/hu.po`
- `addons/portal_rating/i18n/id.po`
- `addons/portal_rating/i18n/is.po`
- `addons/portal_rating/i18n/it.po`
- `addons/portal_rating/i18n/ja.po`
- `addons/portal_rating/i18n/kab.po`
- `addons/portal_rating/i18n/km.po`
- `addons/portal_rating/i18n/ko.po`
- `addons/portal_rating/i18n/ku.po`
- `addons/portal_rating/i18n/lo.po`
- `addons/portal_rating/i18n/lt.po`
- `addons/portal_rating/i18n/lv.po`
- `addons/portal_rating/i18n/mn.po`
- `addons/portal_rating/i18n/my.po`
- `addons/portal_rating/i18n/nb.po`
- `addons/portal_rating/i18n/nl.po`
- `addons/portal_rating/i18n/pl.po`
- `addons/portal_rating/i18n/portal_rating.pot`
- `addons/portal_rating/i18n/pt.po`
- `addons/portal_rating/i18n/pt_BR.po`
- `addons/portal_rating/i18n/ro.po`
- `addons/portal_rating/i18n/ru.po`
- `addons/portal_rating/i18n/sk.po`
- `addons/portal_rating/i18n/sl.po`
- `addons/portal_rating/i18n/sr@latin.po`
- `addons/portal_rating/i18n/sv.po`
- `addons/portal_rating/i18n/th.po`
- `addons/portal_rating/i18n/tr.po`
- `addons/portal_rating/i18n/uk.po`
- `addons/portal_rating/i18n/uz.po`
- `addons/portal_rating/i18n/vi.po`
- `addons/portal_rating/i18n/zh_CN.po`
- `addons/portal_rating/i18n/zh_TW.po`
- `addons/portal_rating/models/__init__.py`
- `addons/portal_rating/models/ir_http.py`
- `addons/portal_rating/models/mail_message.py`
- `addons/portal_rating/models/rating_rating.py`
- `addons/portal_rating/static/src/chatter/portal/@types/models.d.ts`
- `addons/portal_rating/static/src/chatter/portal/chatter_patch.js`
- `addons/portal_rating/static/src/chatter/portal/composer_model_patch.js`
- `addons/portal_rating/static/src/chatter/portal/composer_patch.js`
- `addons/portal_rating/static/src/chatter/portal/composer_patch.xml`
- `addons/portal_rating/static/src/chatter/portal/message_model_patch.js`
- `addons/portal_rating/static/src/chatter/portal/message_patch.js`
- `addons/portal_rating/static/src/chatter/portal/message_patch.xml`
- `addons/portal_rating/static/src/chatter/portal/portal_chatter_patch.js`
- `addons/portal_rating/static/src/chatter/portal/portal_chatter_patch.xml`
- `addons/portal_rating/static/src/chatter/portal/portal_chatter_service_patch.js`
- `addons/portal_rating/static/src/chatter/portal/portal_rating_plugin.js`
- `addons/portal_rating/static/src/chatter/portal/store_service_patch.js`
- `addons/portal_rating/static/src/chatter/portal/suggestion_service_patch.js`
- `addons/portal_rating/static/src/chatter/portal/thread_model_patch.js`
- `addons/portal_rating/static/src/chatter/portal/thread_patch.js`
- `addons/portal_rating/static/src/chatter/portal/thread_patch.xml`
- `addons/portal_rating/static/src/core/common/@types/models.d.ts`
- `addons/portal_rating/static/src/core/common/message_model_patch.js`
- `addons/portal_rating/static/src/core/common/rating_model_patch.js`
- `addons/portal_rating/static/src/core/common/res_partner_model_patch.js`
- `addons/portal_rating/static/src/interactions/portal_composer.js`
- `addons/portal_rating/static/src/interactions/portal_rating_composer.js`
- `addons/portal_rating/static/src/scss/portal_rating.scss`
- `addons/portal_rating/static/src/xml/portal_chatter.xml`
- `addons/portal_rating/static/src/xml/portal_rating_composer.xml`
- `addons/portal_rating/static/src/xml/portal_tools.xml`
- `addons/portal_rating/views/portal_templates.xml`
- `addons/portal_rating/views/rating_rating_views.xml`
- `addons/portal_rating/views/rating_templates.xml`
