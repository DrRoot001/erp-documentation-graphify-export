# Module: crm

- **Module ID:** MOD-054
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm`
- **Manifest:** `addons/crm/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Track leads and close opportunities

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 237 files, including 50 Python, 49 XML, and 48 JavaScript/TypeScript files. The manifest declares dependencies: `base_setup`, `base_install_request`, `sales_team`, `mail`, `calendar`, `resource`, `utm`, `web_tour`, `contacts`, `digest`, `phone_validation`.

## 2. Module structure

- Model/business logic files: 23
- Controller/API files: 3
- XML/data/view/template files: 49
- Browser asset files: 48
- Security files: 2
- Test files: 20
- Scheduled/automation evidence files: 11
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/crm/security/crm_security.xml`, `addons/crm/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 23 model declarations, 394 methods, 4 constraint handlers, 5 onchange handlers, and 49 dependency declarations.
- **Evidence:** `addons/crm/models/res_partner.py:6`, `addons/crm/models/ir_config_parameter.py:7`, `addons/crm/models/mail_activity.py:7`, `addons/crm/models/discuss_channel.py:7`, `addons/crm/models/digest.py:8`, `addons/crm/models/crm_recurring_plan.py:7`, `addons/crm/models/res_groups.py:6`, `addons/crm/models/res_config_settings.py:11`, `addons/crm/models/calendar.py:7`, `addons/crm/models/crm_team.py:19`, `addons/crm/models/utm.py:7`, `addons/crm/models/crm_stage.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 3 route declarations.
- **Evidence:** `addons/crm/controllers/main.py:13`, `addons/crm/controllers/main.py:24`, `addons/crm/controllers/main.py:35`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 49 XML files and 48 JavaScript/TypeScript files; static XML analysis found 268 record/template/menu identifiers.
- **Evidence:** `addons/crm/security/crm_security.xml:3`, `addons/crm/security/crm_security.xml:7`, `addons/crm/security/crm_security.xml:11`, `addons/crm/report/crm_opportunity_report_views.xml:4`, `addons/crm/report/crm_opportunity_report_views.xml:16`, `addons/crm/report/crm_opportunity_report_views.xml:37`, `addons/crm/report/crm_opportunity_report_views.xml:58`, `addons/crm/report/crm_opportunity_report_views.xml:78`, `addons/crm/report/crm_opportunity_report_views.xml:99`, `addons/crm/report/crm_opportunity_report_views.xml:160`, `addons/crm/report/crm_opportunity_report_views.xml:180`, `addons/crm/report/crm_opportunity_report_views.xml:205`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/crm/security/crm_security.xml`, `addons/crm/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 11 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/crm/__manifest__.py`, `addons/crm/models/res_config_settings.py`, `addons/crm/models/crm_team.py`, `addons/crm/models/crm_lead.py`, `addons/crm/wizard/crm_lead_pls_update.py`, `addons/crm/data/crm_lead_prediction_data.xml`, `addons/crm/data/ir_cron_data.xml`, `addons/crm/tests/test_crm_lead_assignment.py`, `addons/crm/tests/test_crm_pls.py`, `addons/crm/tests/test_performances.py`, `addons/crm/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 20 test files are present.
- **Evidence:** `addons/crm/tests/test_crm_activity.py`, `addons/crm/tests/test_crm_ui.py`, `addons/crm/tests/test_crm_lead_assignment.py`, `addons/crm/tests/test_sales_team_ui.py`, `addons/crm/tests/test_crm_pls.py`, `addons/crm/tests/test_crm_lead_duration_mixin.py`, `addons/crm/tests/test_crm_lead_duplicates.py`, `addons/crm/tests/test_performances.py`, `addons/crm/tests/common.py`, `addons/crm/tests/test_digest.py`, `addons/crm/tests/test_crm_lead.py`, `addons/crm/tests/test_crm_lead_merge.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 49; representative identifiers: `group_use_lead`, `group_use_recurring_revenues`, `contacts.res_partner_menu_config`, `crm_lead_view_tree_opportunity_reporting`, `crm_opportunity_report_view_pivot`, `crm_opportunity_report_view_pivot_lead`, `crm_opportunity_report_view_graph`, `crm_opportunity_report_view_graph_lead`, `crm_opportunity_report_view_search`, `crm_lead_view_tree_reporting`, `crm_opportunity_report_action`, `crm_opportunity_report_action_lead`, `crm_activity_report_view_graph`, `crm_activity_report_view_pivot`, `crm_activity_report_view_tree`, `crm_activity_report_view_search`, `crm_activity_report_action`, `crm_activity_report_action_team`, `view_crm_lead2opportunity_partner_mass`, `action_crm_send_mass_convert`
- Menus: 26; representative evidence: `addons/crm/views/crm_menu_views.xml:9`, `addons/crm/views/crm_menu_views.xml:17`, `addons/crm/views/crm_menu_views.xml:22`, `addons/crm/views/crm_menu_views.xml:28`, `addons/crm/views/crm_menu_views.xml:36`, `addons/crm/views/crm_menu_views.xml:42`, `addons/crm/views/crm_menu_views.xml:50`, `addons/crm/views/crm_menu_views.xml:59`, `addons/crm/views/crm_menu_views.xml:65`, `addons/crm/views/crm_menu_views.xml:71`, `addons/crm/views/crm_menu_views.xml:77`, `addons/crm/views/crm_menu_views.xml:83`
- Templates: 4; representative evidence: `addons/crm/data/crm_lead_merge_template.xml:4`, `addons/crm/data/mail_templates.xml:3`, `addons/crm/views/crm_helper_templates.xml:3`, `addons/crm/views/crm_lead_templates.xml:3`
- View/action field declarations: 216; representative evidence: `addons/crm/report/crm_opportunity_report_views.xml:6`, `addons/crm/report/crm_opportunity_report_views.xml:9`, `addons/crm/report/crm_opportunity_report_views.xml:18`, `addons/crm/report/crm_opportunity_report_views.xml:20`, `addons/crm/report/crm_opportunity_report_views.xml:39`, `addons/crm/report/crm_opportunity_report_views.xml:41`, `addons/crm/report/crm_opportunity_report_views.xml:60`, `addons/crm/report/crm_opportunity_report_views.xml:61`, `addons/crm/report/crm_opportunity_report_views.xml:80`, `addons/crm/report/crm_opportunity_report_views.xml:82`, `addons/crm/report/crm_opportunity_report_views.xml:101`, `addons/crm/report/crm_opportunity_report_views.xml:103`
- Browser assets: 48; representative files: `addons/crm/static/src/activity_menu_patch.js`, `addons/crm/static/tests/crm_kanban_progress_bar_mrr_sum_field.test.js`, `addons/crm/static/tests/forecast_view.test.js`, `addons/crm/static/tests/crm_rainbowman.test.js`, `addons/crm/static/tests/forecast_kanban.test.js`, `addons/crm/static/tests/crm_team_switcher.test.js`, `addons/crm/static/tests/crm_test_helpers.js`, `addons/crm/static/tests/crm_mock_server.js`, `addons/crm/static/src/views/crm_control_panel.js`, `addons/crm/static/src/views/forecast_search_model.js`, `addons/crm/static/src/views/crm_search_model.js`, `addons/crm/static/src/views/check_rainbowman_message.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm/__manifest__.py`
- **HTTP entry points:** `addons/crm/controllers/main.py:13`, `addons/crm/controllers/main.py:24`, `addons/crm/controllers/main.py:35`
- **Scheduled entry points:** `addons/crm/__manifest__.py`, `addons/crm/models/res_config_settings.py`, `addons/crm/models/crm_team.py`, `addons/crm/models/crm_lead.py`, `addons/crm/wizard/crm_lead_pls_update.py`, `addons/crm/data/crm_lead_prediction_data.xml`, `addons/crm/data/ir_cron_data.xml`, `addons/crm/tests/test_crm_lead_assignment.py`, `addons/crm/tests/test_crm_pls.py`, `addons/crm/tests/test_performances.py`, `addons/crm/tests/common.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 23
- Representative model evidence: inherits `res.partner` (addons/crm/models/res_partner.py:6); inherits `ir.config_parameter` (addons/crm/models/ir_config_parameter.py:7); inherits `mail.activity` (addons/crm/models/mail_activity.py:7); inherits `discuss.channel` (addons/crm/models/discuss_channel.py:7); inherits `digest.digest` (addons/crm/models/digest.py:8); `crm.recurring.plan` (addons/crm/models/crm_recurring_plan.py:7); inherits `res.groups` (addons/crm/models/res_groups.py:6); inherits `res.config.settings` (addons/crm/models/res_config_settings.py:11); inherits `calendar.event` (addons/crm/models/calendar.py:7); `crm.team` (addons/crm/models/crm_team.py:19); inherits `utm.campaign` (addons/crm/models/utm.py:7); `crm.stage` (addons/crm/models/crm_stage.py:15); inherits `res.users` (addons/crm/models/res_users.py:4); `crm.lead` (addons/crm/models/crm_lead.py:84); inherits `crm.team.member` (addons/crm/models/crm_team_member.py:17); `crm.lead.scoring.frequency` (addons/crm/models/crm_lead_scoring_frequency.py:7); `crm.lead.scoring.frequency.field` (addons/crm/models/crm_lead_scoring_frequency.py:18); `crm.lost.reason` (addons/crm/models/crm_lost_reason.py:7); `crm.activity.report` (addons/crm/report/crm_activity_report.py:7); `crm.lead.pls.update` (addons/crm/wizard/crm_lead_pls_update.py:7); `crm.lead.lost` (addons/crm/wizard/crm_lead_lost.py:9); `crm.merge.opportunity` (addons/crm/wizard/crm_merge_opportunities.py:7); `crm.lead2opportunity.partner.mass` (addons/crm/wizard/crm_lead_to_opportunity_mass.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 3
- Route evidence: `addons/crm/controllers/main.py:13`, `addons/crm/controllers/main.py:24`, `addons/crm/controllers/main.py:35`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_setup`, `base_install_request`, `sales_team`, `mail`, `calendar`, `resource`, `utm`, `web_tour`, `contacts`, `digest`, `phone_validation`
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

- `addons/crm/README.md`
- `addons/crm/__init__.py`
- `addons/crm/__manifest__.py`
- `addons/crm/controllers/__init__.py`
- `addons/crm/controllers/main.py`
- `addons/crm/controllers/webmanifest.py`
- `addons/crm/data/crm_lead_demo.xml`
- `addons/crm/data/crm_lead_merge_template.xml`
- `addons/crm/data/crm_lead_prediction_data.xml`
- `addons/crm/data/crm_lost_reason_data.xml`
- `addons/crm/data/crm_recurring_plan_data.xml`
- `addons/crm/data/crm_stage_data.xml`
- `addons/crm/data/crm_stage_demo.xml`
- `addons/crm/data/crm_team_data.xml`
- `addons/crm/data/crm_team_demo.xml`
- `addons/crm/data/crm_team_member_demo.xml`
- `addons/crm/data/crm_tour.xml`
- `addons/crm/data/digest_data.xml`
- `addons/crm/data/ir_cron_data.xml`
- `addons/crm/data/mail_message_subtype_data.xml`
- `addons/crm/data/mail_template_demo.xml`
- `addons/crm/data/mail_templates.xml`
- `addons/crm/doc/changelog.rst`
- `addons/crm/doc/index.rst`
- `addons/crm/doc/stage_status.rst`
- `addons/crm/i18n/af.po`
- `addons/crm/i18n/am.po`
- `addons/crm/i18n/ar.po`
- `addons/crm/i18n/az.po`
- `addons/crm/i18n/bg.po`
- `addons/crm/i18n/bs.po`
- `addons/crm/i18n/ca.po`
- `addons/crm/i18n/crm.pot`
- `addons/crm/i18n/cs.po`
- `addons/crm/i18n/da.po`
- `addons/crm/i18n/de.po`
- `addons/crm/i18n/el.po`
- `addons/crm/i18n/es.po`
- `addons/crm/i18n/es_419.po`
- `addons/crm/i18n/es_CL.po`
- `addons/crm/i18n/et.po`
- `addons/crm/i18n/eu.po`
- `addons/crm/i18n/fa.po`
- `addons/crm/i18n/fi.po`
- `addons/crm/i18n/fo.po`
- `addons/crm/i18n/fr.po`
- `addons/crm/i18n/fr_CA.po`
- `addons/crm/i18n/gl.po`
- `addons/crm/i18n/gu.po`
- `addons/crm/i18n/he.po`
- `addons/crm/i18n/hi.po`
- `addons/crm/i18n/hr.po`
- `addons/crm/i18n/hu.po`
- `addons/crm/i18n/id.po`
- `addons/crm/i18n/is.po`
- `addons/crm/i18n/it.po`
- `addons/crm/i18n/ja.po`
- `addons/crm/i18n/ka.po`
- `addons/crm/i18n/kab.po`
- `addons/crm/i18n/km.po`
- `addons/crm/i18n/ko.po`
- `addons/crm/i18n/ku.po`
- `addons/crm/i18n/lb.po`
- `addons/crm/i18n/lo.po`
- `addons/crm/i18n/lt.po`
- `addons/crm/i18n/lv.po`
- `addons/crm/i18n/mk.po`
- `addons/crm/i18n/mn.po`
- `addons/crm/i18n/my.po`
- `addons/crm/i18n/nb.po`
- `addons/crm/i18n/nl.po`
- `addons/crm/i18n/pl.po`
- `addons/crm/i18n/pt.po`
- `addons/crm/i18n/pt_BR.po`
- `addons/crm/i18n/ro.po`
- `addons/crm/i18n/ru.po`
- `addons/crm/i18n/sk.po`
- `addons/crm/i18n/sl.po`
- `addons/crm/i18n/sq.po`
- `addons/crm/i18n/sr@latin.po`
- `addons/crm/i18n/sv.po`
- `addons/crm/i18n/th.po`
- `addons/crm/i18n/tr.po`
- `addons/crm/i18n/uk.po`
- `addons/crm/i18n/uz.po`
- `addons/crm/i18n/vi.po`
- `addons/crm/i18n/zh_CN.po`
- `addons/crm/i18n/zh_TW.po`
- `addons/crm/models/__init__.py`
- `addons/crm/models/calendar.py`
- `addons/crm/models/crm_lead.py`
- `addons/crm/models/crm_lead_scoring_frequency.py`
- `addons/crm/models/crm_lost_reason.py`
- `addons/crm/models/crm_recurring_plan.py`
- `addons/crm/models/crm_stage.py`
- `addons/crm/models/crm_team.py`
- `addons/crm/models/crm_team_member.py`
- `addons/crm/models/digest.py`
- `addons/crm/models/discuss_channel.py`
- `addons/crm/models/ir_config_parameter.py`
- `addons/crm/models/mail_activity.py`
- `addons/crm/models/res_config_settings.py`
- `addons/crm/models/res_groups.py`
- `addons/crm/models/res_partner.py`
- `addons/crm/models/res_users.py`
- `addons/crm/models/utm.py`
- `addons/crm/report/__init__.py`
- `addons/crm/report/crm_activity_report.py`
- `addons/crm/report/crm_activity_report_views.xml`
- `addons/crm/report/crm_opportunity_report_views.xml`
- `addons/crm/security/crm_security.xml`
- `addons/crm/security/ir.access.csv`
- `addons/crm/static/description/icon.png`
- `addons/crm/static/description/icon.svg`
- `addons/crm/static/description/icon_hi.png`
- `addons/crm/static/src/activity_menu_patch.js`
- `addons/crm/static/src/components/breadcrumbs/crm_breadcrumbs.js`
- `addons/crm/static/src/components/breadcrumbs/crm_breadcrumbs.xml`
- `addons/crm/static/src/components/lead_generation_dropdown/lead_generation_dropdown.js`
- `addons/crm/static/src/components/lead_generation_dropdown/lead_generation_dropdown.scss`
- `addons/crm/static/src/components/lead_generation_dropdown/lead_generation_dropdown.xml`
- `addons/crm/static/src/components/promote_mail_plugins_dialog/promote_mail_plugins_dialog.js`
- `addons/crm/static/src/components/promote_mail_plugins_dialog/promote_mail_plugins_dialog.xml`
- `addons/crm/static/src/components/team_switcher/team_switcher.js`
- `addons/crm/static/src/components/team_switcher/team_switcher.xml`
- `addons/crm/static/src/core/common/@types/models.d.ts`
- `addons/crm/static/src/core/common/crm_lead_model.js`
- `addons/crm/static/src/core/common/res_partner_model_patch.js`
- `addons/crm/static/src/img/lead_sourcing.png`
- `addons/crm/static/src/img/mail.png`
- `addons/crm/static/src/img/mail_plugins.png`
- `addons/crm/static/src/img/milk-autofill.gif`
- `addons/crm/static/src/img/milk-generate-leads.gif`
- `addons/crm/static/src/img/milk-mapview-toggle.gif`
- `addons/crm/static/src/img/milk-pipeline-progress.gif`
- `addons/crm/static/src/img/milk-probability-rate.gif`
- `addons/crm/static/src/img/pls-tooltip-ai-icon.png`
- `addons/crm/static/src/img/settings.png`
- `addons/crm/static/src/img/survey.png`
- `addons/crm/static/src/img/website.png`
- `addons/crm/static/src/js/fields/many2one_avatar_leader_user.js`
- `addons/crm/static/src/js/tours/crm.js`
- `addons/crm/static/src/scss/crm.scss`
- `addons/crm/static/src/scss/crm_team.scss`
- `addons/crm/static/src/scss/crm_team_member_views.scss`
- `addons/crm/static/src/views/check_rainbowman_message.js`
- `addons/crm/static/src/views/crm_activity/crm_activity_view.js`
- `addons/crm/static/src/views/crm_calendar/crm_calendar_view.js`
- `addons/crm/static/src/views/crm_control_panel.js`
- `addons/crm/static/src/views/crm_form/crm_form.js`
- `addons/crm/static/src/views/crm_form/crm_form.scss`
- `addons/crm/static/src/views/crm_form/crm_pls_tooltip_button.js`
- `addons/crm/static/src/views/crm_form/crm_pls_tooltip_button.scss`
- `addons/crm/static/src/views/crm_form/crm_pls_tooltip_button.xml`
- `addons/crm/static/src/views/crm_graph/crm_graph_view.js`
- `addons/crm/static/src/views/crm_kanban/crm_column_progress.js`
- `addons/crm/static/src/views/crm_kanban/crm_column_progress.xml`
- `addons/crm/static/src/views/crm_kanban/crm_kanban_arch_parser.js`
- `addons/crm/static/src/views/crm_kanban/crm_kanban_model.js`
- `addons/crm/static/src/views/crm_kanban/crm_kanban_renderer.js`
- `addons/crm/static/src/views/crm_kanban/crm_kanban_view.js`
- `addons/crm/static/src/views/crm_kanban/crm_kanban_view.xml`
- `addons/crm/static/src/views/crm_list/crm_list_view.js`
- `addons/crm/static/src/views/crm_list/crm_list_view.xml`
- `addons/crm/static/src/views/crm_pivot/crm_pivot_view.js`
- `addons/crm/static/src/views/crm_search_model.js`
- `addons/crm/static/src/views/fill_temporal_service.js`
- `addons/crm/static/src/views/forecast_graph/forecast_graph_view.js`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_column_quick_create.js`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_controller.js`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_model.js`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_renderer.js`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_renderer.xml`
- `addons/crm/static/src/views/forecast_kanban/forecast_kanban_view.js`
- `addons/crm/static/src/views/forecast_list/forecast_list_view.js`
- `addons/crm/static/src/views/forecast_pivot/forecast_pivot_view.js`
- `addons/crm/static/src/views/forecast_search_model.js`
- `addons/crm/static/src/webclient/share_target/crm_share_target_item.js`
- `addons/crm/static/src/webclient/share_target/crm_share_target_item.xml`
- `addons/crm/static/tests/crm_kanban_progress_bar_mrr_sum_field.test.js`
- `addons/crm/static/tests/crm_mock_server.js`
- `addons/crm/static/tests/crm_rainbowman.test.js`
- `addons/crm/static/tests/crm_team_switcher.test.js`
- `addons/crm/static/tests/crm_test_helpers.js`
- `addons/crm/static/tests/forecast_kanban.test.js`
- `addons/crm/static/tests/forecast_view.test.js`
- `addons/crm/static/tests/mock_server/mock_models/crm_lead.js`
- `addons/crm/static/tests/tours/create_crm_team_tour.js`
- `addons/crm/static/tests/tours/crm_email_and_phone_propagation.js`
- `addons/crm/static/tests/tours/crm_forecast_tour.js`
- `addons/crm/static/tests/tours/crm_rainbowman.js`
- `addons/crm/static/xls/crm_lead.xls`
- `addons/crm/tests/__init__.py`
- `addons/crm/tests/common.py`
- `addons/crm/tests/test_crm_activity.py`
- `addons/crm/tests/test_crm_lead.py`
- `addons/crm/tests/test_crm_lead_assignment.py`
- `addons/crm/tests/test_crm_lead_convert.py`
- `addons/crm/tests/test_crm_lead_convert_mass.py`
- `addons/crm/tests/test_crm_lead_duplicates.py`
- `addons/crm/tests/test_crm_lead_duration_mixin.py`
- `addons/crm/tests/test_crm_lead_merge.py`
- `addons/crm/tests/test_crm_lead_multicompany.py`
- `addons/crm/tests/test_crm_lead_notification.py`
- `addons/crm/tests/test_crm_lead_smart_calendar.py`
- `addons/crm/tests/test_crm_pls.py`
- `addons/crm/tests/test_crm_rainbowman.py`
- `addons/crm/tests/test_crm_ui.py`
- `addons/crm/tests/test_digest.py`
- `addons/crm/tests/test_performances.py`
- `addons/crm/tests/test_res_partner.py`
- `addons/crm/tests/test_sales_team_ui.py`
- `addons/crm/views/calendar_views.xml`
- `addons/crm/views/crm_helper_templates.xml`
- `addons/crm/views/crm_lead_templates.xml`
- `addons/crm/views/crm_lead_views.xml`
- `addons/crm/views/crm_lost_reason_views.xml`
- `addons/crm/views/crm_menu_views.xml`
- `addons/crm/views/crm_recurring_plan_views.xml`
- `addons/crm/views/crm_stage_views.xml`
- `addons/crm/views/crm_team_member_views.xml`
- `addons/crm/views/crm_team_views.xml`
- `addons/crm/views/digest_views.xml`
- `addons/crm/views/mail_activity_plan_views.xml`
- `addons/crm/views/mail_activity_views.xml`
- `addons/crm/views/res_config_settings_views.xml`
- `addons/crm/views/res_partner_views.xml`
- `addons/crm/views/utm_campaign_views.xml`
- `addons/crm/wizard/__init__.py`
- `addons/crm/wizard/crm_lead_lost.py`
- `addons/crm/wizard/crm_lead_lost_views.xml`
- `addons/crm/wizard/crm_lead_pls_update.py`
- `addons/crm/wizard/crm_lead_pls_update_views.xml`
- `addons/crm/wizard/crm_lead_to_opportunity_mass.py`
- `addons/crm/wizard/crm_lead_to_opportunity_mass_views.xml`
- `addons/crm/wizard/crm_merge_opportunities.py`
- `addons/crm/wizard/crm_merge_opportunities_views.xml`
