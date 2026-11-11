# Module: website_crm_iap_reveal

- **Module ID:** MOD-601
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_crm_iap_reveal`
- **Manifest:** `addons/website_crm_iap_reveal/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Generate Leads/Opportunities from your website's traffic

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 69 files, including 12 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `iap_crm`, `iap_mail`, `crm_iap_mine`, `website_crm`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_crm_iap_reveal/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 29 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_crm_iap_reveal/models/crm_reveal_rule.py:21`, `addons/website_crm_iap_reveal/models/ir_http.py:13`, `addons/website_crm_iap_reveal/models/crm_reveal_view.py:12`, `addons/website_crm_iap_reveal/models/crm_lead.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/website_crm_iap_reveal/controllers/website_form.py`, `addons/website_crm_iap_reveal/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 20 record/template/menu identifiers.
- **Evidence:** `addons/website_crm_iap_reveal/data/ir_cron_data.xml:5`, `addons/website_crm_iap_reveal/data/mail_templates.xml:3`, `addons/website_crm_iap_reveal/views/crm_menus.xml:3`, `addons/website_crm_iap_reveal/views/crm_menus.xml:9`, `addons/website_crm_iap_reveal/views/res_config_settings_views.xml:3`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:4`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:19`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:30`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:41`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:52`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:63`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:74`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_crm_iap_reveal/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_crm_iap_reveal/__manifest__.py`, `addons/website_crm_iap_reveal/data/ir_cron_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_crm_iap_reveal/tests/test_lead_reveal.py`, `addons/website_crm_iap_reveal/tests/common.py`, `addons/website_crm_iap_reveal/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `ir_cron_crm_reveal_lead`, `enrich_company`, `crm_reveal_rule_menu_action`, `crm_reveal_view_menu_action`, `res_config_settings_view_form`, `crm_reveal_lead_opportunity_form`, `crm_lead_view_pivot`, `crm_lead_view_graph`, `crm_lead_view_graph_report_opportunity`, `crm_lead_view_graph_report_lead`, `crm_lead_view_graph_report_forecast`, `crm_lead_view_pivot_forecast`, `crm_opportunity_report_view_pivot_lead`, `crm_reveal_rule_form`, `crm_reveal_rule_tree`, `crm_reveal_rule_view_search`, `crm_reveal_rule_action`, `crm_reveal_view_form`, `crm_reveal_view_tree`, `crm_reveal_view_action`
- Menus: 2; representative evidence: `addons/website_crm_iap_reveal/views/crm_menus.xml:3`, `addons/website_crm_iap_reveal/views/crm_menus.xml:9`
- Templates: 1; representative evidence: `addons/website_crm_iap_reveal/data/mail_templates.xml:3`
- View/action field declarations: 32; representative evidence: `addons/website_crm_iap_reveal/views/res_config_settings_views.xml:5`, `addons/website_crm_iap_reveal/views/res_config_settings_views.xml:7`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:6`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:8`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:21`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:23`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:32`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:34`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:43`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:45`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:54`, `addons/website_crm_iap_reveal/views/crm_lead_views.xml:56`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_crm_iap_reveal/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/website_crm_iap_reveal/__manifest__.py`, `addons/website_crm_iap_reveal/data/ir_cron_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `crm.reveal.rule` (addons/website_crm_iap_reveal/models/crm_reveal_rule.py:21); inherits `ir.http` (addons/website_crm_iap_reveal/models/ir_http.py:13); `crm.reveal.view` (addons/website_crm_iap_reveal/models/crm_reveal_view.py:12); inherits `crm.lead` (addons/website_crm_iap_reveal/models/crm_lead.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `iap_crm`, `iap_mail`, `crm_iap_mine`, `website_crm`
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

- `addons/website_crm_iap_reveal/__init__.py`
- `addons/website_crm_iap_reveal/__manifest__.py`
- `addons/website_crm_iap_reveal/controllers/__init__.py`
- `addons/website_crm_iap_reveal/controllers/website_form.py`
- `addons/website_crm_iap_reveal/data/ir_cron_data.xml`
- `addons/website_crm_iap_reveal/data/ir_model_data.xml`
- `addons/website_crm_iap_reveal/data/mail_templates.xml`
- `addons/website_crm_iap_reveal/i18n/ar.po`
- `addons/website_crm_iap_reveal/i18n/az.po`
- `addons/website_crm_iap_reveal/i18n/bg.po`
- `addons/website_crm_iap_reveal/i18n/bs.po`
- `addons/website_crm_iap_reveal/i18n/ca.po`
- `addons/website_crm_iap_reveal/i18n/cs.po`
- `addons/website_crm_iap_reveal/i18n/da.po`
- `addons/website_crm_iap_reveal/i18n/de.po`
- `addons/website_crm_iap_reveal/i18n/el.po`
- `addons/website_crm_iap_reveal/i18n/es.po`
- `addons/website_crm_iap_reveal/i18n/es_419.po`
- `addons/website_crm_iap_reveal/i18n/et.po`
- `addons/website_crm_iap_reveal/i18n/fa.po`
- `addons/website_crm_iap_reveal/i18n/fi.po`
- `addons/website_crm_iap_reveal/i18n/fr.po`
- `addons/website_crm_iap_reveal/i18n/he.po`
- `addons/website_crm_iap_reveal/i18n/hi.po`
- `addons/website_crm_iap_reveal/i18n/hr.po`
- `addons/website_crm_iap_reveal/i18n/hu.po`
- `addons/website_crm_iap_reveal/i18n/id.po`
- `addons/website_crm_iap_reveal/i18n/it.po`
- `addons/website_crm_iap_reveal/i18n/ja.po`
- `addons/website_crm_iap_reveal/i18n/kab.po`
- `addons/website_crm_iap_reveal/i18n/ko.po`
- `addons/website_crm_iap_reveal/i18n/ku.po`
- `addons/website_crm_iap_reveal/i18n/lo.po`
- `addons/website_crm_iap_reveal/i18n/lt.po`
- `addons/website_crm_iap_reveal/i18n/lv.po`
- `addons/website_crm_iap_reveal/i18n/mn.po`
- `addons/website_crm_iap_reveal/i18n/my.po`
- `addons/website_crm_iap_reveal/i18n/nb.po`
- `addons/website_crm_iap_reveal/i18n/nl.po`
- `addons/website_crm_iap_reveal/i18n/pl.po`
- `addons/website_crm_iap_reveal/i18n/pt.po`
- `addons/website_crm_iap_reveal/i18n/pt_BR.po`
- `addons/website_crm_iap_reveal/i18n/ro.po`
- `addons/website_crm_iap_reveal/i18n/ru.po`
- `addons/website_crm_iap_reveal/i18n/sk.po`
- `addons/website_crm_iap_reveal/i18n/sl.po`
- `addons/website_crm_iap_reveal/i18n/sr@latin.po`
- `addons/website_crm_iap_reveal/i18n/sv.po`
- `addons/website_crm_iap_reveal/i18n/th.po`
- `addons/website_crm_iap_reveal/i18n/tr.po`
- `addons/website_crm_iap_reveal/i18n/uk.po`
- `addons/website_crm_iap_reveal/i18n/uz.po`
- `addons/website_crm_iap_reveal/i18n/vi.po`
- `addons/website_crm_iap_reveal/i18n/website_crm_iap_reveal.pot`
- `addons/website_crm_iap_reveal/i18n/zh_CN.po`
- `addons/website_crm_iap_reveal/i18n/zh_TW.po`
- `addons/website_crm_iap_reveal/models/__init__.py`
- `addons/website_crm_iap_reveal/models/crm_lead.py`
- `addons/website_crm_iap_reveal/models/crm_reveal_rule.py`
- `addons/website_crm_iap_reveal/models/crm_reveal_view.py`
- `addons/website_crm_iap_reveal/models/ir_http.py`
- `addons/website_crm_iap_reveal/security/ir.access.csv`
- `addons/website_crm_iap_reveal/tests/__init__.py`
- `addons/website_crm_iap_reveal/tests/common.py`
- `addons/website_crm_iap_reveal/tests/test_lead_reveal.py`
- `addons/website_crm_iap_reveal/views/crm_lead_views.xml`
- `addons/website_crm_iap_reveal/views/crm_menus.xml`
- `addons/website_crm_iap_reveal/views/crm_reveal_views.xml`
- `addons/website_crm_iap_reveal/views/res_config_settings_views.xml`
