# Module: hr_address_extended

- **Module ID:** MOD-082
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_address_extended`
- **Manifest:** `addons/hr_address_extended/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Employees`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Centralize employee information

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 57 files, including 7 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr`, `base_address_extended`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 7 methods, 0 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/hr_address_extended/models/hr_version.py:4`, `addons/hr_address_extended/models/hr_employee.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/hr_address_extended/views/hr_employee_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_address_extended/tests/test_hr_version.py`, `addons/hr_address_extended/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `view_employee_form_inherit_address`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/hr_address_extended/views/hr_employee_views.xml:6`, `addons/hr_address_extended/views/hr_employee_views.xml:9`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_address_extended/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `hr.version` (addons/hr_address_extended/models/hr_version.py:4); inherits `hr.employee` (addons/hr_address_extended/models/hr_employee.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr`, `base_address_extended`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/hr_address_extended/__init__.py`
- `addons/hr_address_extended/__manifest__.py`
- `addons/hr_address_extended/i18n/ar.po`
- `addons/hr_address_extended/i18n/az.po`
- `addons/hr_address_extended/i18n/bg.po`
- `addons/hr_address_extended/i18n/bs.po`
- `addons/hr_address_extended/i18n/ca.po`
- `addons/hr_address_extended/i18n/cs.po`
- `addons/hr_address_extended/i18n/da.po`
- `addons/hr_address_extended/i18n/de.po`
- `addons/hr_address_extended/i18n/el.po`
- `addons/hr_address_extended/i18n/es.po`
- `addons/hr_address_extended/i18n/es_419.po`
- `addons/hr_address_extended/i18n/et.po`
- `addons/hr_address_extended/i18n/fa.po`
- `addons/hr_address_extended/i18n/fi.po`
- `addons/hr_address_extended/i18n/fr.po`
- `addons/hr_address_extended/i18n/he.po`
- `addons/hr_address_extended/i18n/hi.po`
- `addons/hr_address_extended/i18n/hr.po`
- `addons/hr_address_extended/i18n/hr_address_extended.pot`
- `addons/hr_address_extended/i18n/hu.po`
- `addons/hr_address_extended/i18n/id.po`
- `addons/hr_address_extended/i18n/it.po`
- `addons/hr_address_extended/i18n/ja.po`
- `addons/hr_address_extended/i18n/kab.po`
- `addons/hr_address_extended/i18n/ko.po`
- `addons/hr_address_extended/i18n/ku.po`
- `addons/hr_address_extended/i18n/lo.po`
- `addons/hr_address_extended/i18n/lt.po`
- `addons/hr_address_extended/i18n/lv.po`
- `addons/hr_address_extended/i18n/mn.po`
- `addons/hr_address_extended/i18n/my.po`
- `addons/hr_address_extended/i18n/nb.po`
- `addons/hr_address_extended/i18n/nl.po`
- `addons/hr_address_extended/i18n/pl.po`
- `addons/hr_address_extended/i18n/pt.po`
- `addons/hr_address_extended/i18n/pt_BR.po`
- `addons/hr_address_extended/i18n/ro.po`
- `addons/hr_address_extended/i18n/ru.po`
- `addons/hr_address_extended/i18n/sk.po`
- `addons/hr_address_extended/i18n/sl.po`
- `addons/hr_address_extended/i18n/sr@latin.po`
- `addons/hr_address_extended/i18n/sv.po`
- `addons/hr_address_extended/i18n/th.po`
- `addons/hr_address_extended/i18n/tr.po`
- `addons/hr_address_extended/i18n/uk.po`
- `addons/hr_address_extended/i18n/uz.po`
- `addons/hr_address_extended/i18n/vi.po`
- `addons/hr_address_extended/i18n/zh_CN.po`
- `addons/hr_address_extended/i18n/zh_TW.po`
- `addons/hr_address_extended/models/__init__.py`
- `addons/hr_address_extended/models/hr_employee.py`
- `addons/hr_address_extended/models/hr_version.py`
- `addons/hr_address_extended/tests/__init__.py`
- `addons/hr_address_extended/tests/test_hr_version.py`
- `addons/hr_address_extended/views/hr_employee_views.xml`
