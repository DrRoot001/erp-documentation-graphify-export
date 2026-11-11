# Module: website_crm_livechat

- **Module ID:** MOD-602
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_crm_livechat`
- **Manifest:** `addons/website_crm_livechat/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** View livechat sessions for leads

**Manifest description:**

Adds a stat button on lead form view to access their livechat sessions.

**Scope evidence:** The module contains 58 files, including 8 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `website_crm`, `website_livechat`, `crm_livechat`.

## 2. Module structure

- Model/business logic files: 3
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

- **Description:** 3 model declarations, 5 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/website_crm_livechat/models/discuss_channel.py:7`, `addons/website_crm_livechat/models/crm_lead.py:7`, `addons/website_crm_livechat/models/chatbot_script_step.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 1 record/template/menu identifiers.
- **Evidence:** `addons/website_crm_livechat/views/website_crm_lead_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_crm_livechat/tests/test_chatbot_lead_website.py`, `addons/website_crm_livechat/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `crm_lead_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/website_crm_livechat/views/website_crm_lead_views.xml:5`, `addons/website_crm_livechat/views/website_crm_lead_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_crm_livechat/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `discuss.channel` (addons/website_crm_livechat/models/discuss_channel.py:7); inherits `crm.lead` (addons/website_crm_livechat/models/crm_lead.py:7); inherits `chatbot.script.step` (addons/website_crm_livechat/models/chatbot_script_step.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_crm`, `website_livechat`, `crm_livechat`
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

- `addons/website_crm_livechat/__init__.py`
- `addons/website_crm_livechat/__manifest__.py`
- `addons/website_crm_livechat/i18n/ar.po`
- `addons/website_crm_livechat/i18n/az.po`
- `addons/website_crm_livechat/i18n/bg.po`
- `addons/website_crm_livechat/i18n/bs.po`
- `addons/website_crm_livechat/i18n/ca.po`
- `addons/website_crm_livechat/i18n/cs.po`
- `addons/website_crm_livechat/i18n/da.po`
- `addons/website_crm_livechat/i18n/de.po`
- `addons/website_crm_livechat/i18n/el.po`
- `addons/website_crm_livechat/i18n/es.po`
- `addons/website_crm_livechat/i18n/es_419.po`
- `addons/website_crm_livechat/i18n/et.po`
- `addons/website_crm_livechat/i18n/fa.po`
- `addons/website_crm_livechat/i18n/fi.po`
- `addons/website_crm_livechat/i18n/fr.po`
- `addons/website_crm_livechat/i18n/he.po`
- `addons/website_crm_livechat/i18n/hi.po`
- `addons/website_crm_livechat/i18n/hr.po`
- `addons/website_crm_livechat/i18n/hu.po`
- `addons/website_crm_livechat/i18n/id.po`
- `addons/website_crm_livechat/i18n/it.po`
- `addons/website_crm_livechat/i18n/ja.po`
- `addons/website_crm_livechat/i18n/kab.po`
- `addons/website_crm_livechat/i18n/ko.po`
- `addons/website_crm_livechat/i18n/ku.po`
- `addons/website_crm_livechat/i18n/lo.po`
- `addons/website_crm_livechat/i18n/lt.po`
- `addons/website_crm_livechat/i18n/lv.po`
- `addons/website_crm_livechat/i18n/mn.po`
- `addons/website_crm_livechat/i18n/my.po`
- `addons/website_crm_livechat/i18n/nb.po`
- `addons/website_crm_livechat/i18n/nl.po`
- `addons/website_crm_livechat/i18n/pl.po`
- `addons/website_crm_livechat/i18n/pt.po`
- `addons/website_crm_livechat/i18n/pt_BR.po`
- `addons/website_crm_livechat/i18n/ro.po`
- `addons/website_crm_livechat/i18n/ru.po`
- `addons/website_crm_livechat/i18n/sk.po`
- `addons/website_crm_livechat/i18n/sl.po`
- `addons/website_crm_livechat/i18n/sr@latin.po`
- `addons/website_crm_livechat/i18n/sv.po`
- `addons/website_crm_livechat/i18n/th.po`
- `addons/website_crm_livechat/i18n/tr.po`
- `addons/website_crm_livechat/i18n/uk.po`
- `addons/website_crm_livechat/i18n/uz.po`
- `addons/website_crm_livechat/i18n/vi.po`
- `addons/website_crm_livechat/i18n/website_crm_livechat.pot`
- `addons/website_crm_livechat/i18n/zh_CN.po`
- `addons/website_crm_livechat/i18n/zh_TW.po`
- `addons/website_crm_livechat/models/__init__.py`
- `addons/website_crm_livechat/models/chatbot_script_step.py`
- `addons/website_crm_livechat/models/crm_lead.py`
- `addons/website_crm_livechat/models/discuss_channel.py`
- `addons/website_crm_livechat/tests/__init__.py`
- `addons/website_crm_livechat/tests/test_chatbot_lead_website.py`
- `addons/website_crm_livechat/views/website_crm_lead_views.xml`
