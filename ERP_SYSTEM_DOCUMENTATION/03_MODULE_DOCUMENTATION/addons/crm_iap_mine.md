# Module: crm_iap_mine

- **Module ID:** MOD-056
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_iap_mine`
- **Manifest:** `addons/crm_iap_mine/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate Leads/Opportunities based on country, industries, size, etc.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 77 files, including 13 Python, 7 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `iap_crm`, `iap_mail`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 2
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/crm_iap_mine/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 39 methods, 0 constraint handlers, 5 onchange handlers, and 6 dependency declarations.
- **Evidence:** `addons/crm_iap_mine/models/crm_iap_lead_helpers.py:4`, `addons/crm_iap_mine/models/crm_iap_lead_industry.py:9`, `addons/crm_iap_mine/models/crm_iap_lead_role.py:7`, `addons/crm_iap_mine/models/crm_iap_lead_industry_division.py:6`, `addons/crm_iap_mine/models/crm_iap_lead_mining_request.py:21`, `addons/crm_iap_mine/models/crm_iap_lead_seniority.py:7`, `addons/crm_iap_mine/models/crm_lead.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 2 JavaScript/TypeScript files; static XML analysis found 12 record/template/menu identifiers.
- **Evidence:** `addons/crm_iap_mine/data/mail_template_data.xml:5`, `addons/crm_iap_mine/data/ir_sequence_data.xml:5`, `addons/crm_iap_mine/views/crm_menus.xml:4`, `addons/crm_iap_mine/views/crm_menus.xml:10`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:3`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:111`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:128`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:154`, `addons/crm_iap_mine/views/res_config_settings_views.xml:3`, `addons/crm_iap_mine/views/crm_iap_lead_industry_views.xml:3`, `addons/crm_iap_mine/views/crm_iap_lead_industry_views.xml:15`, `addons/crm_iap_mine/views/mail_templates.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/crm_iap_mine/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/crm_iap_mine/tests/test_lead_mine.py`, `addons/crm_iap_mine/tests/common.py`, `addons/crm_iap_mine/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `lead_generation_no_credits`, `ir_sequence_crm_iap_mine`, `Lead Generation`, `crm_iap_lead_mining_request_menu_action`, `crm_iap_lead_mining_request_view_form`, `crm_iap_lead_mining_request_view_tree`, `crm_iap_lead_mining_request_view_search`, `crm_iap_lead_mining_request_action`, `res_config_settings_view_form`, `crm_iap_lead_industry_view_search`, `crm_iap_lead_industry_view_tree`, `enrich_company`
- Menus: 2; representative evidence: `addons/crm_iap_mine/views/crm_menus.xml:4`, `addons/crm_iap_mine/views/crm_menus.xml:10`
- Templates: 1; representative evidence: `addons/crm_iap_mine/views/mail_templates.xml:4`
- View/action field declarations: 14; representative evidence: `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:5`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:6`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:113`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:114`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:130`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:131`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:156`, `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml:157`, `addons/crm_iap_mine/views/res_config_settings_views.xml:5`, `addons/crm_iap_mine/views/res_config_settings_views.xml:7`, `addons/crm_iap_mine/views/crm_iap_lead_industry_views.xml:5`, `addons/crm_iap_mine/views/crm_iap_lead_industry_views.xml:6`
- Browser assets: 2; representative files: `addons/crm_iap_mine/static/src/js/tours/crm_iap_lead.js`, `addons/crm_iap_mine/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_iap_mine/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `crm.iap.lead.helpers` (addons/crm_iap_mine/models/crm_iap_lead_helpers.py:4); `crm.iap.lead.industry` (addons/crm_iap_mine/models/crm_iap_lead_industry.py:9); `crm.iap.lead.role` (addons/crm_iap_mine/models/crm_iap_lead_role.py:7); `crm.iap.lead.industry.division` (addons/crm_iap_mine/models/crm_iap_lead_industry_division.py:6); `crm.iap.lead.mining.request` (addons/crm_iap_mine/models/crm_iap_lead_mining_request.py:21); `crm.iap.lead.seniority` (addons/crm_iap_mine/models/crm_iap_lead_seniority.py:7); inherits `crm.lead` (addons/crm_iap_mine/models/crm_lead.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `iap_crm`, `iap_mail`
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

- `addons/crm_iap_mine/__init__.py`
- `addons/crm_iap_mine/__manifest__.py`
- `addons/crm_iap_mine/data/crm.iap.lead.industry.csv`
- `addons/crm_iap_mine/data/crm.iap.lead.industry.division.csv`
- `addons/crm_iap_mine/data/crm.iap.lead.role.csv`
- `addons/crm_iap_mine/data/crm.iap.lead.seniority.csv`
- `addons/crm_iap_mine/data/ir_sequence_data.xml`
- `addons/crm_iap_mine/data/mail_template_data.xml`
- `addons/crm_iap_mine/i18n/ar.po`
- `addons/crm_iap_mine/i18n/az.po`
- `addons/crm_iap_mine/i18n/bg.po`
- `addons/crm_iap_mine/i18n/bs.po`
- `addons/crm_iap_mine/i18n/ca.po`
- `addons/crm_iap_mine/i18n/crm_iap_mine.pot`
- `addons/crm_iap_mine/i18n/cs.po`
- `addons/crm_iap_mine/i18n/da.po`
- `addons/crm_iap_mine/i18n/de.po`
- `addons/crm_iap_mine/i18n/el.po`
- `addons/crm_iap_mine/i18n/es.po`
- `addons/crm_iap_mine/i18n/es_419.po`
- `addons/crm_iap_mine/i18n/et.po`
- `addons/crm_iap_mine/i18n/fa.po`
- `addons/crm_iap_mine/i18n/fi.po`
- `addons/crm_iap_mine/i18n/fr.po`
- `addons/crm_iap_mine/i18n/he.po`
- `addons/crm_iap_mine/i18n/hi.po`
- `addons/crm_iap_mine/i18n/hr.po`
- `addons/crm_iap_mine/i18n/hu.po`
- `addons/crm_iap_mine/i18n/id.po`
- `addons/crm_iap_mine/i18n/it.po`
- `addons/crm_iap_mine/i18n/ja.po`
- `addons/crm_iap_mine/i18n/kab.po`
- `addons/crm_iap_mine/i18n/ko.po`
- `addons/crm_iap_mine/i18n/ku.po`
- `addons/crm_iap_mine/i18n/lo.po`
- `addons/crm_iap_mine/i18n/lt.po`
- `addons/crm_iap_mine/i18n/lv.po`
- `addons/crm_iap_mine/i18n/mn.po`
- `addons/crm_iap_mine/i18n/my.po`
- `addons/crm_iap_mine/i18n/nb.po`
- `addons/crm_iap_mine/i18n/nl.po`
- `addons/crm_iap_mine/i18n/pl.po`
- `addons/crm_iap_mine/i18n/pt.po`
- `addons/crm_iap_mine/i18n/pt_BR.po`
- `addons/crm_iap_mine/i18n/ro.po`
- `addons/crm_iap_mine/i18n/ru.po`
- `addons/crm_iap_mine/i18n/sk.po`
- `addons/crm_iap_mine/i18n/sl.po`
- `addons/crm_iap_mine/i18n/sr@latin.po`
- `addons/crm_iap_mine/i18n/sv.po`
- `addons/crm_iap_mine/i18n/th.po`
- `addons/crm_iap_mine/i18n/tr.po`
- `addons/crm_iap_mine/i18n/uk.po`
- `addons/crm_iap_mine/i18n/uz.po`
- `addons/crm_iap_mine/i18n/vi.po`
- `addons/crm_iap_mine/i18n/zh_CN.po`
- `addons/crm_iap_mine/i18n/zh_TW.po`
- `addons/crm_iap_mine/models/__init__.py`
- `addons/crm_iap_mine/models/crm_iap_lead_helpers.py`
- `addons/crm_iap_mine/models/crm_iap_lead_industry.py`
- `addons/crm_iap_mine/models/crm_iap_lead_industry_division.py`
- `addons/crm_iap_mine/models/crm_iap_lead_mining_request.py`
- `addons/crm_iap_mine/models/crm_iap_lead_role.py`
- `addons/crm_iap_mine/models/crm_iap_lead_seniority.py`
- `addons/crm_iap_mine/models/crm_lead.py`
- `addons/crm_iap_mine/security/ir.access.csv`
- `addons/crm_iap_mine/static/img/crunchbase.ico`
- `addons/crm_iap_mine/static/src/components/lead_generation_dropdown/crm_lead_gen_element.js`
- `addons/crm_iap_mine/static/src/js/tours/crm_iap_lead.js`
- `addons/crm_iap_mine/tests/__init__.py`
- `addons/crm_iap_mine/tests/common.py`
- `addons/crm_iap_mine/tests/test_lead_mine.py`
- `addons/crm_iap_mine/views/crm_iap_lead_industry_views.xml`
- `addons/crm_iap_mine/views/crm_iap_lead_mining_request_views.xml`
- `addons/crm_iap_mine/views/crm_menus.xml`
- `addons/crm_iap_mine/views/mail_templates.xml`
- `addons/crm_iap_mine/views/res_config_settings_views.xml`
