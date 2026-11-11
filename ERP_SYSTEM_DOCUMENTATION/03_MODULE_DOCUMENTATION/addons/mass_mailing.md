# Module: mass_mailing

- **Module ID:** MOD-362
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mass_mailing`
- **Manifest:** `addons/mass_mailing/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Marketing/Email Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Design, send and track emails

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 481 files, including 55 Python, 103 XML, and 97 JavaScript/TypeScript files. The manifest declares dependencies: `contacts`, `mail`, `html_builder`, `utm`, `link_tracker`, `social_media`, `web_tour`, `digest`.

## 2. Module structure

- Model/business logic files: 32
- Controller/API files: 3
- XML/data/view/template files: 103
- Browser asset files: 97
- Security files: 2
- Test files: 16
- Scheduled/automation evidence files: 11
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mass_mailing/security/ir.access.csv`, `addons/mass_mailing/security/res_groups_data.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 32 model declarations, 375 methods, 4 constraint handlers, 1 onchange handlers, and 33 dependency declarations.
- **Evidence:** `addons/mass_mailing/models/res_partner.py:7`, `addons/mass_mailing/models/mailing_trace.py:10`, `addons/mass_mailing/models/mail_mail.py:10`, `addons/mass_mailing/models/ir_ui_view.py:4`, `addons/mass_mailing/models/res_groups.py:6`, `addons/mass_mailing/models/res_config_settings.py:7`, `addons/mass_mailing/models/ir_model.py:7`, `addons/mass_mailing/models/mail_render_mixin.py:7`, `addons/mass_mailing/models/ir_mail_server.py:9`, `addons/mass_mailing/models/utm_source.py:9`, `addons/mass_mailing/models/mailing_filter.py:10`, `addons/mass_mailing/models/mailing_contact.py:17`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 17 route declarations.
- **Evidence:** `addons/mass_mailing/controllers/legacy.py:13`, `addons/mass_mailing/controllers/main.py:84`, `addons/mass_mailing/controllers/main.py:100`, `addons/mass_mailing/controllers/main.py:106`, `addons/mass_mailing/controllers/main.py:134`, `addons/mass_mailing/controllers/main.py:161`, `addons/mass_mailing/controllers/main.py:281`, `addons/mass_mailing/controllers/main.py:312`, `addons/mass_mailing/controllers/main.py:382`, `addons/mass_mailing/controllers/main.py:387`, `addons/mass_mailing/controllers/main.py:396`, `addons/mass_mailing/controllers/main.py:410`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 103 XML files and 97 JavaScript/TypeScript files; static XML analysis found 217 record/template/menu identifiers.
- **Evidence:** `addons/mass_mailing/demo/mailing_subscription.xml:5`, `addons/mass_mailing/demo/mailing_subscription.xml:9`, `addons/mass_mailing/demo/mailing_subscription.xml:13`, `addons/mass_mailing/demo/mailing_subscription.xml:17`, `addons/mass_mailing/demo/mailing_subscription.xml:23`, `addons/mass_mailing/demo/mailing_subscription.xml:27`, `addons/mass_mailing/demo/mailing_subscription.xml:33`, `addons/mass_mailing/demo/mailing_subscription.xml:40`, `addons/mass_mailing/demo/mailing_subscription.xml:44`, `addons/mass_mailing/demo/mailing_subscription.xml:50`, `addons/mass_mailing/demo/mailing_list_contact.xml:5`, `addons/mass_mailing/demo/mailing_list_contact.xml:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/mass_mailing/security/ir.access.csv`, `addons/mass_mailing/security/res_groups_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 11 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mass_mailing/__manifest__.py`, `addons/mass_mailing/models/res_config_settings.py`, `addons/mass_mailing/models/mailing.py`, `addons/mass_mailing/models/utm_campaign.py`, `addons/mass_mailing/data/ir_actions_server_data.xml`, `addons/mass_mailing/data/ir_cron_data.xml`, `addons/mass_mailing/tests/test_mailing_internals.py`, `addons/mass_mailing/tests/test_mail_mail.py`, `addons/mass_mailing/tests/test_mailing_mailing_schedule_date.py`, `addons/mass_mailing/tests/test_mailing_retry.py`, `addons/mass_mailing/tests/test_mailing_ab_testing.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 16 test files are present.
- **Evidence:** `addons/mass_mailing/tests/test_utm.py`, `addons/mass_mailing/tests/test_mass_mailing_snippets.py`, `addons/mass_mailing/tests/test_mailing_contact.py`, `addons/mass_mailing/tests/test_mailing_internals.py`, `addons/mass_mailing/tests/test_mail_render_mixin.py`, `addons/mass_mailing/tests/test_mail_mail.py`, `addons/mass_mailing/tests/test_mailing_filter.py`, `addons/mass_mailing/tests/test_mailing_mailing_schedule_date.py`, `addons/mass_mailing/tests/test_mailing_contact_to_list.py`, `addons/mass_mailing/tests/common.py`, `addons/mass_mailing/tests/test_mailing_list.py`, `addons/mass_mailing/tests/test_mailing_ui.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 103; representative identifiers: `mailing_list_data_sub_contact_1`, `mailing_list_data_sub_contact_2`, `mailing_list_data_sub_contact_3`, `mailing_list_data_sub_contact_4`, `mailing_list_data_sub_contact_5`, `mailing_list_data_sub_contact_6`, `mailing_list_data_sub_contact_7`, `mailing_list_1_sub_contact_3`, `mailing_list_1_sub_contact_6`, `mail_blacklist_demo_1`, `mailing_list_1`, `mass_mail_contact_1`, `mass_mail_contact_2`, `mass_mail_contact_3`, `mass_mail_contact_4`, `mass_mail_contact_5`, `mass_mail_contact_6`, `mass_mail_contact_7`, `mass_mail_1_stat_0`, `mass_mail_1_stat_1`
- Menus: 20; representative evidence: `addons/mass_mailing/views/mailing_menus.xml:4`, `addons/mass_mailing/views/mailing_menus.xml:11`, `addons/mass_mailing/views/mailing_menus.xml:18`, `addons/mass_mailing/views/mailing_menus.xml:22`, `addons/mass_mailing/views/mailing_menus.xml:27`, `addons/mass_mailing/views/mailing_menus.xml:32`, `addons/mass_mailing/views/mailing_menus.xml:39`, `addons/mass_mailing/views/mailing_menus.xml:46`, `addons/mass_mailing/views/mailing_menus.xml:54`, `addons/mass_mailing/views/mailing_menus.xml:58`, `addons/mass_mailing/views/mailing_menus.xml:63`, `addons/mass_mailing/views/mailing_menus.xml:70`
- Templates: 25; representative evidence: `addons/mass_mailing/demo/mailing_mailing.xml:3`, `addons/mass_mailing/data/digest_data.xml:4`, `addons/mass_mailing/data/mailing_data_templates.xml:8`, `addons/mass_mailing/data/mailing_data_templates.xml:40`, `addons/mass_mailing/data/mailing_data_templates.xml:81`, `addons/mass_mailing/views/themes_templates.xml:4`, `addons/mass_mailing/views/themes_templates.xml:17`, `addons/mass_mailing/views/themes_templates.xml:21`, `addons/mass_mailing/views/mailing_templates_portal_layouts.xml:4`, `addons/mass_mailing/views/mailing_templates_portal_management.xml:3`, `addons/mass_mailing/views/mailing_templates_portal_management.xml:28`, `addons/mass_mailing/views/mailing_templates_portal_management.xml:53`
- View/action field declarations: 188; representative evidence: `addons/mass_mailing/demo/mailing_trace.xml:7`, `addons/mass_mailing/demo/mailing_trace.xml:19`, `addons/mass_mailing/demo/mailing_trace.xml:31`, `addons/mass_mailing/demo/mailing_trace.xml:42`, `addons/mass_mailing/demo/mailing_trace.xml:53`, `addons/mass_mailing/demo/mailing_trace.xml:63`, `addons/mass_mailing/demo/mailing_trace.xml:72`, `addons/mass_mailing/demo/mailing_trace.xml:82`, `addons/mass_mailing/report/mailing_trace_report_views.xml:5`, `addons/mass_mailing/report/mailing_trace_report_views.xml:6`, `addons/mass_mailing/report/mailing_trace_report_views.xml:30`, `addons/mass_mailing/report/mailing_trace_report_views.xml:31`
- Browser assets: 97; representative files: `addons/mass_mailing/static/tests/mass_mailing_html_field.test.js`, `addons/mass_mailing/static/tests/mass_mailing_link_plugin.test.js`, `addons/mass_mailing/static/tests/mass_mailing_test_helpers.js`, `addons/mass_mailing/static/tests/mailing_contact_to_list.test.js`, `addons/mass_mailing/static/tests/mass_mailing_snippet_model.test.js`, `addons/mass_mailing/static/tests/mailing_preview_iframe.test.js`, `addons/mass_mailing/static/src/iframe/mass_mailing_iframe.js`, `addons/mass_mailing/static/src/iframe/mass_mailing_iframe_utils.js`, `addons/mass_mailing/static/src/themes/theme_service.js`, `addons/mass_mailing/static/src/action/client_actions.js`, `addons/mass_mailing/static/src/interactions/subscribe.js`, `addons/mass_mailing/static/src/views/mass_mailing_subscription_graph_renderer.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mass_mailing/__manifest__.py`
- **HTTP entry points:** `addons/mass_mailing/controllers/legacy.py:13`, `addons/mass_mailing/controllers/main.py:84`, `addons/mass_mailing/controllers/main.py:100`, `addons/mass_mailing/controllers/main.py:106`, `addons/mass_mailing/controllers/main.py:134`, `addons/mass_mailing/controllers/main.py:161`, `addons/mass_mailing/controllers/main.py:281`, `addons/mass_mailing/controllers/main.py:312`, `addons/mass_mailing/controllers/main.py:382`, `addons/mass_mailing/controllers/main.py:387`, `addons/mass_mailing/controllers/main.py:396`, `addons/mass_mailing/controllers/main.py:410`
- **Scheduled entry points:** `addons/mass_mailing/__manifest__.py`, `addons/mass_mailing/models/res_config_settings.py`, `addons/mass_mailing/models/mailing.py`, `addons/mass_mailing/models/utm_campaign.py`, `addons/mass_mailing/data/ir_actions_server_data.xml`, `addons/mass_mailing/data/ir_cron_data.xml`, `addons/mass_mailing/tests/test_mailing_internals.py`, `addons/mass_mailing/tests/test_mail_mail.py`, `addons/mass_mailing/tests/test_mailing_mailing_schedule_date.py`, `addons/mass_mailing/tests/test_mailing_retry.py`, `addons/mass_mailing/tests/test_mailing_ab_testing.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 32
- Representative model evidence: inherits `res.partner` (addons/mass_mailing/models/res_partner.py:7); `mailing.trace` (addons/mass_mailing/models/mailing_trace.py:10); inherits `mail.mail` (addons/mass_mailing/models/mail_mail.py:10); inherits `ir.ui.view` (addons/mass_mailing/models/ir_ui_view.py:4); inherits `res.groups` (addons/mass_mailing/models/res_groups.py:6); inherits `res.config.settings` (addons/mass_mailing/models/res_config_settings.py:7); inherits `ir.model` (addons/mass_mailing/models/ir_model.py:7); inherits `mail.render.mixin` (addons/mass_mailing/models/mail_render_mixin.py:7); inherits `ir.mail_server` (addons/mass_mailing/models/ir_mail_server.py:9); inherits `utm.source` (addons/mass_mailing/models/utm_source.py:9); `mailing.filter` (addons/mass_mailing/models/mailing_filter.py:10); `mailing.contact` (addons/mass_mailing/models/mailing_contact.py:17); inherits `ir.http` (addons/mass_mailing/models/ir_http.py:6); `mailing.mailing` (addons/mass_mailing/models/mailing.py:38); inherits `link.tracker` (addons/mass_mailing/models/link_tracker.py:9); inherits `link.tracker.click` (addons/mass_mailing/models/link_tracker.py:15); inherits `utm.campaign` (addons/mass_mailing/models/utm_campaign.py:12); inherits `mail.blacklist` (addons/mass_mailing/models/mail_blacklist.py:7); `mailing.subscription.optout` (addons/mass_mailing/models/mailing_subscription_optout.py:7); inherits `mail.thread` (addons/mass_mailing/models/mail_thread.py:12); inherits `res.users` (addons/mass_mailing/models/res_users.py:7); `mailing.list` (addons/mass_mailing/models/mailing_list.py:11); `mailing.subscription` (addons/mass_mailing/models/mailing_subscription.py:7); inherits `ir.attachment` (addons/mass_mailing/models/ir_attachment.py:6); inherits `utm.medium` (addons/mass_mailing/models/utm_medium.py:9); inherits `res.company` (addons/mass_mailing/models/res_company.py:8); `mailing.trace.report` (addons/mass_mailing/report/mailing_trace_report.py:7); `mailing.contact.to.list` (addons/mass_mailing/wizard/mailing_contact_to_list.py:7); inherits `mail.compose.message` (addons/mass_mailing/wizard/mail_compose_message.py:10); `mailing.mailing.schedule.date` (addons/mass_mailing/wizard/mailing_mailing_schedule_date.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 17
- Route evidence: `addons/mass_mailing/controllers/legacy.py:13`, `addons/mass_mailing/controllers/main.py:84`, `addons/mass_mailing/controllers/main.py:100`, `addons/mass_mailing/controllers/main.py:106`, `addons/mass_mailing/controllers/main.py:134`, `addons/mass_mailing/controllers/main.py:161`, `addons/mass_mailing/controllers/main.py:281`, `addons/mass_mailing/controllers/main.py:312`, `addons/mass_mailing/controllers/main.py:382`, `addons/mass_mailing/controllers/main.py:387`, `addons/mass_mailing/controllers/main.py:396`, `addons/mass_mailing/controllers/main.py:410`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `contacts`, `mail`, `html_builder`, `utm`, `link_tracker`, `social_media`, `web_tour`, `digest`
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

- `addons/mass_mailing/README.md`
- `addons/mass_mailing/__init__.py`
- `addons/mass_mailing/__manifest__.py`
- `addons/mass_mailing/controllers/__init__.py`
- `addons/mass_mailing/controllers/legacy.py`
- `addons/mass_mailing/controllers/main.py`
- `addons/mass_mailing/data/digest_data.xml`
- `addons/mass_mailing/data/ir_actions_server_data.xml`
- `addons/mass_mailing/data/ir_attachment_data.xml`
- `addons/mass_mailing/data/ir_config_parameter_data.xml`
- `addons/mass_mailing/data/ir_cron_data.xml`
- `addons/mass_mailing/data/mailing_data_templates.xml`
- `addons/mass_mailing/data/mailing_list_contact.xml`
- `addons/mass_mailing/data/mailing_subscription.xml`
- `addons/mass_mailing/data/mailing_subscription_optout.xml`
- `addons/mass_mailing/data/mass_mailing_tour.xml`
- `addons/mass_mailing/data/portal_entry_data.xml`
- `addons/mass_mailing/data/res_groups_privilege_data.xml`
- `addons/mass_mailing/demo/mailing_list_contact.xml`
- `addons/mass_mailing/demo/mailing_mailing.xml`
- `addons/mass_mailing/demo/mailing_subscription.xml`
- `addons/mass_mailing/demo/mailing_trace.xml`
- `addons/mass_mailing/demo/res_users.xml`
- `addons/mass_mailing/demo/utm.xml`
- `addons/mass_mailing/doc/changelog.rst`
- `addons/mass_mailing/doc/index.rst`
- `addons/mass_mailing/i18n/af.po`
- `addons/mass_mailing/i18n/am.po`
- `addons/mass_mailing/i18n/ar.po`
- `addons/mass_mailing/i18n/az.po`
- `addons/mass_mailing/i18n/bg.po`
- `addons/mass_mailing/i18n/bs.po`
- `addons/mass_mailing/i18n/ca.po`
- `addons/mass_mailing/i18n/cs.po`
- `addons/mass_mailing/i18n/da.po`
- `addons/mass_mailing/i18n/de.po`
- `addons/mass_mailing/i18n/el.po`
- `addons/mass_mailing/i18n/es.po`
- `addons/mass_mailing/i18n/es_419.po`
- `addons/mass_mailing/i18n/es_CL.po`
- `addons/mass_mailing/i18n/et.po`
- `addons/mass_mailing/i18n/eu.po`
- `addons/mass_mailing/i18n/fa.po`
- `addons/mass_mailing/i18n/fi.po`
- `addons/mass_mailing/i18n/fo.po`
- `addons/mass_mailing/i18n/fr.po`
- `addons/mass_mailing/i18n/fr_BE.po`
- `addons/mass_mailing/i18n/fr_CA.po`
- `addons/mass_mailing/i18n/gl.po`
- `addons/mass_mailing/i18n/gu.po`
- `addons/mass_mailing/i18n/he.po`
- `addons/mass_mailing/i18n/hi.po`
- `addons/mass_mailing/i18n/hr.po`
- `addons/mass_mailing/i18n/hu.po`
- `addons/mass_mailing/i18n/id.po`
- `addons/mass_mailing/i18n/is.po`
- `addons/mass_mailing/i18n/it.po`
- `addons/mass_mailing/i18n/ja.po`
- `addons/mass_mailing/i18n/ka.po`
- `addons/mass_mailing/i18n/kab.po`
- `addons/mass_mailing/i18n/km.po`
- `addons/mass_mailing/i18n/ko.po`
- `addons/mass_mailing/i18n/ku.po`
- `addons/mass_mailing/i18n/lb.po`
- `addons/mass_mailing/i18n/lo.po`
- `addons/mass_mailing/i18n/lt.po`
- `addons/mass_mailing/i18n/lv.po`
- `addons/mass_mailing/i18n/mass_mailing.pot`
- `addons/mass_mailing/i18n/mk.po`
- `addons/mass_mailing/i18n/mn.po`
- `addons/mass_mailing/i18n/my.po`
- `addons/mass_mailing/i18n/nb.po`
- `addons/mass_mailing/i18n/nl.po`
- `addons/mass_mailing/i18n/pl.po`
- `addons/mass_mailing/i18n/pt.po`
- `addons/mass_mailing/i18n/pt_BR.po`
- `addons/mass_mailing/i18n/ro.po`
- `addons/mass_mailing/i18n/ru.po`
- `addons/mass_mailing/i18n/sk.po`
- `addons/mass_mailing/i18n/sl.po`
- `addons/mass_mailing/i18n/sq.po`
- `addons/mass_mailing/i18n/sr@latin.po`
- `addons/mass_mailing/i18n/sv.po`
- `addons/mass_mailing/i18n/th.po`
- `addons/mass_mailing/i18n/tr.po`
- `addons/mass_mailing/i18n/uk.po`
- `addons/mass_mailing/i18n/uz.po`
- `addons/mass_mailing/i18n/vi.po`
- `addons/mass_mailing/i18n/zh_CN.po`
- `addons/mass_mailing/i18n/zh_TW.po`
- `addons/mass_mailing/models/__init__.py`
- `addons/mass_mailing/models/ir_attachment.py`
- `addons/mass_mailing/models/ir_http.py`
- `addons/mass_mailing/models/ir_mail_server.py`
- `addons/mass_mailing/models/ir_model.py`
- `addons/mass_mailing/models/ir_ui_view.py`
- `addons/mass_mailing/models/link_tracker.py`
- `addons/mass_mailing/models/mail_blacklist.py`
- `addons/mass_mailing/models/mail_mail.py`
- `addons/mass_mailing/models/mail_render_mixin.py`
- `addons/mass_mailing/models/mail_thread.py`
- `addons/mass_mailing/models/mailing.py`
- `addons/mass_mailing/models/mailing_contact.py`
- `addons/mass_mailing/models/mailing_filter.py`
- `addons/mass_mailing/models/mailing_list.py`
- `addons/mass_mailing/models/mailing_subscription.py`
- `addons/mass_mailing/models/mailing_subscription_optout.py`
- `addons/mass_mailing/models/mailing_trace.py`
- `addons/mass_mailing/models/res_company.py`
- `addons/mass_mailing/models/res_config_settings.py`
- `addons/mass_mailing/models/res_groups.py`
- `addons/mass_mailing/models/res_partner.py`
- `addons/mass_mailing/models/res_users.py`
- `addons/mass_mailing/models/utm_campaign.py`
- `addons/mass_mailing/models/utm_medium.py`
- `addons/mass_mailing/models/utm_source.py`
- `addons/mass_mailing/report/__init__.py`
- `addons/mass_mailing/report/mailing_trace_report.py`
- `addons/mass_mailing/report/mailing_trace_report_views.xml`
- `addons/mass_mailing/security/ir.access.csv`
- `addons/mass_mailing/security/res_groups_data.xml`
- `addons/mass_mailing/static/description/icon.png`
- `addons/mass_mailing/static/description/icon.svg`
- `addons/mass_mailing/static/description/icon_hi.png`
- `addons/mass_mailing/static/shapes/s_attributes_1.svg`
- `addons/mass_mailing/static/shapes/s_attributes_2.svg`
- `addons/mass_mailing/static/shapes/s_attributes_3.svg`
- `addons/mass_mailing/static/shapes/s_attributes_4.svg`
- `addons/mass_mailing/static/shapes/s_attributes_5.svg`
- `addons/mass_mailing/static/shapes/s_newsletter_benefits_popup.svg`
- `addons/mass_mailing/static/shapes/s_newsletter_sms_notifications.svg`
- `addons/mass_mailing/static/src/action/client_actions.js`
- `addons/mass_mailing/static/src/builder/builder_overlay_patch.js`
- `addons/mass_mailing/static/src/builder/components/builder_row.scss`
- `addons/mass_mailing/static/src/builder/components/company_update_dialog.js`
- `addons/mass_mailing/static/src/builder/components/company_update_dialog.xml`
- `addons/mass_mailing/static/src/builder/components/mass_mailing_builder_select_label.js`
- `addons/mass_mailing/static/src/builder/components/mass_mailing_builder_select_label.scss`
- `addons/mass_mailing/static/src/builder/components/mass_mailing_builder_select_label.xml`
- `addons/mass_mailing/static/src/builder/fontfamily_picker.js`
- `addons/mass_mailing/static/src/builder/fontfamily_picker.xml`
- `addons/mass_mailing/static/src/builder/mass_mailing_builder.js`
- `addons/mass_mailing/static/src/builder/mass_mailing_builder.xml`
- `addons/mass_mailing/static/src/builder/mass_mailing_options.xml`
- `addons/mass_mailing/static/src/builder/mass_mailing_snippet_model.js`
- `addons/mass_mailing/static/src/builder/mass_mailing_snippet_preprocessor.js`
- `addons/mass_mailing/static/src/builder/options/alert_option.xml`
- `addons/mass_mailing/static/src/builder/options/alignment_option.xml`
- `addons/mass_mailing/static/src/builder/options/bento_blocks_add_card_option.xml`
- `addons/mass_mailing/static/src/builder/options/blockquote_option.xml`
- `addons/mass_mailing/static/src/builder/options/border_options.xml`
- `addons/mass_mailing/static/src/builder/options/color_picker_option.xml`
- `addons/mass_mailing/static/src/builder/options/company_team_options.xml`
- `addons/mass_mailing/static/src/builder/options/cta_badge_option.xml`
- `addons/mass_mailing/static/src/builder/options/image_tool_option.js`
- `addons/mass_mailing/static/src/builder/options/image_tool_option.xml`
- `addons/mass_mailing/static/src/builder/options/masonry_block_template_option.xml`
- `addons/mass_mailing/static/src/builder/options/options_container.js`
- `addons/mass_mailing/static/src/builder/options/options_container.scss`
- `addons/mass_mailing/static/src/builder/options/options_container.xml`
- `addons/mass_mailing/static/src/builder/options/padding_option.xml`
- `addons/mass_mailing/static/src/builder/options/record_snapshot_option.xml`
- `addons/mass_mailing/static/src/builder/options/snippet_visibility_option.inside.scss`
- `addons/mass_mailing/static/src/builder/options/snippet_visibility_option.js`
- `addons/mass_mailing/static/src/builder/options/snippet_visibility_option.xml`
- `addons/mass_mailing/static/src/builder/options/social_media_links.js`
- `addons/mass_mailing/static/src/builder/options/social_media_links.xml`
- `addons/mass_mailing/static/src/builder/options/social_media_option.xml`
- `addons/mass_mailing/static/src/builder/plugins/background_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/bento_blocks_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/border_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/color_ui_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/crop_image_action.js`
- `addons/mass_mailing/static/src/builder/plugins/cta_badge_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/customize_mailing_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/customize_mailing_variables.js`
- `addons/mass_mailing/static/src/builder/plugins/design_tab_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/dropzone_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/empty_mailing_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/empty_not_editable_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/font_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/icon_snippet_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/image_snippet_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/layout_column_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/mail_blockquote_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/masonry_block_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/mass_mailing_setup_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/move_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/operation_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/padding_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/power_buttons.scss`
- `addons/mass_mailing/static/src/builder/plugins/record_snapshot_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/save_snippet_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/schedule_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/signature_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/signature_snippet_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/snippet_visibility_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/social_media_option_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/version_control_plugin.js`
- `addons/mass_mailing/static/src/builder/plugins/view_in_browser_option_plugin.js`
- `addons/mass_mailing/static/src/builder/snippet_viewer/add_snippet_dialog.js`
- `addons/mass_mailing/static/src/builder/snippet_viewer/add_snippet_dialog.xml`
- `addons/mass_mailing/static/src/builder/snippet_viewer/snippet_viewer.scss`
- `addons/mass_mailing/static/src/builder/tabs/design_tab.js`
- `addons/mass_mailing/static/src/builder/tabs/design_tab.xml`
- `addons/mass_mailing/static/src/components/mailing_filter_form_view_dialog/mailing_filter_form_view_dialog.js`
- `addons/mass_mailing/static/src/components/mailing_filter_form_view_dialog/mailing_filter_form_view_dialog.xml`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mailing_preview_iframe.dark.scss`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mailing_preview_iframe.js`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mailing_preview_iframe.scss`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mailing_preview_iframe.xml`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mass_mailing_preview_record_field.js`
- `addons/mass_mailing/static/src/components/mailing_preview_iframe/mass_mailing_preview_record_field.xml`
- `addons/mass_mailing/static/src/components/mailing_preview_mode_toggle/mailing_preview_mode_toggle.js`
- `addons/mass_mailing/static/src/components/mailing_preview_mode_toggle/mailing_preview_mode_toggle.xml`
- `addons/mass_mailing/static/src/components/mass_mailing_link_popover/mailing_link_popover.xml`
- `addons/mass_mailing/static/src/components/mass_mailing_link_popover/mass_mailing_link_popover.js`
- `addons/mass_mailing/static/src/components/mass_mailing_save_as_template_cog_menu/mass_mailing_save_as_template_cog_menu.js`
- `addons/mass_mailing/static/src/components/mass_mailing_save_as_template_cog_menu/mass_mailing_save_as_template_cog_menu.xml`
- `addons/mass_mailing/static/src/editor/plugins/mass_mailing_contenteditable_plugin.js`
- `addons/mass_mailing/static/src/editor/plugins/mass_mailing_link_plugin.js`
- `addons/mass_mailing/static/src/editor/plugins/other_plugins.js`
- `addons/mass_mailing/static/src/editor/plugins/plugin_templates.xml`
- `addons/mass_mailing/static/src/editor/plugins/unsubscribe_command_plugin.js`
- `addons/mass_mailing/static/src/fields/deliverance_percent_pie/deliverance_percent_pie_field.js`
- `addons/mass_mailing/static/src/fields/deliverance_percent_pie/deliverance_percent_pie_field.xml`
- `addons/mass_mailing/static/src/fields/domain_savable_field/domain_savable_field.js`
- `addons/mass_mailing/static/src/fields/domain_savable_field/domain_savable_field.xml`
- `addons/mass_mailing/static/src/fields/html_field/mass_mailing_html_field.js`
- `addons/mass_mailing/static/src/fields/html_field/mass_mailing_html_field.scss`
- `addons/mass_mailing/static/src/fields/html_field/mass_mailing_html_field.xml`
- `addons/mass_mailing/static/src/fields/mass_mailing_many2many_tags_field/mass_mailing_many2many_tags_field.js`
- `addons/mass_mailing/static/src/fields/template_preview_field/mailing_template_kanban_card/mailing_template_kanban_card.scss`
- `addons/mass_mailing/static/src/fields/template_preview_field/mailing_template_kanban_card/mailing_template_kanban_card.shadowdom.scss`
- `addons/mass_mailing/static/src/fields/template_preview_field/template_preview_field.js`
- `addons/mass_mailing/static/src/fields/template_preview_field/template_preview_field.xml`
- `addons/mass_mailing/static/src/fields/template_preview_field/theme_selector_template_preview/theme_selector_template_preview.shadowdom.scss`
- `addons/mass_mailing/static/src/iframe/mass_mailing_iframe.js`
- `addons/mass_mailing/static/src/iframe/mass_mailing_iframe.scss`
- `addons/mass_mailing/static/src/iframe/mass_mailing_iframe.xml`
- `addons/mass_mailing/static/src/iframe/mass_mailing_iframe_utils.js`
- `addons/mass_mailing/static/src/iframe_assets/iframe_style.scss`
- `addons/mass_mailing/static/src/iframe_assets/snippets_style.scss`
- `addons/mass_mailing/static/src/img/newsletter.svg`
- `addons/mass_mailing/static/src/img/snippets_demo/s_bento_grid_default_image_2.webp`
- `addons/mass_mailing/static/src/img/snippets_demo/s_bento_grid_default_image_4.jpg`
- `addons/mass_mailing/static/src/img/snippets_demo/s_shape_image_default_image.jpg`
- `addons/mass_mailing/static/src/img/snippets_demo/s_showcase.jpg`
- `addons/mass_mailing/static/src/img/snippets_demo/s_video.jpg`
- `addons/mass_mailing/static/src/img/snippets_demo/set_catalog_square_md_1.webp`
- Additional source files not expanded in this page: 231; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
