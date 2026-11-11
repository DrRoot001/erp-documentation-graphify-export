# Module: event

- **Module ID:** MOD-064
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/event`
- **Manifest:** `addons/event/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Events`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Trainings, Conferences, Meetings, Exhibitions, Registrations

**Manifest description:**

Organization and management of Events.
======================================

The event module allows you to efficiently organize events and all related tasks: planning, registration tracking,
attendances, etc.

Key Features
------------
* Manage your Events and Registrations
* Use emails to automatically confirm and send acknowledgments for any event registration

**Scope evidence:** The module contains 178 files, including 32 Python, 40 XML, and 16 JavaScript/TypeScript files. The manifest declares dependencies: `barcodes`, `base_setup`, `digest`, `mail`, `phone_validation`, `portal`, `utm`.

## 2. Module structure

- Model/business logic files: 20
- Controller/API files: 3
- XML/data/view/template files: 40
- Browser asset files: 16
- Security files: 2
- Test files: 6
- Scheduled/automation evidence files: 5
- Reporting evidence files: 4

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/event/security/ir.access.csv`, `addons/event/security/event_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 20 model declarations, 239 methods, 11 constraint handlers, 5 onchange handlers, and 56 dependency declarations.
- **Evidence:** `addons/event/models/res_partner.py:14`, `addons/event/models/event_question_answer.py:8`, `addons/event/models/event_mail_registration.py:11`, `addons/event/models/event_ticket.py:8`, `addons/event/models/digest.py:6`, `addons/event/models/event_registration_answer.py:7`, `addons/event/models/mail_template.py:7`, `addons/event/models/res_config_settings.py:10`, `addons/event/models/event_mail.py:25`, `addons/event/models/event_type_ticket.py:4`, `addons/event/models/event_slot.py:14`, `addons/event/models/event_type.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 4 route declarations.
- **Evidence:** `addons/event/controllers/portal.py:14`, `addons/event/controllers/main.py:16`, `addons/event/controllers/main.py:35`, `addons/event/controllers/main.py:87`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 40 XML files and 16 JavaScript/TypeScript files; static XML analysis found 206 record/template/menu identifiers.
- **Evidence:** `addons/event/security/event_security.xml:3`, `addons/event/security/event_security.xml:9`, `addons/event/security/event_security.xml:16`, `addons/event/security/event_security.xml:23`, `addons/event/report/event_event_templates.xml:6`, `addons/event/report/event_event_templates.xml:110`, `addons/event/report/event_event_templates.xml:123`, `addons/event/report/event_event_templates.xml:143`, `addons/event/report/event_event_templates.xml:159`, `addons/event/report/event_event_templates.xml:173`, `addons/event/report/event_event_templates.xml:260`, `addons/event/report/event_event_templates.xml:291`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/event/security/ir.access.csv`, `addons/event/security/event_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 5 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/event/__manifest__.py`, `addons/event/models/event_event.py`, `addons/event/models/event_registration.py`, `addons/event/data/ir_cron_data.xml`, `addons/event/tests/test_event_mail_schedule.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 4 files contain report-action/template indicators.
- **Evidence:** `addons/event/controllers/main.py`, `addons/event/report/event_event_reports.xml`, `addons/event/report/event_registration_report.xml`, `addons/event/tests/common.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/event/tests/test_event_slot.py`, `addons/event/tests/common.py`, `addons/event/tests/test_event_mail_schedule.py`, `addons/event/tests/test_event_internals.py`, `addons/event/tests/test_mailing.py`, `addons/event/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 40; representative identifiers: `res_groups_privilege_events`, `group_event_registration_desk`, `group_event_user`, `group_event_manager`, `event_report_template_foldable_badge`, `event_report_template_a6_badge`, `event_report_template_four_per_sheet_badge`, `event_registration_report_template_badge`, `event_event_report_template_badge`, `event_report_template_full_page_ticket`, `event_report_full_page_ticket_layout`, `event_registration_report_template_full_page_ticket`, `event_event_report_template_full_page_ticket`, `event_registration_report_template_responsive_html_ticket`, `event_report_template_badge_card`, `event_report_template_formatted_event_address`, `paperformat_event_badge`, `paperformat_event_full_page_ticket`, `action_report_event_registration_full_page_ticket`, `action_report_event_event_full_page_ticket`
- Menus: 12; representative evidence: `addons/event/views/res_config_settings_views.xml:94`, `addons/event/views/event_registration_views.xml:384`, `addons/event/views/event_event_views.xml:369`, `addons/event/views/event_menu_views.xml:5`, `addons/event/views/event_menu_views.xml:12`, `addons/event/views/event_menu_views.xml:19`, `addons/event/views/event_menu_views.xml:26`, `addons/event/views/event_menu_views.xml:31`, `addons/event/views/event_menu_views.xml:35`, `addons/event/views/event_menu_views.xml:39`, `addons/event/views/event_menu_views.xml:44`, `addons/event/views/event_menu_views.xml:48`
- Templates: 17; representative evidence: `addons/event/report/event_event_templates.xml:6`, `addons/event/report/event_event_templates.xml:110`, `addons/event/report/event_event_templates.xml:123`, `addons/event/report/event_event_templates.xml:143`, `addons/event/report/event_event_templates.xml:159`, `addons/event/report/event_event_templates.xml:173`, `addons/event/report/event_event_templates.xml:260`, `addons/event/report/event_event_templates.xml:291`, `addons/event/report/event_event_templates.xml:302`, `addons/event/report/event_event_templates.xml:315`, `addons/event/report/event_event_templates.xml:328`, `addons/event/report/event_event_templates.xml:401`
- View/action field declarations: 138; representative evidence: `addons/event/report/event_event_reports.xml:42`, `addons/event/report/event_event_reports.xml:53`, `addons/event/report/event_event_reports.xml:64`, `addons/event/report/event_event_reports.xml:75`, `addons/event/report/event_event_reports.xml:86`, `addons/event/report/event_event_reports.xml:93`, `addons/event/report/event_registration_report.xml:6`, `addons/event/data/event_demo.xml:84`, `addons/event/data/event_demo.xml:95`, `addons/event/data/event_demo.xml:104`, `addons/event/views/digest_views.xml:5`, `addons/event/views/digest_views.xml:7`
- Browser assets: 16; representative files: `addons/event/static/src/event_state_selection_field/event_state_selection_field.js`, `addons/event/static/src/icon_selection_field/icon_selection_field.js`, `addons/event/static/src/client_action/event_barcode.js`, `addons/event/static/src/client_action/event_registration_summary_dialog.js`, `addons/event/static/src/template_reference_field/field_event_mail_template_reference.js`, `addons/event/static/src/views/event_registration_kanban_controller.js`, `addons/event/static/src/views/event_registration_list_controller.js`, `addons/event/static/src/js/tours/event_steps.js`, `addons/event/static/src/js/tours/event_tour.js`, `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_controller.js`, `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_renderer.js`, `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_model.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/event/__manifest__.py`
- **HTTP entry points:** `addons/event/controllers/portal.py:14`, `addons/event/controllers/main.py:16`, `addons/event/controllers/main.py:35`, `addons/event/controllers/main.py:87`
- **Scheduled entry points:** `addons/event/__manifest__.py`, `addons/event/models/event_event.py`, `addons/event/models/event_registration.py`, `addons/event/data/ir_cron_data.xml`, `addons/event/tests/test_event_mail_schedule.py`
- **Report entry points:** `addons/event/controllers/main.py`, `addons/event/report/event_event_reports.xml`, `addons/event/report/event_registration_report.xml`, `addons/event/tests/common.py`

## 7. Database interactions

- Model declarations: 20
- Representative model evidence: inherits `res.partner` (addons/event/models/res_partner.py:14); `event.question.answer` (addons/event/models/event_question_answer.py:8); `event.mail.registration` (addons/event/models/event_mail_registration.py:11); `event.event.ticket` (addons/event/models/event_ticket.py:8); inherits `digest.digest` (addons/event/models/digest.py:6); `event.registration.answer` (addons/event/models/event_registration_answer.py:7); inherits `mail.template` (addons/event/models/mail_template.py:7); inherits `res.config.settings` (addons/event/models/res_config_settings.py:10); `event.mail` (addons/event/models/event_mail.py:25); `event.type.ticket` (addons/event/models/event_type_ticket.py:4); `event.slot` (addons/event/models/event_slot.py:14); `event.type` (addons/event/models/event_type.py:5); `event.question` (addons/event/models/event_question.py:7); `event.tag.category` (addons/event/models/event_tag.py:9); `event.tag` (addons/event/models/event_tag.py:27); `event.type.mail` (addons/event/models/event_type_mail.py:4); `event.event` (addons/event/models/event_event.py:31); `event.registration` (addons/event/models/event_registration.py:14); `event.mail.slot` (addons/event/models/event_mail_slot.py:5); `event.stage` (addons/event/models/event_stage.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 4
- Route evidence: `addons/event/controllers/portal.py:14`, `addons/event/controllers/main.py:16`, `addons/event/controllers/main.py:35`, `addons/event/controllers/main.py:87`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `barcodes`, `base_setup`, `digest`, `mail`, `phone_validation`, `portal`, `utm`
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

- `addons/event/__init__.py`
- `addons/event/__manifest__.py`
- `addons/event/controllers/__init__.py`
- `addons/event/controllers/main.py`
- `addons/event/controllers/portal.py`
- `addons/event/data/digest_data.xml`
- `addons/event/data/event_data.xml`
- `addons/event/data/event_demo.xml`
- `addons/event/data/event_demo_misc.xml`
- `addons/event/data/event_question_data.xml`
- `addons/event/data/event_registration_demo.xml`
- `addons/event/data/event_tour.xml`
- `addons/event/data/ir_cron_data.xml`
- `addons/event/data/mail_template_data.xml`
- `addons/event/data/portal_entry_data.xml`
- `addons/event/data/res_partner_demo.xml`
- `addons/event/data/res_users_demo.xml`
- `addons/event/i18n/af.po`
- `addons/event/i18n/am.po`
- `addons/event/i18n/ar.po`
- `addons/event/i18n/az.po`
- `addons/event/i18n/bg.po`
- `addons/event/i18n/bs.po`
- `addons/event/i18n/ca.po`
- `addons/event/i18n/cs.po`
- `addons/event/i18n/da.po`
- `addons/event/i18n/de.po`
- `addons/event/i18n/el.po`
- `addons/event/i18n/es.po`
- `addons/event/i18n/es_419.po`
- `addons/event/i18n/es_CL.po`
- `addons/event/i18n/et.po`
- `addons/event/i18n/eu.po`
- `addons/event/i18n/event.pot`
- `addons/event/i18n/fa.po`
- `addons/event/i18n/fi.po`
- `addons/event/i18n/fo.po`
- `addons/event/i18n/fr.po`
- `addons/event/i18n/fr_BE.po`
- `addons/event/i18n/fr_CA.po`
- `addons/event/i18n/gl.po`
- `addons/event/i18n/gu.po`
- `addons/event/i18n/he.po`
- `addons/event/i18n/hi.po`
- `addons/event/i18n/hr.po`
- `addons/event/i18n/hu.po`
- `addons/event/i18n/id.po`
- `addons/event/i18n/is.po`
- `addons/event/i18n/it.po`
- `addons/event/i18n/ja.po`
- `addons/event/i18n/ka.po`
- `addons/event/i18n/kab.po`
- `addons/event/i18n/km.po`
- `addons/event/i18n/ko.po`
- `addons/event/i18n/ku.po`
- `addons/event/i18n/lb.po`
- `addons/event/i18n/lo.po`
- `addons/event/i18n/lt.po`
- `addons/event/i18n/lv.po`
- `addons/event/i18n/mk.po`
- `addons/event/i18n/mn.po`
- `addons/event/i18n/my.po`
- `addons/event/i18n/nb.po`
- `addons/event/i18n/nl.po`
- `addons/event/i18n/pl.po`
- `addons/event/i18n/pt.po`
- `addons/event/i18n/pt_BR.po`
- `addons/event/i18n/ro.po`
- `addons/event/i18n/ru.po`
- `addons/event/i18n/sk.po`
- `addons/event/i18n/sl.po`
- `addons/event/i18n/sq.po`
- `addons/event/i18n/sr@latin.po`
- `addons/event/i18n/sv.po`
- `addons/event/i18n/th.po`
- `addons/event/i18n/tr.po`
- `addons/event/i18n/uk.po`
- `addons/event/i18n/uz.po`
- `addons/event/i18n/vi.po`
- `addons/event/i18n/zh_CN.po`
- `addons/event/i18n/zh_TW.po`
- `addons/event/models/__init__.py`
- `addons/event/models/digest.py`
- `addons/event/models/event_event.py`
- `addons/event/models/event_mail.py`
- `addons/event/models/event_mail_registration.py`
- `addons/event/models/event_mail_slot.py`
- `addons/event/models/event_question.py`
- `addons/event/models/event_question_answer.py`
- `addons/event/models/event_registration.py`
- `addons/event/models/event_registration_answer.py`
- `addons/event/models/event_slot.py`
- `addons/event/models/event_stage.py`
- `addons/event/models/event_tag.py`
- `addons/event/models/event_ticket.py`
- `addons/event/models/event_type.py`
- `addons/event/models/event_type_mail.py`
- `addons/event/models/event_type_ticket.py`
- `addons/event/models/mail_template.py`
- `addons/event/models/res_config_settings.py`
- `addons/event/models/res_partner.py`
- `addons/event/report/__init__.py`
- `addons/event/report/event_event_reports.xml`
- `addons/event/report/event_event_templates.xml`
- `addons/event/report/event_registration_report.xml`
- `addons/event/security/event_security.xml`
- `addons/event/security/ir.access.csv`
- `addons/event/static/description/icon.png`
- `addons/event/static/description/icon.svg`
- `addons/event/static/description/icon_hi.png`
- `addons/event/static/src/client_action/event_barcode.js`
- `addons/event/static/src/client_action/event_barcode.scss`
- `addons/event/static/src/client_action/event_barcode.xml`
- `addons/event/static/src/client_action/event_registration_summary_dialog.js`
- `addons/event/static/src/client_action/event_registration_summary_dialog.xml`
- `addons/event/static/src/event_state_selection_field/event_state_selection_field.js`
- `addons/event/static/src/event_state_selection_field/event_state_selection_field.scss`
- `addons/event/static/src/event_state_selection_field/event_state_selection_field.xml`
- `addons/event/static/src/icon_selection_field/icon_selection_field.js`
- `addons/event/static/src/icon_selection_field/icon_selection_field.xml`
- `addons/event/static/src/img/apple-calendar-128.png`
- `addons/event/static/src/img/apple-calendar.svg`
- `addons/event/static/src/img/event_ticket.svg`
- `addons/event/static/src/img/google-calendar-128.png`
- `addons/event/static/src/img/google-calendar.svg`
- `addons/event/static/src/img/how_to_fold_1.png`
- `addons/event/static/src/img/how_to_fold_2.png`
- `addons/event/static/src/img/how_to_fold_3.png`
- `addons/event/static/src/img/how_to_fold_4.png`
- `addons/event/static/src/img/outlook-calendar-128.png`
- `addons/event/static/src/img/outlook-calendar.svg`
- `addons/event/static/src/img/partner_bloem.png`
- `addons/event/static/src/img/partner_pterocarpus.png`
- `addons/event/static/src/img/partner_tree_dealers.png`
- `addons/event/static/src/js/tours/event_steps.js`
- `addons/event/static/src/js/tours/event_tour.js`
- `addons/event/static/src/scss/event.scss`
- `addons/event/static/src/scss/event_badge_report.scss`
- `addons/event/static/src/scss/event_full_page_ticket_report.scss`
- `addons/event/static/src/scss/event_full_page_ticket_report_pdf.scss`
- `addons/event/static/src/scss/event_full_page_ticket_responsive_html_report.scss`
- `addons/event/static/src/template_reference_field/field_event_mail_template_reference.js`
- `addons/event/static/src/template_reference_field/field_event_mail_template_reference.scss`
- `addons/event/static/src/template_reference_field/field_event_mail_template_reference.xml`
- `addons/event/static/src/views/event_registration_kanban_controller.js`
- `addons/event/static/src/views/event_registration_list_controller.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_common_renderer.xml`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_controller.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_controller.xml`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_model.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_renderer.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_calendar_view.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_multi_selection_buttons.js`
- `addons/event/static/src/views/event_slot/calendar/event_slot_multi_selection_buttons.xml`
- `addons/event/static/src/views/event_slot/list/event_slot_list_controller.js`
- `addons/event/static/src/views/event_slot/list/event_slot_list_view.js`
- `addons/event/tests/__init__.py`
- `addons/event/tests/common.py`
- `addons/event/tests/test_event_internals.py`
- `addons/event/tests/test_event_mail_schedule.py`
- `addons/event/tests/test_event_slot.py`
- `addons/event/tests/test_mailing.py`
- `addons/event/views/digest_views.xml`
- `addons/event/views/event_event_views.xml`
- `addons/event/views/event_mail_views.xml`
- `addons/event/views/event_menu_views.xml`
- `addons/event/views/event_question_views.xml`
- `addons/event/views/event_registration_answer_views.xml`
- `addons/event/views/event_registration_views.xml`
- `addons/event/views/event_slot_views.xml`
- `addons/event/views/event_stage_views.xml`
- `addons/event/views/event_tag_views.xml`
- `addons/event/views/event_templates.xml`
- `addons/event/views/event_ticket_views.xml`
- `addons/event/views/event_type_views.xml`
- `addons/event/views/portal_templates.xml`
- `addons/event/views/res_config_settings_views.xml`
- `addons/event/views/res_partner_views.xml`
