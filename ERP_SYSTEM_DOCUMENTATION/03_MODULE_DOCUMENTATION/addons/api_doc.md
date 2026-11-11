# Module: api_doc

- **Module ID:** MOD-018
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/api_doc`
- **Manifest:** `addons/api_doc/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Odoo Dynamic API Documentation
==============================

This module provides a dynamic documentation page for developpers at the
/doc URL. The documentation is generated using the database to list the
models and their fields and methods. It also provides a playground to run
the methods over HTTP, with examples in various programming languages.

**Scope evidence:** The module contains 89 files, including 10 Python, 10 XML, and 21 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 2
- XML/data/view/template files: 10
- Browser asset files: 21
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/api_doc/security/res_groups.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 52 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/api_doc/models/ir_attachment.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/api_doc/controllers/api_doc.py:39`, `addons/api_doc/controllers/api_doc.py:49`, `addons/api_doc/controllers/api_doc.py:53`, `addons/api_doc/controllers/api_doc.py:167`, `addons/api_doc/controllers/api_doc.py:171`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 10 XML files and 21 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/api_doc/security/res_groups.xml:4`, `addons/api_doc/views/docclient.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/api_doc/security/res_groups.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/api_doc/models/ir_attachment.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/api_doc/tests/test_doc.py`, `addons/api_doc/tests/test_api_doc_tour.py`, `addons/api_doc/tests/__init__.py`, `addons/api_doc/tests/dummy_methods.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 10; representative identifiers: `group_allow_doc`, `api_doc.docclient`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/api_doc/views/docclient.xml:3`
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 21; representative files: `addons/api_doc/static/src/doc_client.js`, `addons/api_doc/static/src/main.js`, `addons/api_doc/static/src/start_doc_client.js`, `addons/api_doc/static/src/doc_model_store.js`, `addons/api_doc/static/src/api_action.js`, `addons/api_doc/static/tests/doc_test_helpers.js`, `addons/api_doc/static/tests/api_doc.test.js`, `addons/api_doc/static/src/components/doc_table.js`, `addons/api_doc/static/src/components/doc_model.js`, `addons/api_doc/static/src/components/doc_method.js`, `addons/api_doc/static/src/components/doc_loading_indicator.js`, `addons/api_doc/static/src/components/doc_sidebar.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/api_doc/__manifest__.py`
- **HTTP entry points:** `addons/api_doc/controllers/api_doc.py:39`, `addons/api_doc/controllers/api_doc.py:49`, `addons/api_doc/controllers/api_doc.py:53`, `addons/api_doc/controllers/api_doc.py:167`, `addons/api_doc/controllers/api_doc.py:171`
- **Scheduled entry points:** `addons/api_doc/models/ir_attachment.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `ir.attachment` (addons/api_doc/models/ir_attachment.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/api_doc/controllers/api_doc.py:39`, `addons/api_doc/controllers/api_doc.py:49`, `addons/api_doc/controllers/api_doc.py:53`, `addons/api_doc/controllers/api_doc.py:167`, `addons/api_doc/controllers/api_doc.py:171`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/api_doc/__init__.py`
- `addons/api_doc/__manifest__.py`
- `addons/api_doc/controllers/__init__.py`
- `addons/api_doc/controllers/api_doc.py`
- `addons/api_doc/i18n/api_doc.pot`
- `addons/api_doc/i18n/ar.po`
- `addons/api_doc/i18n/az.po`
- `addons/api_doc/i18n/bg.po`
- `addons/api_doc/i18n/bs.po`
- `addons/api_doc/i18n/ca.po`
- `addons/api_doc/i18n/cs.po`
- `addons/api_doc/i18n/da.po`
- `addons/api_doc/i18n/de.po`
- `addons/api_doc/i18n/el.po`
- `addons/api_doc/i18n/es.po`
- `addons/api_doc/i18n/es_419.po`
- `addons/api_doc/i18n/et.po`
- `addons/api_doc/i18n/fa.po`
- `addons/api_doc/i18n/fi.po`
- `addons/api_doc/i18n/fr.po`
- `addons/api_doc/i18n/he.po`
- `addons/api_doc/i18n/hi.po`
- `addons/api_doc/i18n/hr.po`
- `addons/api_doc/i18n/hu.po`
- `addons/api_doc/i18n/id.po`
- `addons/api_doc/i18n/it.po`
- `addons/api_doc/i18n/ja.po`
- `addons/api_doc/i18n/kab.po`
- `addons/api_doc/i18n/ko.po`
- `addons/api_doc/i18n/ku.po`
- `addons/api_doc/i18n/lt.po`
- `addons/api_doc/i18n/lv.po`
- `addons/api_doc/i18n/mn.po`
- `addons/api_doc/i18n/my.po`
- `addons/api_doc/i18n/nb.po`
- `addons/api_doc/i18n/nl.po`
- `addons/api_doc/i18n/pl.po`
- `addons/api_doc/i18n/pt.po`
- `addons/api_doc/i18n/pt_BR.po`
- `addons/api_doc/i18n/ro.po`
- `addons/api_doc/i18n/ru.po`
- `addons/api_doc/i18n/sk.po`
- `addons/api_doc/i18n/sl.po`
- `addons/api_doc/i18n/sr@latin.po`
- `addons/api_doc/i18n/sv.po`
- `addons/api_doc/i18n/th.po`
- `addons/api_doc/i18n/tr.po`
- `addons/api_doc/i18n/uk.po`
- `addons/api_doc/i18n/vi.po`
- `addons/api_doc/i18n/zh_CN.po`
- `addons/api_doc/i18n/zh_TW.po`
- `addons/api_doc/models/__init__.py`
- `addons/api_doc/models/ir_attachment.py`
- `addons/api_doc/security/res_groups.xml`
- `addons/api_doc/static/src/api_action.js`
- `addons/api_doc/static/src/components/doc_copyable_pre.js`
- `addons/api_doc/static/src/components/doc_error_dialog.js`
- `addons/api_doc/static/src/components/doc_loading_indicator.js`
- `addons/api_doc/static/src/components/doc_method.js`
- `addons/api_doc/static/src/components/doc_method.xml`
- `addons/api_doc/static/src/components/doc_modal_api_key.js`
- `addons/api_doc/static/src/components/doc_modal_api_key.xml`
- `addons/api_doc/static/src/components/doc_modal_search.js`
- `addons/api_doc/static/src/components/doc_modal_search.xml`
- `addons/api_doc/static/src/components/doc_model.js`
- `addons/api_doc/static/src/components/doc_model.xml`
- `addons/api_doc/static/src/components/doc_request.js`
- `addons/api_doc/static/src/components/doc_request.xml`
- `addons/api_doc/static/src/components/doc_sidebar.js`
- `addons/api_doc/static/src/components/doc_sidebar.xml`
- `addons/api_doc/static/src/components/doc_table.js`
- `addons/api_doc/static/src/components/doc_table.xml`
- `addons/api_doc/static/src/doc_client.css`
- `addons/api_doc/static/src/doc_client.js`
- `addons/api_doc/static/src/doc_client.xml`
- `addons/api_doc/static/src/doc_model_store.js`
- `addons/api_doc/static/src/main.js`
- `addons/api_doc/static/src/start_doc_client.js`
- `addons/api_doc/static/src/utils/doc_code_gen.js`
- `addons/api_doc/static/src/utils/doc_model_search.js`
- `addons/api_doc/static/src/utils/doc_model_utils.js`
- `addons/api_doc/static/src/utils/doc_ui_store.js`
- `addons/api_doc/static/tests/api_doc.test.js`
- `addons/api_doc/static/tests/doc_test_helpers.js`
- `addons/api_doc/tests/__init__.py`
- `addons/api_doc/tests/dummy_methods.py`
- `addons/api_doc/tests/test_api_doc_tour.py`
- `addons/api_doc/tests/test_doc.py`
- `addons/api_doc/views/docclient.xml`
