# Module: data_recycle

- **Module ID:** MOD-061
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/data_recycle`
- **Manifest:** `addons/data_recycle/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Productivity/Data Cleaning`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Find old records and archive/delete them

**Manifest description:**

Find old records and archive/delete them

**Scope evidence:** The module contains 69 files, including 7 Python, 6 XML, and 3 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 3
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 4
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/data_recycle/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 28 methods, 1 constraint handlers, 1 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/data_recycle/models/data_recycle_record.py:9`, `addons/data_recycle/models/data_recycle_model.py:19`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 3 JavaScript/TypeScript files; static XML analysis found 14 record/template/menu identifiers.
- **Evidence:** `addons/data_recycle/data/ir_cron_data.xml:3`, `addons/data_recycle/views/data_cleaning_menu.xml:3`, `addons/data_recycle/views/data_cleaning_menu.xml:9`, `addons/data_recycle/views/data_cleaning_menu.xml:16`, `addons/data_recycle/views/data_cleaning_menu.xml:22`, `addons/data_recycle/views/data_cleaning_menu.xml:28`, `addons/data_recycle/views/data_recycle_record_views.xml:4`, `addons/data_recycle/views/data_recycle_record_views.xml:26`, `addons/data_recycle/views/data_recycle_record_views.xml:39`, `addons/data_recycle/views/data_recycle_record_views.xml:56`, `addons/data_recycle/views/data_recycle_templates.xml:3`, `addons/data_recycle/views/data_recycle_model_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/data_recycle/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 4 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/data_recycle/__manifest__.py`, `addons/data_recycle/models/data_recycle_model.py`, `addons/data_recycle/data/ir_cron_data.xml`, `addons/data_recycle/tests/test_data_recycle.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/data_recycle/tests/test_data_recycle.py`, `addons/data_recycle/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `ir_cron_clean_records`, `Data Cleaning`, `Recycle Records`, `Configuration`, `Rules`, `Recycle Records`, `view_data_recycle_record_list`, `view_data_recycle_record_search`, `action_data_recycle_record`, `action_data_recycle_record_notification`, `notification`, `view_data_recycle_model_list`, `view_data_merge_model_form`, `action_data_recycle_config`
- Menus: 5; representative evidence: `addons/data_recycle/views/data_cleaning_menu.xml:3`, `addons/data_recycle/views/data_cleaning_menu.xml:9`, `addons/data_recycle/views/data_cleaning_menu.xml:16`, `addons/data_recycle/views/data_cleaning_menu.xml:22`, `addons/data_recycle/views/data_cleaning_menu.xml:28`
- Templates: 1; representative evidence: `addons/data_recycle/views/data_recycle_templates.xml:3`
- View/action field declarations: 14; representative evidence: `addons/data_recycle/views/data_recycle_record_views.xml:6`, `addons/data_recycle/views/data_recycle_record_views.xml:7`, `addons/data_recycle/views/data_recycle_record_views.xml:28`, `addons/data_recycle/views/data_recycle_record_views.xml:29`, `addons/data_recycle/views/data_recycle_record_views.xml:42`, `addons/data_recycle/views/data_recycle_record_views.xml:43`, `addons/data_recycle/views/data_recycle_record_views.xml:58`, `addons/data_recycle/views/data_recycle_record_views.xml:59`, `addons/data_recycle/views/data_recycle_model_views.xml:6`, `addons/data_recycle/views/data_recycle_model_views.xml:7`, `addons/data_recycle/views/data_recycle_model_views.xml:20`, `addons/data_recycle/views/data_recycle_model_views.xml:21`
- Browser assets: 3; representative files: `addons/data_recycle/static/src/cog_menu/data_refresh_cog_menu.js`, `addons/data_recycle/static/src/views/data_recycle_list_view.js`, `addons/data_recycle/static/src/views/data_cleaning_common_list.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/data_recycle/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/data_recycle/__manifest__.py`, `addons/data_recycle/models/data_recycle_model.py`, `addons/data_recycle/data/ir_cron_data.xml`, `addons/data_recycle/tests/test_data_recycle.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: `data_recycle.record` (addons/data_recycle/models/data_recycle_record.py:9); `data_recycle.model` (addons/data_recycle/models/data_recycle_model.py:19)
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
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/data_recycle/__init__.py`
- `addons/data_recycle/__manifest__.py`
- `addons/data_recycle/data/ir_cron_data.xml`
- `addons/data_recycle/i18n/ar.po`
- `addons/data_recycle/i18n/az.po`
- `addons/data_recycle/i18n/bg.po`
- `addons/data_recycle/i18n/bs.po`
- `addons/data_recycle/i18n/ca.po`
- `addons/data_recycle/i18n/cs.po`
- `addons/data_recycle/i18n/da.po`
- `addons/data_recycle/i18n/data_recycle.pot`
- `addons/data_recycle/i18n/de.po`
- `addons/data_recycle/i18n/el.po`
- `addons/data_recycle/i18n/es.po`
- `addons/data_recycle/i18n/es_419.po`
- `addons/data_recycle/i18n/et.po`
- `addons/data_recycle/i18n/fa.po`
- `addons/data_recycle/i18n/fi.po`
- `addons/data_recycle/i18n/fr.po`
- `addons/data_recycle/i18n/he.po`
- `addons/data_recycle/i18n/hi.po`
- `addons/data_recycle/i18n/hr.po`
- `addons/data_recycle/i18n/hu.po`
- `addons/data_recycle/i18n/id.po`
- `addons/data_recycle/i18n/it.po`
- `addons/data_recycle/i18n/ja.po`
- `addons/data_recycle/i18n/kab.po`
- `addons/data_recycle/i18n/ko.po`
- `addons/data_recycle/i18n/ku.po`
- `addons/data_recycle/i18n/lo.po`
- `addons/data_recycle/i18n/lt.po`
- `addons/data_recycle/i18n/lv.po`
- `addons/data_recycle/i18n/mn.po`
- `addons/data_recycle/i18n/my.po`
- `addons/data_recycle/i18n/nb.po`
- `addons/data_recycle/i18n/nl.po`
- `addons/data_recycle/i18n/pl.po`
- `addons/data_recycle/i18n/pt.po`
- `addons/data_recycle/i18n/pt_BR.po`
- `addons/data_recycle/i18n/ro.po`
- `addons/data_recycle/i18n/ru.po`
- `addons/data_recycle/i18n/sk.po`
- `addons/data_recycle/i18n/sl.po`
- `addons/data_recycle/i18n/sr@latin.po`
- `addons/data_recycle/i18n/sv.po`
- `addons/data_recycle/i18n/th.po`
- `addons/data_recycle/i18n/tr.po`
- `addons/data_recycle/i18n/uk.po`
- `addons/data_recycle/i18n/uz.po`
- `addons/data_recycle/i18n/vi.po`
- `addons/data_recycle/i18n/zh_CN.po`
- `addons/data_recycle/i18n/zh_TW.po`
- `addons/data_recycle/models/__init__.py`
- `addons/data_recycle/models/data_recycle_model.py`
- `addons/data_recycle/models/data_recycle_record.py`
- `addons/data_recycle/security/ir.access.csv`
- `addons/data_recycle/static/description/icon.png`
- `addons/data_recycle/static/description/icon.svg`
- `addons/data_recycle/static/description/icon_hi.png`
- `addons/data_recycle/static/src/cog_menu/data_refresh_cog_menu.js`
- `addons/data_recycle/static/src/cog_menu/data_refresh_cog_menu.xml`
- `addons/data_recycle/static/src/views/data_cleaning_common_list.js`
- `addons/data_recycle/static/src/views/data_recycle_list_view.js`
- `addons/data_recycle/tests/__init__.py`
- `addons/data_recycle/tests/test_data_recycle.py`
- `addons/data_recycle/views/data_cleaning_menu.xml`
- `addons/data_recycle/views/data_recycle_model_views.xml`
- `addons/data_recycle/views/data_recycle_record_views.xml`
- `addons/data_recycle/views/data_recycle_templates.xml`
