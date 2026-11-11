# Module: portal_discuss

- **Module ID:** MOD-420
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/portal_discuss`
- **Manifest:** `addons/portal_discuss/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Services`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Bridge module adding Discuss access from portal.

**Scope evidence:** The module contains 63 files, including 10 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `portal`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 3
- XML/data/view/template files: 2
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/portal_discuss/models/discuss_channel.py:6`, `addons/portal_discuss/models/portal_entry.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 0 route declarations.
- **Evidence:** `addons/portal_discuss/controllers/portal.py`, `addons/portal_discuss/controllers/public_page.py`, `addons/portal_discuss/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/portal_discuss/data/portal_entry_data.xml:3`, `addons/portal_discuss/views/portal_templates.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/portal_discuss/tests/test_portal_discuss.py`, `addons/portal_discuss/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `portal_entry_discuss`, `portal_docs_entry_inherit_discuss`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/portal_discuss/views/portal_templates.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 1; representative files: `addons/portal_discuss/static/src/core/common/discuss_client_action_patch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/portal_discuss/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `discuss.channel` (addons/portal_discuss/models/discuss_channel.py:6); inherits `portal.entry` (addons/portal_discuss/models/portal_entry.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `portal`
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

- `addons/portal_discuss/__init__.py`
- `addons/portal_discuss/__manifest__.py`
- `addons/portal_discuss/controllers/__init__.py`
- `addons/portal_discuss/controllers/portal.py`
- `addons/portal_discuss/controllers/public_page.py`
- `addons/portal_discuss/data/portal_entry_data.xml`
- `addons/portal_discuss/i18n/ar.po`
- `addons/portal_discuss/i18n/az.po`
- `addons/portal_discuss/i18n/bg.po`
- `addons/portal_discuss/i18n/bs.po`
- `addons/portal_discuss/i18n/ca.po`
- `addons/portal_discuss/i18n/cs.po`
- `addons/portal_discuss/i18n/da.po`
- `addons/portal_discuss/i18n/de.po`
- `addons/portal_discuss/i18n/el.po`
- `addons/portal_discuss/i18n/es.po`
- `addons/portal_discuss/i18n/es_419.po`
- `addons/portal_discuss/i18n/et.po`
- `addons/portal_discuss/i18n/fa.po`
- `addons/portal_discuss/i18n/fi.po`
- `addons/portal_discuss/i18n/fr.po`
- `addons/portal_discuss/i18n/he.po`
- `addons/portal_discuss/i18n/hi.po`
- `addons/portal_discuss/i18n/hr.po`
- `addons/portal_discuss/i18n/hu.po`
- `addons/portal_discuss/i18n/id.po`
- `addons/portal_discuss/i18n/it.po`
- `addons/portal_discuss/i18n/ja.po`
- `addons/portal_discuss/i18n/kab.po`
- `addons/portal_discuss/i18n/ko.po`
- `addons/portal_discuss/i18n/ku.po`
- `addons/portal_discuss/i18n/lo.po`
- `addons/portal_discuss/i18n/lt.po`
- `addons/portal_discuss/i18n/lv.po`
- `addons/portal_discuss/i18n/mn.po`
- `addons/portal_discuss/i18n/my.po`
- `addons/portal_discuss/i18n/nb.po`
- `addons/portal_discuss/i18n/nl.po`
- `addons/portal_discuss/i18n/pl.po`
- `addons/portal_discuss/i18n/portal_discuss.pot`
- `addons/portal_discuss/i18n/pt.po`
- `addons/portal_discuss/i18n/pt_BR.po`
- `addons/portal_discuss/i18n/ro.po`
- `addons/portal_discuss/i18n/ru.po`
- `addons/portal_discuss/i18n/sk.po`
- `addons/portal_discuss/i18n/sl.po`
- `addons/portal_discuss/i18n/sr@latin.po`
- `addons/portal_discuss/i18n/sv.po`
- `addons/portal_discuss/i18n/th.po`
- `addons/portal_discuss/i18n/tr.po`
- `addons/portal_discuss/i18n/uk.po`
- `addons/portal_discuss/i18n/uz.po`
- `addons/portal_discuss/i18n/vi.po`
- `addons/portal_discuss/i18n/zh_CN.po`
- `addons/portal_discuss/i18n/zh_TW.po`
- `addons/portal_discuss/models/__init__.py`
- `addons/portal_discuss/models/discuss_channel.py`
- `addons/portal_discuss/models/portal_entry.py`
- `addons/portal_discuss/static/src/core/common/discuss_client_action_patch.js`
- `addons/portal_discuss/static/src/img/portal-discuss.png`
- `addons/portal_discuss/tests/__init__.py`
- `addons/portal_discuss/tests/test_portal_discuss.py`
- `addons/portal_discuss/views/portal_templates.xml`
