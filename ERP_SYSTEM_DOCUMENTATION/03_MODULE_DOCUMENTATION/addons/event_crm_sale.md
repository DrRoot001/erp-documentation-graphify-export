# Module: event_crm_sale

- **Module ID:** MOD-068
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event_crm_sale`
- **Manifest:** `addons/event_crm_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Add information of sale order linked to the registration for the creation of the lead.

**Scope evidence:** The module contains 56 files, including 6 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `event_crm`, `event_sale`.

## 2. Module structure

- Model/business logic files: 1
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

- **Description:** 1 model declarations, 2 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/event_crm_sale/models/event_registration.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/event_crm_sale/views/event_lead_rule_views.xml:3`, `addons/event_crm_sale/views/event_lead_rule_views.xml:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/event_crm_sale/tests/test_event_crm_flow.py`, `addons/event_crm_sale/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `event_lead_rule_view_tree`, `event_lead_rule_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/event_crm_sale/views/event_lead_rule_views.xml:5`, `addons/event_crm_sale/views/event_lead_rule_views.xml:7`, `addons/event_crm_sale/views/event_lead_rule_views.xml:15`, `addons/event_crm_sale/views/event_lead_rule_views.xml:17`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event_crm_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `event.registration` (addons/event_crm_sale/models/event_registration.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `event_crm`, `event_sale`
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

- `addons/event_crm_sale/__init__.py`
- `addons/event_crm_sale/__manifest__.py`
- `addons/event_crm_sale/i18n/ar.po`
- `addons/event_crm_sale/i18n/az.po`
- `addons/event_crm_sale/i18n/bg.po`
- `addons/event_crm_sale/i18n/bs.po`
- `addons/event_crm_sale/i18n/ca.po`
- `addons/event_crm_sale/i18n/cs.po`
- `addons/event_crm_sale/i18n/da.po`
- `addons/event_crm_sale/i18n/de.po`
- `addons/event_crm_sale/i18n/el.po`
- `addons/event_crm_sale/i18n/es.po`
- `addons/event_crm_sale/i18n/es_419.po`
- `addons/event_crm_sale/i18n/et.po`
- `addons/event_crm_sale/i18n/event_crm_sale.pot`
- `addons/event_crm_sale/i18n/fa.po`
- `addons/event_crm_sale/i18n/fi.po`
- `addons/event_crm_sale/i18n/fr.po`
- `addons/event_crm_sale/i18n/he.po`
- `addons/event_crm_sale/i18n/hi.po`
- `addons/event_crm_sale/i18n/hr.po`
- `addons/event_crm_sale/i18n/hu.po`
- `addons/event_crm_sale/i18n/id.po`
- `addons/event_crm_sale/i18n/it.po`
- `addons/event_crm_sale/i18n/ja.po`
- `addons/event_crm_sale/i18n/kab.po`
- `addons/event_crm_sale/i18n/ko.po`
- `addons/event_crm_sale/i18n/ku.po`
- `addons/event_crm_sale/i18n/lo.po`
- `addons/event_crm_sale/i18n/lt.po`
- `addons/event_crm_sale/i18n/lv.po`
- `addons/event_crm_sale/i18n/mn.po`
- `addons/event_crm_sale/i18n/my.po`
- `addons/event_crm_sale/i18n/nb.po`
- `addons/event_crm_sale/i18n/nl.po`
- `addons/event_crm_sale/i18n/pl.po`
- `addons/event_crm_sale/i18n/pt.po`
- `addons/event_crm_sale/i18n/pt_BR.po`
- `addons/event_crm_sale/i18n/ro.po`
- `addons/event_crm_sale/i18n/ru.po`
- `addons/event_crm_sale/i18n/sk.po`
- `addons/event_crm_sale/i18n/sl.po`
- `addons/event_crm_sale/i18n/sr@latin.po`
- `addons/event_crm_sale/i18n/sv.po`
- `addons/event_crm_sale/i18n/th.po`
- `addons/event_crm_sale/i18n/tr.po`
- `addons/event_crm_sale/i18n/uk.po`
- `addons/event_crm_sale/i18n/uz.po`
- `addons/event_crm_sale/i18n/vi.po`
- `addons/event_crm_sale/i18n/zh_CN.po`
- `addons/event_crm_sale/i18n/zh_TW.po`
- `addons/event_crm_sale/models/__init__.py`
- `addons/event_crm_sale/models/event_registration.py`
- `addons/event_crm_sale/tests/__init__.py`
- `addons/event_crm_sale/tests/test_event_crm_flow.py`
- `addons/event_crm_sale/views/event_lead_rule_views.xml`
