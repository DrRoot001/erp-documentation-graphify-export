# Module: website_event_crm

- **Module ID:** MOD-611
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_event_crm`
- **Manifest:** `addons/website_event_crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allow per-order lead creation mode

**Scope evidence:** The module contains 58 files, including 7 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `event_crm`, `website_event`.

## 2. Module structure

- Model/business logic files: 1
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

- **Description:** 1 model declarations, 7 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_event_crm/models/event_registration.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/website_event_crm/data/event_crm_demo.xml:5`, `addons/website_event_crm/views/event_lead_rule_views.xml:3`, `addons/website_event_crm/views/event_lead_rule_views.xml:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_event_crm/tests/test_event_registration.py`, `addons/website_event_crm/tests/test_visitor_propagation.py`, `addons/website_event_crm/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `event_lead_rule_1`, `event_lead_rule_view_tree`, `event_lead_rule_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/website_event_crm/views/event_lead_rule_views.xml:5`, `addons/website_event_crm/views/event_lead_rule_views.xml:7`, `addons/website_event_crm/views/event_lead_rule_views.xml:15`, `addons/website_event_crm/views/event_lead_rule_views.xml:17`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_event_crm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `event.registration` (addons/website_event_crm/models/event_registration.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_crm`, `website_event`
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

- `addons/website_event_crm/__init__.py`
- `addons/website_event_crm/__manifest__.py`
- `addons/website_event_crm/data/event_crm_demo.xml`
- `addons/website_event_crm/i18n/ar.po`
- `addons/website_event_crm/i18n/az.po`
- `addons/website_event_crm/i18n/bg.po`
- `addons/website_event_crm/i18n/bs.po`
- `addons/website_event_crm/i18n/ca.po`
- `addons/website_event_crm/i18n/cs.po`
- `addons/website_event_crm/i18n/da.po`
- `addons/website_event_crm/i18n/de.po`
- `addons/website_event_crm/i18n/el.po`
- `addons/website_event_crm/i18n/es.po`
- `addons/website_event_crm/i18n/es_419.po`
- `addons/website_event_crm/i18n/et.po`
- `addons/website_event_crm/i18n/fa.po`
- `addons/website_event_crm/i18n/fi.po`
- `addons/website_event_crm/i18n/fr.po`
- `addons/website_event_crm/i18n/he.po`
- `addons/website_event_crm/i18n/hi.po`
- `addons/website_event_crm/i18n/hr.po`
- `addons/website_event_crm/i18n/hu.po`
- `addons/website_event_crm/i18n/id.po`
- `addons/website_event_crm/i18n/it.po`
- `addons/website_event_crm/i18n/ja.po`
- `addons/website_event_crm/i18n/kab.po`
- `addons/website_event_crm/i18n/ko.po`
- `addons/website_event_crm/i18n/ku.po`
- `addons/website_event_crm/i18n/lo.po`
- `addons/website_event_crm/i18n/lt.po`
- `addons/website_event_crm/i18n/lv.po`
- `addons/website_event_crm/i18n/mn.po`
- `addons/website_event_crm/i18n/my.po`
- `addons/website_event_crm/i18n/nb.po`
- `addons/website_event_crm/i18n/nl.po`
- `addons/website_event_crm/i18n/pl.po`
- `addons/website_event_crm/i18n/pt.po`
- `addons/website_event_crm/i18n/pt_BR.po`
- `addons/website_event_crm/i18n/ro.po`
- `addons/website_event_crm/i18n/ru.po`
- `addons/website_event_crm/i18n/sk.po`
- `addons/website_event_crm/i18n/sl.po`
- `addons/website_event_crm/i18n/sr@latin.po`
- `addons/website_event_crm/i18n/sv.po`
- `addons/website_event_crm/i18n/th.po`
- `addons/website_event_crm/i18n/tr.po`
- `addons/website_event_crm/i18n/uk.po`
- `addons/website_event_crm/i18n/uz.po`
- `addons/website_event_crm/i18n/vi.po`
- `addons/website_event_crm/i18n/website_event_crm.pot`
- `addons/website_event_crm/i18n/zh_CN.po`
- `addons/website_event_crm/i18n/zh_TW.po`
- `addons/website_event_crm/models/__init__.py`
- `addons/website_event_crm/models/event_registration.py`
- `addons/website_event_crm/tests/__init__.py`
- `addons/website_event_crm/tests/test_event_registration.py`
- `addons/website_event_crm/tests/test_visitor_propagation.py`
- `addons/website_event_crm/views/event_lead_rule_views.xml`
