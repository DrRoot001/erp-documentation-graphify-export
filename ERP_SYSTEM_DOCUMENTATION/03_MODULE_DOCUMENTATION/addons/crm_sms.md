# Module: crm_sms

- **Module ID:** MOD-060
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_sms`
- **Manifest:** `addons/crm_sms/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add SMS capabilities to CRM

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 55 files, including 4 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `crm`, `sms`.

## 2. Module structure

- Model/business logic files: 0
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/crm_sms/security/ir.access.csv`

## 4. Functionalities

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 4 record/template/menu identifiers.
- **Evidence:** `addons/crm_sms/views/crm_lead_views.xml:4`, `addons/crm_sms/views/crm_lead_views.xml:17`, `addons/crm_sms/views/crm_lead_views.xml:30`, `addons/crm_sms/views/crm_lead_views.xml:44`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/crm_sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/crm_sms/tests/test_crm_lead.py`, `addons/crm_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `crm_lead_act_window_sms_composer_single`, `crm_lead_act_window_sms_composer_multi`, `crm_case_tree_view_oppor`, `crm_lead_view_tree_opportunity_reporting`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/crm_sms/views/crm_lead_views.xml:6`, `addons/crm_sms/views/crm_lead_views.xml:7`, `addons/crm_sms/views/crm_lead_views.xml:19`, `addons/crm_sms/views/crm_lead_views.xml:20`, `addons/crm_sms/views/crm_lead_views.xml:32`, `addons/crm_sms/views/crm_lead_views.xml:34`, `addons/crm_sms/views/crm_lead_views.xml:46`, `addons/crm_sms/views/crm_lead_views.xml:48`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 0
- Representative model evidence: No literal model metadata found
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `crm`, `sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Not found
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/crm_sms/__init__.py`
- `addons/crm_sms/__manifest__.py`
- `addons/crm_sms/i18n/ar.po`
- `addons/crm_sms/i18n/az.po`
- `addons/crm_sms/i18n/bg.po`
- `addons/crm_sms/i18n/bs.po`
- `addons/crm_sms/i18n/ca.po`
- `addons/crm_sms/i18n/crm_sms.pot`
- `addons/crm_sms/i18n/cs.po`
- `addons/crm_sms/i18n/da.po`
- `addons/crm_sms/i18n/de.po`
- `addons/crm_sms/i18n/el.po`
- `addons/crm_sms/i18n/es.po`
- `addons/crm_sms/i18n/es_419.po`
- `addons/crm_sms/i18n/et.po`
- `addons/crm_sms/i18n/fa.po`
- `addons/crm_sms/i18n/fi.po`
- `addons/crm_sms/i18n/fr.po`
- `addons/crm_sms/i18n/he.po`
- `addons/crm_sms/i18n/hi.po`
- `addons/crm_sms/i18n/hr.po`
- `addons/crm_sms/i18n/hu.po`
- `addons/crm_sms/i18n/id.po`
- `addons/crm_sms/i18n/it.po`
- `addons/crm_sms/i18n/ja.po`
- `addons/crm_sms/i18n/kab.po`
- `addons/crm_sms/i18n/ko.po`
- `addons/crm_sms/i18n/ku.po`
- `addons/crm_sms/i18n/lo.po`
- `addons/crm_sms/i18n/lt.po`
- `addons/crm_sms/i18n/lv.po`
- `addons/crm_sms/i18n/mn.po`
- `addons/crm_sms/i18n/my.po`
- `addons/crm_sms/i18n/nb.po`
- `addons/crm_sms/i18n/nl.po`
- `addons/crm_sms/i18n/pl.po`
- `addons/crm_sms/i18n/pt.po`
- `addons/crm_sms/i18n/pt_BR.po`
- `addons/crm_sms/i18n/ro.po`
- `addons/crm_sms/i18n/ru.po`
- `addons/crm_sms/i18n/sk.po`
- `addons/crm_sms/i18n/sl.po`
- `addons/crm_sms/i18n/sr@latin.po`
- `addons/crm_sms/i18n/sv.po`
- `addons/crm_sms/i18n/th.po`
- `addons/crm_sms/i18n/tr.po`
- `addons/crm_sms/i18n/uk.po`
- `addons/crm_sms/i18n/uz.po`
- `addons/crm_sms/i18n/vi.po`
- `addons/crm_sms/i18n/zh_CN.po`
- `addons/crm_sms/i18n/zh_TW.po`
- `addons/crm_sms/security/ir.access.csv`
- `addons/crm_sms/tests/__init__.py`
- `addons/crm_sms/tests/test_crm_lead.py`
- `addons/crm_sms/views/crm_lead_views.xml`
