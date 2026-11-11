# Module: base_install_request

- **Module ID:** MOD-039
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_install_request`
- **Manifest:** `addons/base_install_request/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allow internal users requesting a module installation
=====================================================

**Scope evidence:** The module contains 60 files, including 6 Python, 4 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 0
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_install_request/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 6 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/base_install_request/models/ir_module_module.py:7`, `addons/base_install_request/wizard/base_module_install_request.py:9`, `addons/base_install_request/wizard/base_module_install_request.py:71`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 0 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/base_install_request/wizard/base_module_install_request_views.xml:3`, `addons/base_install_request/wizard/base_module_install_request_views.xml:21`, `addons/base_install_request/wizard/base_module_install_request_views.xml:37`, `addons/base_install_request/data/mail_templates_module_install.xml:3`, `addons/base_install_request/data/mail_templates.xml:3`, `addons/base_install_request/views/ir_module_module_views.xml:3`, `addons/base_install_request/views/ir_module_module_views.xml:14`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_install_request/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base_module_install_request_view_form`, `base_module_install_review_view_form`, `action_base_module_install_review`, `base_install_request.base_module_install_review_description`, `mail_installation_request_template`, `ir_module_module_view_kanban`, `base.menu_management`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/base_install_request/data/mail_templates_module_install.xml:3`, `addons/base_install_request/data/mail_templates.xml:3`
- View/action field declarations: 8; representative evidence: `addons/base_install_request/wizard/base_module_install_request_views.xml:5`, `addons/base_install_request/wizard/base_module_install_request_views.xml:6`, `addons/base_install_request/wizard/base_module_install_request_views.xml:23`, `addons/base_install_request/wizard/base_module_install_request_views.xml:24`, `addons/base_install_request/wizard/base_module_install_request_views.xml:39`, `addons/base_install_request/wizard/base_module_install_request_views.xml:40`, `addons/base_install_request/views/ir_module_module_views.xml:5`, `addons/base_install_request/views/ir_module_module_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_install_request/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `ir.module.module` (addons/base_install_request/models/ir_module_module.py:7); `base.module.install.request` (addons/base_install_request/wizard/base_module_install_request.py:9); `base.module.install.review` (addons/base_install_request/wizard/base_module_install_request.py:71)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/base_install_request/__init__.py`
- `addons/base_install_request/__manifest__.py`
- `addons/base_install_request/data/mail_templates.xml`
- `addons/base_install_request/data/mail_templates_module_install.xml`
- `addons/base_install_request/i18n/ar.po`
- `addons/base_install_request/i18n/az.po`
- `addons/base_install_request/i18n/base_install_request.pot`
- `addons/base_install_request/i18n/bg.po`
- `addons/base_install_request/i18n/bs.po`
- `addons/base_install_request/i18n/ca.po`
- `addons/base_install_request/i18n/cs.po`
- `addons/base_install_request/i18n/da.po`
- `addons/base_install_request/i18n/de.po`
- `addons/base_install_request/i18n/el.po`
- `addons/base_install_request/i18n/es.po`
- `addons/base_install_request/i18n/es_419.po`
- `addons/base_install_request/i18n/et.po`
- `addons/base_install_request/i18n/fa.po`
- `addons/base_install_request/i18n/fi.po`
- `addons/base_install_request/i18n/fr.po`
- `addons/base_install_request/i18n/he.po`
- `addons/base_install_request/i18n/hi.po`
- `addons/base_install_request/i18n/hr.po`
- `addons/base_install_request/i18n/hu.po`
- `addons/base_install_request/i18n/id.po`
- `addons/base_install_request/i18n/it.po`
- `addons/base_install_request/i18n/ja.po`
- `addons/base_install_request/i18n/kab.po`
- `addons/base_install_request/i18n/ko.po`
- `addons/base_install_request/i18n/ku.po`
- `addons/base_install_request/i18n/lo.po`
- `addons/base_install_request/i18n/lt.po`
- `addons/base_install_request/i18n/lv.po`
- `addons/base_install_request/i18n/mn.po`
- `addons/base_install_request/i18n/my.po`
- `addons/base_install_request/i18n/nb.po`
- `addons/base_install_request/i18n/nl.po`
- `addons/base_install_request/i18n/pl.po`
- `addons/base_install_request/i18n/pt.po`
- `addons/base_install_request/i18n/pt_BR.po`
- `addons/base_install_request/i18n/ro.po`
- `addons/base_install_request/i18n/ru.po`
- `addons/base_install_request/i18n/sk.po`
- `addons/base_install_request/i18n/sl.po`
- `addons/base_install_request/i18n/sr@latin.po`
- `addons/base_install_request/i18n/sv.po`
- `addons/base_install_request/i18n/th.po`
- `addons/base_install_request/i18n/tr.po`
- `addons/base_install_request/i18n/uk.po`
- `addons/base_install_request/i18n/uz.po`
- `addons/base_install_request/i18n/vi.po`
- `addons/base_install_request/i18n/zh_CN.po`
- `addons/base_install_request/i18n/zh_TW.po`
- `addons/base_install_request/models/__init__.py`
- `addons/base_install_request/models/ir_module_module.py`
- `addons/base_install_request/security/ir.access.csv`
- `addons/base_install_request/views/ir_module_module_views.xml`
- `addons/base_install_request/wizard/__init__.py`
- `addons/base_install_request/wizard/base_module_install_request.py`
- `addons/base_install_request/wizard/base_module_install_request_views.xml`
