# Module: website_crm_partner_assign

- **Module ID:** MOD-603
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_crm_partner_assign`
- **Manifest:** `addons/website_crm_partner_assign/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Publish your resellers/partners and forward leads to them

**Manifest description:**

This module allows to forward incoming leads/opportunities to your resellers/partners.

Forwarding leads can be done for one or several leads at a time. The action is available in the *Assigned Partner* section of the lead/opportunity form view and in the *Action* menu of the list view.

The automatic assignment is figured from the weight of partner levels and the geolocalization. Partners get leads that are located around them.

**Scope evidence:** The module contains 110 files, including 19 Python, 17 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `base_geolocalize`, `crm`, `account`, `website_partnership`, `website_partner`, `website_google_map`, `portal`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 2
- XML/data/view/template files: 17
- Browser asset files: 2
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_crm_partner_assign/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 70 methods, 0 constraint handlers, 2 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/website_crm_partner_assign/models/res_partner_grade.py:7`, `addons/website_crm_partner_assign/models/res_partner.py:6`, `addons/website_crm_partner_assign/models/portal_entry.py:4`, `addons/website_crm_partner_assign/models/crm_lead.py:12`, `addons/website_crm_partner_assign/models/website.py:7`, `addons/website_crm_partner_assign/models/res_partner_activation.py:7`, `addons/website_crm_partner_assign/report/crm_partner_report.py:8`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner.py:11`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner.py:131`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 5 route declarations.
- **Evidence:** `addons/website_crm_partner_assign/controllers/main.py:43`, `addons/website_crm_partner_assign/controllers/main.py:86`, `addons/website_crm_partner_assign/controllers/main.py:155`, `addons/website_crm_partner_assign/controllers/main.py:161`, `addons/website_crm_partner_assign/controllers/main.py:334`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 17 XML files and 2 JavaScript/TypeScript files; static XML analysis found 67 record/template/menu identifiers.
- **Evidence:** `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:5`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:30`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:44`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:57`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:3`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:40`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:48`, `addons/website_crm_partner_assign/data/mail_template_data.xml:5`, `addons/website_crm_partner_assign/data/crm_lead_demo.xml:6`, `addons/website_crm_partner_assign/data/res_partner_activation_data.xml:3`, `addons/website_crm_partner_assign/data/res_partner_activation_data.xml:7`, `addons/website_crm_partner_assign/data/res_partner_activation_data.xml:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_crm_partner_assign/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/website_crm_partner_assign/tests/test_partner_assign.py`, `addons/website_crm_partner_assign/tests/test_website_crm_partner_technical_page.py`, `addons/website_crm_partner_assign/tests/__init__.py`, `addons/website_crm_partner_assign/tests/test_res_partner.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 17; representative identifiers: `view_report_crm_partner_assign_filter`, `view_report_crm_partner_assign_graph`, `action_report_crm_partner_assign`, `menu_report_crm_partner_assign_tree`, `crm_lead_forward_to_partner_form`, `crm_lead_forward_to_partner_act`, `action_crm_send_mass_forward`, `email_template_lead_forward_mail`, `crm_case_partner_assign_1`, `res_partner_activation_data_fully_operational`, `res_partner_activation_data_ramp_up`, `res_partner_activation_data_first_contact`, `tag_portal_lead_partner_unavailable`, `tag_portal_lead_is_spam`, `tag_portal_lead_own_opp`, `crm_lead_merge_summary_inherit_partner_assign`, `portal_entry_leads`, `portal_entry_opportunities`, `base.res_partner_3`, `base.res_partner_4`
- Menus: 3; representative evidence: `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:57`, `addons/website_crm_partner_assign/views/website_page_views.xml:63`, `addons/website_crm_partner_assign/views/partner_assign_menus.xml:4`
- Templates: 18; representative evidence: `addons/website_crm_partner_assign/data/crm_lead_merge_template.xml:4`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:5`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:11`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:64`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:85`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:91`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:143`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:172`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:180`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:186`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:194`, `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml:207`
- View/action field declarations: 58; representative evidence: `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:7`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:8`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:32`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:33`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:46`, `addons/website_crm_partner_assign/report/crm_partner_report_view.xml:48`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:5`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:6`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:42`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:43`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:50`, `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml:51`
- Browser assets: 2; representative files: `addons/website_crm_partner_assign/static/src/website_builder/website_crm_partner_assign_option.js`, `addons/website_crm_partner_assign/static/src/interactions/crm_partner_assign.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_crm_partner_assign/__manifest__.py`
- **HTTP entry points:** `addons/website_crm_partner_assign/controllers/main.py:43`, `addons/website_crm_partner_assign/controllers/main.py:86`, `addons/website_crm_partner_assign/controllers/main.py:155`, `addons/website_crm_partner_assign/controllers/main.py:161`, `addons/website_crm_partner_assign/controllers/main.py:334`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: `res.partner.grade` (addons/website_crm_partner_assign/models/res_partner_grade.py:7); inherits `res.partner` (addons/website_crm_partner_assign/models/res_partner.py:6); inherits `portal.entry` (addons/website_crm_partner_assign/models/portal_entry.py:4); inherits `crm.lead` (addons/website_crm_partner_assign/models/crm_lead.py:12); inherits `website` (addons/website_crm_partner_assign/models/website.py:7); `res.partner.activation` (addons/website_crm_partner_assign/models/res_partner_activation.py:7); `crm.partner.report.assign` (addons/website_crm_partner_assign/report/crm_partner_report.py:8); `crm.lead.forward.to.partner` (addons/website_crm_partner_assign/wizard/crm_forward_to_partner.py:11); `crm.lead.assignation` (addons/website_crm_partner_assign/wizard/crm_forward_to_partner.py:131)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 5
- Route evidence: `addons/website_crm_partner_assign/controllers/main.py:43`, `addons/website_crm_partner_assign/controllers/main.py:86`, `addons/website_crm_partner_assign/controllers/main.py:155`, `addons/website_crm_partner_assign/controllers/main.py:161`, `addons/website_crm_partner_assign/controllers/main.py:334`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_geolocalize`, `crm`, `account`, `website_partnership`, `website_partner`, `website_google_map`, `portal`
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

- `addons/website_crm_partner_assign/__init__.py`
- `addons/website_crm_partner_assign/__manifest__.py`
- `addons/website_crm_partner_assign/controllers/__init__.py`
- `addons/website_crm_partner_assign/controllers/main.py`
- `addons/website_crm_partner_assign/data/crm_lead_demo.xml`
- `addons/website_crm_partner_assign/data/crm_lead_merge_template.xml`
- `addons/website_crm_partner_assign/data/crm_tag_data.xml`
- `addons/website_crm_partner_assign/data/mail_template_data.xml`
- `addons/website_crm_partner_assign/data/portal_entry_data.xml`
- `addons/website_crm_partner_assign/data/res_partner_activation_data.xml`
- `addons/website_crm_partner_assign/data/res_partner_demo.xml`
- `addons/website_crm_partner_assign/i18n/af.po`
- `addons/website_crm_partner_assign/i18n/am.po`
- `addons/website_crm_partner_assign/i18n/ar.po`
- `addons/website_crm_partner_assign/i18n/az.po`
- `addons/website_crm_partner_assign/i18n/bg.po`
- `addons/website_crm_partner_assign/i18n/bs.po`
- `addons/website_crm_partner_assign/i18n/ca.po`
- `addons/website_crm_partner_assign/i18n/cs.po`
- `addons/website_crm_partner_assign/i18n/da.po`
- `addons/website_crm_partner_assign/i18n/de.po`
- `addons/website_crm_partner_assign/i18n/el.po`
- `addons/website_crm_partner_assign/i18n/es.po`
- `addons/website_crm_partner_assign/i18n/es_419.po`
- `addons/website_crm_partner_assign/i18n/es_CL.po`
- `addons/website_crm_partner_assign/i18n/et.po`
- `addons/website_crm_partner_assign/i18n/eu.po`
- `addons/website_crm_partner_assign/i18n/fa.po`
- `addons/website_crm_partner_assign/i18n/fi.po`
- `addons/website_crm_partner_assign/i18n/fr.po`
- `addons/website_crm_partner_assign/i18n/fr_BE.po`
- `addons/website_crm_partner_assign/i18n/fr_CA.po`
- `addons/website_crm_partner_assign/i18n/gl.po`
- `addons/website_crm_partner_assign/i18n/gu.po`
- `addons/website_crm_partner_assign/i18n/he.po`
- `addons/website_crm_partner_assign/i18n/hi.po`
- `addons/website_crm_partner_assign/i18n/hr.po`
- `addons/website_crm_partner_assign/i18n/hu.po`
- `addons/website_crm_partner_assign/i18n/hy.po`
- `addons/website_crm_partner_assign/i18n/id.po`
- `addons/website_crm_partner_assign/i18n/is.po`
- `addons/website_crm_partner_assign/i18n/it.po`
- `addons/website_crm_partner_assign/i18n/ja.po`
- `addons/website_crm_partner_assign/i18n/ka.po`
- `addons/website_crm_partner_assign/i18n/kab.po`
- `addons/website_crm_partner_assign/i18n/kk.po`
- `addons/website_crm_partner_assign/i18n/km.po`
- `addons/website_crm_partner_assign/i18n/ko.po`
- `addons/website_crm_partner_assign/i18n/ku.po`
- `addons/website_crm_partner_assign/i18n/lo.po`
- `addons/website_crm_partner_assign/i18n/lt.po`
- `addons/website_crm_partner_assign/i18n/lv.po`
- `addons/website_crm_partner_assign/i18n/mk.po`
- `addons/website_crm_partner_assign/i18n/mn.po`
- `addons/website_crm_partner_assign/i18n/my.po`
- `addons/website_crm_partner_assign/i18n/nb.po`
- `addons/website_crm_partner_assign/i18n/nl.po`
- `addons/website_crm_partner_assign/i18n/pl.po`
- `addons/website_crm_partner_assign/i18n/pt.po`
- `addons/website_crm_partner_assign/i18n/pt_BR.po`
- `addons/website_crm_partner_assign/i18n/ro.po`
- `addons/website_crm_partner_assign/i18n/ru.po`
- `addons/website_crm_partner_assign/i18n/sk.po`
- `addons/website_crm_partner_assign/i18n/sl.po`
- `addons/website_crm_partner_assign/i18n/sq.po`
- `addons/website_crm_partner_assign/i18n/sr@latin.po`
- `addons/website_crm_partner_assign/i18n/sv.po`
- `addons/website_crm_partner_assign/i18n/ta.po`
- `addons/website_crm_partner_assign/i18n/th.po`
- `addons/website_crm_partner_assign/i18n/tr.po`
- `addons/website_crm_partner_assign/i18n/uk.po`
- `addons/website_crm_partner_assign/i18n/uz.po`
- `addons/website_crm_partner_assign/i18n/vi.po`
- `addons/website_crm_partner_assign/i18n/website_crm_partner_assign.pot`
- `addons/website_crm_partner_assign/i18n/zh_CN.po`
- `addons/website_crm_partner_assign/i18n/zh_TW.po`
- `addons/website_crm_partner_assign/models/__init__.py`
- `addons/website_crm_partner_assign/models/crm_lead.py`
- `addons/website_crm_partner_assign/models/portal_entry.py`
- `addons/website_crm_partner_assign/models/res_partner.py`
- `addons/website_crm_partner_assign/models/res_partner_activation.py`
- `addons/website_crm_partner_assign/models/res_partner_grade.py`
- `addons/website_crm_partner_assign/models/website.py`
- `addons/website_crm_partner_assign/report/__init__.py`
- `addons/website_crm_partner_assign/report/crm_partner_report.py`
- `addons/website_crm_partner_assign/report/crm_partner_report_view.xml`
- `addons/website_crm_partner_assign/security/ir.access.csv`
- `addons/website_crm_partner_assign/static/description/icon.png`
- `addons/website_crm_partner_assign/static/description/icon.svg`
- `addons/website_crm_partner_assign/static/description/icon_hi.png`
- `addons/website_crm_partner_assign/static/src/img/leads.svg`
- `addons/website_crm_partner_assign/static/src/img/quotation.svg`
- `addons/website_crm_partner_assign/static/src/interactions/crm_partner_assign.js`
- `addons/website_crm_partner_assign/static/src/scss/crm_partner_assign.scss`
- `addons/website_crm_partner_assign/static/src/website_builder/website_crm_partner_assign_option.js`
- `addons/website_crm_partner_assign/static/src/website_builder/website_crm_partner_assign_option.xml`
- `addons/website_crm_partner_assign/tests/__init__.py`
- `addons/website_crm_partner_assign/tests/test_partner_assign.py`
- `addons/website_crm_partner_assign/tests/test_res_partner.py`
- `addons/website_crm_partner_assign/tests/test_website_crm_partner_technical_page.py`
- `addons/website_crm_partner_assign/views/crm_lead_views.xml`
- `addons/website_crm_partner_assign/views/partner_assign_menus.xml`
- `addons/website_crm_partner_assign/views/res_partner_activation_views.xml`
- `addons/website_crm_partner_assign/views/res_partner_grade_views.xml`
- `addons/website_crm_partner_assign/views/res_partner_views.xml`
- `addons/website_crm_partner_assign/views/website_crm_partner_assign_templates.xml`
- `addons/website_crm_partner_assign/views/website_page_views.xml`
- `addons/website_crm_partner_assign/wizard/__init__.py`
- `addons/website_crm_partner_assign/wizard/crm_forward_to_partner.py`
- `addons/website_crm_partner_assign/wizard/crm_forward_to_partner_view.xml`
