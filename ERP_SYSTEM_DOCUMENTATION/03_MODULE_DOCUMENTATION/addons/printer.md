# Module: printer

- **Module ID:** MOD-468
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/printer`
- **Manifest:** `addons/printer/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `not declared`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Base module to manage external printers (e.g. ePOS, ZPL)

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 75 files, including 10 Python, 5 XML, and 10 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 10
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/printer/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 24 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/printer/models/printer.py:4`, `addons/printer/models/ir_actions_report.py:40`, `addons/printer/wizard/select_printers_wizard.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 10 JavaScript/TypeScript files; static XML analysis found 8 record/template/menu identifiers.
- **Evidence:** `addons/printer/demo/printers.xml:4`, `addons/printer/demo/printers.xml:9`, `addons/printer/wizard/select_printers_wizard.xml:3`, `addons/printer/views/ir_actions_report.xml:2`, `addons/printer/views/printer_views.xml:3`, `addons/printer/views/printer_views.xml:24`, `addons/printer/views/printer_views.xml:37`, `addons/printer/views/printer_views.xml:50`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/printer/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/printer/models/printer.py`, `addons/printer/models/ir_actions_report.py`, `addons/printer/views/ir_actions_report.xml`, `addons/printer/tests/test_get_print_jobs.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/printer/tests/test_thermal_printer_format.py`, `addons/printer/tests/test_get_print_jobs.py`, `addons/printer/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `zebra_printer_demo`, `epos_printer_demo`, `view_select_printers_wizard`, `act_report_xml_view_printer`, `printer_view_form`, `manage_printers_action`, `printer_view_list`, `action_reset_linked_printers`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/printer/wizard/select_printers_wizard.xml:5`, `addons/printer/wizard/select_printers_wizard.xml:6`, `addons/printer/views/ir_actions_report.xml:4`, `addons/printer/views/ir_actions_report.xml:6`, `addons/printer/views/printer_views.xml:5`, `addons/printer/views/printer_views.xml:6`, `addons/printer/views/printer_views.xml:27`, `addons/printer/views/printer_views.xml:28`, `addons/printer/views/printer_views.xml:39`, `addons/printer/views/printer_views.xml:40`
- Browser assets: 10; representative files: `addons/printer/static/src/print_action_handler.js`, `addons/printer/static/src/services/report_printers_cache.js`, `addons/printer/static/src/@types/registry.d.ts`, `addons/printer/static/src/@types/services.d.ts`, `addons/printer/static/src/wizard/select_printers_wizard.js`, `addons/printer/static/src/client_actions/reset_cached_printers.js`, `addons/printer/static/tests/unit/print_action_handler.test.js`, `addons/printer/static/tests/tours/utils.js`, `addons/printer/static/tests/tours/test_print_label_zebra_tour.js`, `addons/printer/static/tests/tours/test_print_label_epos_tour.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/printer/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/printer/models/printer.py`, `addons/printer/models/ir_actions_report.py`, `addons/printer/views/ir_actions_report.xml`, `addons/printer/tests/test_get_print_jobs.py`

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: `printer.printer` (addons/printer/models/printer.py:4); inherits `ir.actions.report` (addons/printer/models/ir_actions_report.py:40); `select.printers.wizard` (addons/printer/wizard/select_printers_wizard.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
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

- `addons/printer/__init__.py`
- `addons/printer/__manifest__.py`
- `addons/printer/demo/printers.xml`
- `addons/printer/i18n/ar.po`
- `addons/printer/i18n/az.po`
- `addons/printer/i18n/bg.po`
- `addons/printer/i18n/bs.po`
- `addons/printer/i18n/ca.po`
- `addons/printer/i18n/cs.po`
- `addons/printer/i18n/da.po`
- `addons/printer/i18n/de.po`
- `addons/printer/i18n/el.po`
- `addons/printer/i18n/es.po`
- `addons/printer/i18n/es_419.po`
- `addons/printer/i18n/et.po`
- `addons/printer/i18n/fa.po`
- `addons/printer/i18n/fi.po`
- `addons/printer/i18n/fr.po`
- `addons/printer/i18n/he.po`
- `addons/printer/i18n/hi.po`
- `addons/printer/i18n/hr.po`
- `addons/printer/i18n/hu.po`
- `addons/printer/i18n/id.po`
- `addons/printer/i18n/it.po`
- `addons/printer/i18n/ja.po`
- `addons/printer/i18n/kab.po`
- `addons/printer/i18n/ko.po`
- `addons/printer/i18n/ku.po`
- `addons/printer/i18n/lo.po`
- `addons/printer/i18n/lt.po`
- `addons/printer/i18n/lv.po`
- `addons/printer/i18n/mn.po`
- `addons/printer/i18n/my.po`
- `addons/printer/i18n/nb.po`
- `addons/printer/i18n/nl.po`
- `addons/printer/i18n/pl.po`
- `addons/printer/i18n/printer.pot`
- `addons/printer/i18n/pt.po`
- `addons/printer/i18n/pt_BR.po`
- `addons/printer/i18n/ro.po`
- `addons/printer/i18n/ru.po`
- `addons/printer/i18n/sk.po`
- `addons/printer/i18n/sl.po`
- `addons/printer/i18n/sr@latin.po`
- `addons/printer/i18n/sv.po`
- `addons/printer/i18n/th.po`
- `addons/printer/i18n/tr.po`
- `addons/printer/i18n/uk.po`
- `addons/printer/i18n/uz.po`
- `addons/printer/i18n/vi.po`
- `addons/printer/i18n/zh_CN.po`
- `addons/printer/i18n/zh_TW.po`
- `addons/printer/models/__init__.py`
- `addons/printer/models/ir_actions_report.py`
- `addons/printer/models/printer.py`
- `addons/printer/security/ir.access.csv`
- `addons/printer/static/src/@types/registry.d.ts`
- `addons/printer/static/src/@types/services.d.ts`
- `addons/printer/static/src/client_actions/reset_cached_printers.js`
- `addons/printer/static/src/client_actions/reset_cached_printers.xml`
- `addons/printer/static/src/print_action_handler.js`
- `addons/printer/static/src/services/report_printers_cache.js`
- `addons/printer/static/src/wizard/select_printers_wizard.js`
- `addons/printer/static/tests/tours/test_print_label_epos_tour.js`
- `addons/printer/static/tests/tours/test_print_label_zebra_tour.js`
- `addons/printer/static/tests/tours/utils.js`
- `addons/printer/static/tests/unit/print_action_handler.test.js`
- `addons/printer/tests/__init__.py`
- `addons/printer/tests/test_get_print_jobs.py`
- `addons/printer/tests/test_thermal_printer_format.py`
- `addons/printer/views/ir_actions_report.xml`
- `addons/printer/views/printer_views.xml`
- `addons/printer/wizard/__init__.py`
- `addons/printer/wizard/select_printers_wizard.py`
- `addons/printer/wizard/select_printers_wizard.xml`
