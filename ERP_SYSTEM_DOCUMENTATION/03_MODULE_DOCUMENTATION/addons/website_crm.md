# Module: website_crm

- **Module ID:** MOD-600
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_crm`
- **Manifest:** `addons/website_crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate leads from a contact form

**Manifest description:**

Add capability to your website forms to generate leads or opportunities in the CRM app.
Forms has to be customized inside the *Website Builder* in order to generate leads.

This module includes contact phone and mobile numbers validation.

**Scope evidence:** The module contains 81 files, including 12 Python, 6 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `crm`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 6
- Browser asset files: 4
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_crm/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 24 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/website_crm/models/website_visitor.py:7`, `addons/website_crm/models/crm_lead.py:7`, `addons/website_crm/models/website.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/website_crm/controllers/website_form.py`, `addons/website_crm/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 4 JavaScript/TypeScript files; static XML analysis found 11 record/template/menu identifiers.
- **Evidence:** `addons/website_crm/data/ir_actions_data.xml:4`, `addons/website_crm/data/ir_actions_data.xml:10`, `addons/website_crm/data/ir_model_data.xml:4`, `addons/website_crm/data/crm_lead_merge_template.xml:4`, `addons/website_crm/views/website_visitor_views.xml:3`, `addons/website_crm/views/website_visitor_views.xml:18`, `addons/website_crm/views/website_visitor_views.xml:29`, `addons/website_crm/views/website_visitor_views.xml:43`, `addons/website_crm/views/crm_lead_views.xml:3`, `addons/website_crm/views/crm_lead_views.xml:18`, `addons/website_crm/views/website_templates_contactus.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_crm/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/website_crm/tests/test_website_visitor.py`, `addons/website_crm/tests/test_website_crm.py`, `addons/website_crm/tests/test_crm_lead_merge.py`, `addons/website_crm/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `action_open_website`, `base.open_menu`, `crm.model_crm_lead`, `crm_lead_merge_summary_inherit_website`, `website_visitor_view_form`, `website_visitor_view_tree`, `website_visitor_view_search`, `website_visitor_view_kanban`, `crm_lead_view_form`, `crm_lead_action_from_visitor`, `Contact Form (Opportunity)`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/website_crm/data/crm_lead_merge_template.xml:4`, `addons/website_crm/views/website_templates_contactus.xml:4`
- View/action field declarations: 12; representative evidence: `addons/website_crm/views/website_visitor_views.xml:5`, `addons/website_crm/views/website_visitor_views.xml:7`, `addons/website_crm/views/website_visitor_views.xml:20`, `addons/website_crm/views/website_visitor_views.xml:22`, `addons/website_crm/views/website_visitor_views.xml:31`, `addons/website_crm/views/website_visitor_views.xml:33`, `addons/website_crm/views/website_visitor_views.xml:45`, `addons/website_crm/views/website_visitor_views.xml:47`, `addons/website_crm/views/crm_lead_views.xml:5`, `addons/website_crm/views/crm_lead_views.xml:7`, `addons/website_crm/views/crm_lead_views.xml:20`, `addons/website_crm/views/crm_lead_views.xml:21`
- Browser assets: 4; representative files: `addons/website_crm/static/src/js/website_crm_editor.js`, `addons/website_crm/static/src/js/website_crm_editor.edit.js`, `addons/website_crm/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`, `addons/website_crm/static/tests/tours/website_crm.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_crm/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `website.visitor` (addons/website_crm/models/website_visitor.py:7); inherits `crm.lead` (addons/website_crm/models/crm_lead.py:7); inherits `website` (addons/website_crm/models/website.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `crm`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_crm/README.md`
- `addons/website_crm/__init__.py`
- `addons/website_crm/__manifest__.py`
- `addons/website_crm/controllers/__init__.py`
- `addons/website_crm/controllers/website_form.py`
- `addons/website_crm/data/crm_lead_merge_template.xml`
- `addons/website_crm/data/ir_actions_data.xml`
- `addons/website_crm/data/ir_model_data.xml`
- `addons/website_crm/i18n/af.po`
- `addons/website_crm/i18n/ar.po`
- `addons/website_crm/i18n/az.po`
- `addons/website_crm/i18n/bg.po`
- `addons/website_crm/i18n/bs.po`
- `addons/website_crm/i18n/ca.po`
- `addons/website_crm/i18n/cs.po`
- `addons/website_crm/i18n/da.po`
- `addons/website_crm/i18n/de.po`
- `addons/website_crm/i18n/el.po`
- `addons/website_crm/i18n/es.po`
- `addons/website_crm/i18n/es_419.po`
- `addons/website_crm/i18n/et.po`
- `addons/website_crm/i18n/fa.po`
- `addons/website_crm/i18n/fi.po`
- `addons/website_crm/i18n/fr.po`
- `addons/website_crm/i18n/gu.po`
- `addons/website_crm/i18n/he.po`
- `addons/website_crm/i18n/hi.po`
- `addons/website_crm/i18n/hr.po`
- `addons/website_crm/i18n/hu.po`
- `addons/website_crm/i18n/id.po`
- `addons/website_crm/i18n/is.po`
- `addons/website_crm/i18n/it.po`
- `addons/website_crm/i18n/ja.po`
- `addons/website_crm/i18n/kab.po`
- `addons/website_crm/i18n/km.po`
- `addons/website_crm/i18n/ko.po`
- `addons/website_crm/i18n/ku.po`
- `addons/website_crm/i18n/lo.po`
- `addons/website_crm/i18n/lt.po`
- `addons/website_crm/i18n/lv.po`
- `addons/website_crm/i18n/mk.po`
- `addons/website_crm/i18n/mn.po`
- `addons/website_crm/i18n/my.po`
- `addons/website_crm/i18n/nb.po`
- `addons/website_crm/i18n/nl.po`
- `addons/website_crm/i18n/pl.po`
- `addons/website_crm/i18n/pt.po`
- `addons/website_crm/i18n/pt_BR.po`
- `addons/website_crm/i18n/ro.po`
- `addons/website_crm/i18n/ru.po`
- `addons/website_crm/i18n/sk.po`
- `addons/website_crm/i18n/sl.po`
- `addons/website_crm/i18n/sr@latin.po`
- `addons/website_crm/i18n/sv.po`
- `addons/website_crm/i18n/th.po`
- `addons/website_crm/i18n/tr.po`
- `addons/website_crm/i18n/uk.po`
- `addons/website_crm/i18n/uz.po`
- `addons/website_crm/i18n/vi.po`
- `addons/website_crm/i18n/website_crm.pot`
- `addons/website_crm/i18n/zh_CN.po`
- `addons/website_crm/i18n/zh_TW.po`
- `addons/website_crm/models/__init__.py`
- `addons/website_crm/models/crm_lead.py`
- `addons/website_crm/models/website.py`
- `addons/website_crm/models/website_visitor.py`
- `addons/website_crm/security/ir.access.csv`
- `addons/website_crm/static/description/icon.png`
- `addons/website_crm/static/description/icon.svg`
- `addons/website_crm/static/description/icon_hi.png`
- `addons/website_crm/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`
- `addons/website_crm/static/src/js/website_crm_editor.edit.js`
- `addons/website_crm/static/src/js/website_crm_editor.js`
- `addons/website_crm/static/tests/tours/website_crm.js`
- `addons/website_crm/tests/__init__.py`
- `addons/website_crm/tests/test_crm_lead_merge.py`
- `addons/website_crm/tests/test_website_crm.py`
- `addons/website_crm/tests/test_website_visitor.py`
- `addons/website_crm/views/crm_lead_views.xml`
- `addons/website_crm/views/website_templates_contactus.xml`
- `addons/website_crm/views/website_visitor_views.xml`
