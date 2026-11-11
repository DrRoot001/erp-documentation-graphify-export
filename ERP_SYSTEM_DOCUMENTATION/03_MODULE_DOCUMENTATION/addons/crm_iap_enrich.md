# Module: crm_iap_enrich

- **Module ID:** MOD-055
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_iap_enrich`
- **Manifest:** `addons/crm_iap_enrich/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Enrich Leads/Opportunities using email address domain

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 62 files, including 8 Python, 5 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `iap_crm`, `iap_mail`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 7
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 14 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/crm_iap_enrich/models/res_config_settings.py:7`, `addons/crm_iap_enrich/models/crm_lead.py:13`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 0 JavaScript/TypeScript files; static XML analysis found 6 record/template/menu identifiers.
- **Evidence:** `addons/crm_iap_enrich/data/ir_cron.xml:3`, `addons/crm_iap_enrich/data/mail_templates.xml:4`, `addons/crm_iap_enrich/data/mail_templates.xml:11`, `addons/crm_iap_enrich/data/ir_action.xml:4`, `addons/crm_iap_enrich/views/crm_lead_views.xml:3`, `addons/crm_iap_enrich/views/res_config_settings_view.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/crm_iap_enrich/__manifest__.py`, `addons/crm_iap_enrich/__init__.py`, `addons/crm_iap_enrich/models/res_config_settings.py`, `addons/crm_iap_enrich/models/crm_lead.py`, `addons/crm_iap_enrich/data/ir_cron.xml`, `addons/crm_iap_enrich/data/ir_action.xml`, `addons/crm_iap_enrich/tests/test_lead_enrich.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/crm_iap_enrich/tests/test_lead_enrich.py`, `addons/crm_iap_enrich/tests/test_crm_lead_merge.py`, `addons/crm_iap_enrich/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `ir_cron_lead_enrichment`, `mail_message_lead_enrich_notfound`, `mail_message_lead_enrich_no_email`, `action_enrich_mail`, `crm_lead_view_form`, `res_config_settings_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 2; representative evidence: `addons/crm_iap_enrich/data/mail_templates.xml:4`, `addons/crm_iap_enrich/data/mail_templates.xml:11`
- View/action field declarations: 4; representative evidence: `addons/crm_iap_enrich/views/crm_lead_views.xml:5`, `addons/crm_iap_enrich/views/crm_lead_views.xml:7`, `addons/crm_iap_enrich/views/res_config_settings_view.xml:6`, `addons/crm_iap_enrich/views/res_config_settings_view.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_iap_enrich/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/crm_iap_enrich/__manifest__.py`, `addons/crm_iap_enrich/__init__.py`, `addons/crm_iap_enrich/models/res_config_settings.py`, `addons/crm_iap_enrich/models/crm_lead.py`, `addons/crm_iap_enrich/data/ir_cron.xml`, `addons/crm_iap_enrich/data/ir_action.xml`, `addons/crm_iap_enrich/tests/test_lead_enrich.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.config.settings` (addons/crm_iap_enrich/models/res_config_settings.py:7); inherits `crm.lead` (addons/crm_iap_enrich/models/crm_lead.py:13)
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
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/crm_iap_enrich/__init__.py`
- `addons/crm_iap_enrich/__manifest__.py`
- `addons/crm_iap_enrich/data/ir_action.xml`
- `addons/crm_iap_enrich/data/ir_cron.xml`
- `addons/crm_iap_enrich/data/mail_templates.xml`
- `addons/crm_iap_enrich/i18n/ar.po`
- `addons/crm_iap_enrich/i18n/az.po`
- `addons/crm_iap_enrich/i18n/bg.po`
- `addons/crm_iap_enrich/i18n/bs.po`
- `addons/crm_iap_enrich/i18n/ca.po`
- `addons/crm_iap_enrich/i18n/crm_iap_enrich.pot`
- `addons/crm_iap_enrich/i18n/cs.po`
- `addons/crm_iap_enrich/i18n/da.po`
- `addons/crm_iap_enrich/i18n/de.po`
- `addons/crm_iap_enrich/i18n/el.po`
- `addons/crm_iap_enrich/i18n/es.po`
- `addons/crm_iap_enrich/i18n/es_419.po`
- `addons/crm_iap_enrich/i18n/et.po`
- `addons/crm_iap_enrich/i18n/fa.po`
- `addons/crm_iap_enrich/i18n/fi.po`
- `addons/crm_iap_enrich/i18n/fr.po`
- `addons/crm_iap_enrich/i18n/he.po`
- `addons/crm_iap_enrich/i18n/hi.po`
- `addons/crm_iap_enrich/i18n/hr.po`
- `addons/crm_iap_enrich/i18n/hu.po`
- `addons/crm_iap_enrich/i18n/id.po`
- `addons/crm_iap_enrich/i18n/it.po`
- `addons/crm_iap_enrich/i18n/ja.po`
- `addons/crm_iap_enrich/i18n/kab.po`
- `addons/crm_iap_enrich/i18n/ko.po`
- `addons/crm_iap_enrich/i18n/ku.po`
- `addons/crm_iap_enrich/i18n/lo.po`
- `addons/crm_iap_enrich/i18n/lt.po`
- `addons/crm_iap_enrich/i18n/lv.po`
- `addons/crm_iap_enrich/i18n/mn.po`
- `addons/crm_iap_enrich/i18n/my.po`
- `addons/crm_iap_enrich/i18n/nb.po`
- `addons/crm_iap_enrich/i18n/nl.po`
- `addons/crm_iap_enrich/i18n/pl.po`
- `addons/crm_iap_enrich/i18n/pt.po`
- `addons/crm_iap_enrich/i18n/pt_BR.po`
- `addons/crm_iap_enrich/i18n/ro.po`
- `addons/crm_iap_enrich/i18n/ru.po`
- `addons/crm_iap_enrich/i18n/sk.po`
- `addons/crm_iap_enrich/i18n/sl.po`
- `addons/crm_iap_enrich/i18n/sr@latin.po`
- `addons/crm_iap_enrich/i18n/sv.po`
- `addons/crm_iap_enrich/i18n/th.po`
- `addons/crm_iap_enrich/i18n/tr.po`
- `addons/crm_iap_enrich/i18n/uk.po`
- `addons/crm_iap_enrich/i18n/uz.po`
- `addons/crm_iap_enrich/i18n/vi.po`
- `addons/crm_iap_enrich/i18n/zh_CN.po`
- `addons/crm_iap_enrich/i18n/zh_TW.po`
- `addons/crm_iap_enrich/models/__init__.py`
- `addons/crm_iap_enrich/models/crm_lead.py`
- `addons/crm_iap_enrich/models/res_config_settings.py`
- `addons/crm_iap_enrich/tests/__init__.py`
- `addons/crm_iap_enrich/tests/test_crm_lead_merge.py`
- `addons/crm_iap_enrich/tests/test_lead_enrich.py`
- `addons/crm_iap_enrich/views/crm_lead_views.xml`
- `addons/crm_iap_enrich/views/res_config_settings_view.xml`
