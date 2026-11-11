# Module: l10n_fr_hr_holidays

- **Module ID:** MOD-192
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_fr_hr_holidays`
- **Manifest:** `addons/l10n_fr_hr_holidays/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources/Time Off`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Management of leaves for part-time workers in France

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 14 files, including 10 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `hr_holidays`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 23 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/l10n_fr_hr_holidays/models/res_config_settings.py:7`, `addons/l10n_fr_hr_holidays/models/hr_leave.py:12`, `addons/l10n_fr_hr_holidays/models/hr_version.py:9`, `addons/l10n_fr_hr_holidays/models/res_company.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:3`, `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:15`, `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:28`, `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:33`, `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:42`, `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml:57`, `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml:3`, `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml:22`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/l10n_fr_hr_holidays/tests/test_french_leaves.py`, `addons/l10n_fr_hr_holidays/tests/test_french_work_entries.py`, `addons/l10n_fr_hr_holidays/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `l10n_fr_part_time_calendar`, `base.partner_demo_company_fr`, `base.demo_company_fr`, `l10n_fr_part_time_employee`, `hr_holidays.l10n_fr_work_entry_type_paid_time_off`, `l10n_fr_hr_holidays_allocation`, `res_config_settings_view_form`, `Settings`
- Menus: 1; representative evidence: `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml:22`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml:5`, `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_fr_hr_holidays/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.config.settings` (addons/l10n_fr_hr_holidays/models/res_config_settings.py:7); inherits `hr.leave` (addons/l10n_fr_hr_holidays/models/hr_leave.py:12); inherits `hr.version` (addons/l10n_fr_hr_holidays/models/hr_version.py:9); inherits `res.company` (addons/l10n_fr_hr_holidays/models/res_company.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `hr_holidays`
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

- `addons/l10n_fr_hr_holidays/__init__.py`
- `addons/l10n_fr_hr_holidays/__manifest__.py`
- `addons/l10n_fr_hr_holidays/data/l10n_fr_hr_holidays_demo.xml`
- `addons/l10n_fr_hr_holidays/i18n/fr.po`
- `addons/l10n_fr_hr_holidays/i18n/l10n_fr_hr_holidays.pot`
- `addons/l10n_fr_hr_holidays/models/__init__.py`
- `addons/l10n_fr_hr_holidays/models/hr_leave.py`
- `addons/l10n_fr_hr_holidays/models/hr_version.py`
- `addons/l10n_fr_hr_holidays/models/res_company.py`
- `addons/l10n_fr_hr_holidays/models/res_config_settings.py`
- `addons/l10n_fr_hr_holidays/tests/__init__.py`
- `addons/l10n_fr_hr_holidays/tests/test_french_leaves.py`
- `addons/l10n_fr_hr_holidays/tests/test_french_work_entries.py`
- `addons/l10n_fr_hr_holidays/views/res_config_settings_views.xml`
