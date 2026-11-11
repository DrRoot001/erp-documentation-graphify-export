# Module: base_report_wkhtmltox

- **Module ID:** MOD-041
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_report_wkhtmltox`
- **Manifest:** `addons/base_report_wkhtmltox/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** wkhtmltopdf rendering engine

**Manifest description:**

This module is the implementation of the wkhtmltopdf and
wlhtmltoimage rendering engine for Odoo.

learn more about it here:
https://wkhtmltopdf.org/

**Scope evidence:** The module contains 55 files, including 6 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: None declared.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/base_report_wkhtmltox/models/ir_actions_report.py:127`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/base_report_wkhtmltox/models/ir_actions_report.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/base_report_wkhtmltox/tests/test_split_table.py`, `addons/base_report_wkhtmltox/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_report_wkhtmltox/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/base_report_wkhtmltox/models/ir_actions_report.py`

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `ir.actions.report` (addons/base_report_wkhtmltox/models/ir_actions_report.py:127)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: None declared
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/base_report_wkhtmltox/__init__.py`
- `addons/base_report_wkhtmltox/__manifest__.py`
- `addons/base_report_wkhtmltox/i18n/ar.po`
- `addons/base_report_wkhtmltox/i18n/az.po`
- `addons/base_report_wkhtmltox/i18n/base_report_wkhtmltox.pot`
- `addons/base_report_wkhtmltox/i18n/bg.po`
- `addons/base_report_wkhtmltox/i18n/bs.po`
- `addons/base_report_wkhtmltox/i18n/ca.po`
- `addons/base_report_wkhtmltox/i18n/cs.po`
- `addons/base_report_wkhtmltox/i18n/da.po`
- `addons/base_report_wkhtmltox/i18n/de.po`
- `addons/base_report_wkhtmltox/i18n/el.po`
- `addons/base_report_wkhtmltox/i18n/es.po`
- `addons/base_report_wkhtmltox/i18n/es_419.po`
- `addons/base_report_wkhtmltox/i18n/et.po`
- `addons/base_report_wkhtmltox/i18n/fa.po`
- `addons/base_report_wkhtmltox/i18n/fi.po`
- `addons/base_report_wkhtmltox/i18n/fr.po`
- `addons/base_report_wkhtmltox/i18n/he.po`
- `addons/base_report_wkhtmltox/i18n/hi.po`
- `addons/base_report_wkhtmltox/i18n/hr.po`
- `addons/base_report_wkhtmltox/i18n/hu.po`
- `addons/base_report_wkhtmltox/i18n/id.po`
- `addons/base_report_wkhtmltox/i18n/it.po`
- `addons/base_report_wkhtmltox/i18n/ja.po`
- `addons/base_report_wkhtmltox/i18n/kab.po`
- `addons/base_report_wkhtmltox/i18n/ko.po`
- `addons/base_report_wkhtmltox/i18n/ku.po`
- `addons/base_report_wkhtmltox/i18n/lo.po`
- `addons/base_report_wkhtmltox/i18n/lt.po`
- `addons/base_report_wkhtmltox/i18n/lv.po`
- `addons/base_report_wkhtmltox/i18n/mn.po`
- `addons/base_report_wkhtmltox/i18n/my.po`
- `addons/base_report_wkhtmltox/i18n/nb.po`
- `addons/base_report_wkhtmltox/i18n/nl.po`
- `addons/base_report_wkhtmltox/i18n/pl.po`
- `addons/base_report_wkhtmltox/i18n/pt.po`
- `addons/base_report_wkhtmltox/i18n/pt_BR.po`
- `addons/base_report_wkhtmltox/i18n/ro.po`
- `addons/base_report_wkhtmltox/i18n/ru.po`
- `addons/base_report_wkhtmltox/i18n/sk.po`
- `addons/base_report_wkhtmltox/i18n/sl.po`
- `addons/base_report_wkhtmltox/i18n/sr@latin.po`
- `addons/base_report_wkhtmltox/i18n/sv.po`
- `addons/base_report_wkhtmltox/i18n/th.po`
- `addons/base_report_wkhtmltox/i18n/tr.po`
- `addons/base_report_wkhtmltox/i18n/uk.po`
- `addons/base_report_wkhtmltox/i18n/uz.po`
- `addons/base_report_wkhtmltox/i18n/vi.po`
- `addons/base_report_wkhtmltox/i18n/zh_CN.po`
- `addons/base_report_wkhtmltox/i18n/zh_TW.po`
- `addons/base_report_wkhtmltox/models/__init__.py`
- `addons/base_report_wkhtmltox/models/ir_actions_report.py`
- `addons/base_report_wkhtmltox/tests/__init__.py`
- `addons/base_report_wkhtmltox/tests/test_split_table.py`
