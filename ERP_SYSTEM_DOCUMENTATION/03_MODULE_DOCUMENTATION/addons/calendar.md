# Module: calendar

- **Module ID:** MOD-046
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/calendar`
- **Manifest:** `addons/calendar/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Productivity/Calendar`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Schedule employees' meetings

**Manifest description:**

This is a full-featured calendar system.
========================================

It supports:
------------
    - Calendar of events
    - Recurring events

If you need to manage your meetings, you should install the CRM module.

**Scope evidence:** The module contains 230 files, including 47 Python, 39 XML, and 59 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `mail`.

## 2. Module structure

- Model/business logic files: 20
- Controller/API files: 2
- XML/data/view/template files: 39
- Browser asset files: 59
- Security files: 1
- Test files: 20
- Scheduled/automation evidence files: 7
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/calendar/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 20 model declarations, 521 methods, 1 constraint handlers, 4 onchange handlers, and 41 dependency declarations.
- **Evidence:** `addons/calendar/models/res_partner.py:11`, `addons/calendar/models/mail_activity.py:9`, `addons/calendar/models/calendar_event_type.py:8`, `addons/calendar/models/discuss_channel.py:10`, `addons/calendar/models/calendar_filter.py:8`, `addons/calendar/models/res_users_settings.py:6`, `addons/calendar/models/mail_activity_mixin.py:6`, `addons/calendar/models/calendar_event.py:96`, `addons/calendar/models/calendar_user.py:7`, `addons/calendar/models/ir_http.py:9`, `addons/calendar/models/calendar_attendee.py:14`, `addons/calendar/models/calendar_calendar.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 10 route declarations.
- **Evidence:** `addons/calendar/controllers/main.py:14`, `addons/calendar/controllers/main.py:22`, `addons/calendar/controllers/main.py:36`, `addons/calendar/controllers/main.py:44`, `addons/calendar/controllers/main.py:58`, `addons/calendar/controllers/main.py:87`, `addons/calendar/controllers/main.py:103`, `addons/calendar/controllers/main.py:114`, `addons/calendar/controllers/main.py:118`, `addons/calendar/controllers/main.py:122`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 39 XML files and 59 JavaScript/TypeScript files; static XML analysis found 75 record/template/menu identifiers.
- **Evidence:** `addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.xml:3`, `addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.xml:3`, `addons/calendar/wizard/mail_activity_schedule_views.xml:4`, `addons/calendar/data/calendar_cron.xml:5`, `addons/calendar/data/mail_template_data.xml:4`, `addons/calendar/data/mail_template_data.xml:148`, `addons/calendar/data/mail_template_data.xml:301`, `addons/calendar/data/mail_template_data.xml:435`, `addons/calendar/data/mail_template_data.xml:559`, `addons/calendar/data/mail_activity_type_data.xml:4`, `addons/calendar/data/mail_message_subtype_data.xml:4`, `addons/calendar/data/mail_message_subtype_data.xml:11`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/calendar/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 7 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/calendar/__manifest__.py`, `addons/calendar/models/calendar_filter.py`, `addons/calendar/models/calendar_event.py`, `addons/calendar/models/calendar_recurrence.py`, `addons/calendar/data/calendar_cron.xml`, `addons/calendar/tests/test_access_rights.py`, `addons/calendar/tests/test_event_notifications.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 20 test files are present.
- **Evidence:** `addons/calendar/tests/test_access_rights.py`, `addons/calendar/tests/test_discuss_meetings.py`, `addons/calendar/tests/test_calendar_tour.py`, `addons/calendar/tests/test_calendar_event_calendar.py`, `addons/calendar/tests/test_res_users.py`, `addons/calendar/tests/test_calendar_user.py`, `addons/calendar/tests/test_calendar_controller.py`, `addons/calendar/tests/test_attendees.py`, `addons/calendar/tests/test_res_users_calendars.py`, `addons/calendar/tests/test_event_recurrence.py`, `addons/calendar/tests/test_calendar_calendar.py`, `addons/calendar/tests/test_event_notifications.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 39; representative identifiers: `calendar_event_multi_archive_or_unlink_wizard_view_form`, `calendar_event_archive_or_unlink_wizard_view_form`, `mail_activity_schedule_view_form`, `ir_cron_scheduler_alarm`, `calendar_template_meeting_invitation`, `calendar_template_meeting_changedate`, `calendar_template_meeting_reminder`, `calendar_template_meeting_update`, `calendar_template_delete_event`, `mail.mail_activity_data_meeting`, `calendar.subtype_invitation`, `calendar.mt_calendar_event_updated`, `alarm_notif_1`, `alarm_notif_2`, `alarm_notif_3`, `alarm_notif_4`, `alarm_notif_5`, `alarm_mail_1`, `alarm_mail_2`, `alarm_mail_1_day`
- Menus: 10; representative evidence: `addons/calendar/views/calendar_views.xml:590`, `addons/calendar/views/calendar_views.xml:597`, `addons/calendar/views/calendar_views.xml:605`, `addons/calendar/views/calendar_views.xml:612`, `addons/calendar/views/calendar_views.xml:620`, `addons/calendar/views/calendar_views.xml:628`, `addons/calendar/views/calendar_views.xml:635`, `addons/calendar/views/calendar_views.xml:642`, `addons/calendar/views/calendar_views.xml:648`, `addons/calendar/views/calendar_views.xml:653`
- Templates: 2; representative evidence: `addons/calendar/data/mail_templates_chatter.xml:4`, `addons/calendar/views/calendar_templates.xml:4`
- View/action field declarations: 61; representative evidence: `addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.xml:5`, `addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.xml:6`, `addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.xml:5`, `addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.xml:6`, `addons/calendar/wizard/mail_activity_schedule_views.xml:6`, `addons/calendar/wizard/mail_activity_schedule_views.xml:8`, `addons/calendar/data/mail_message_subtype_data.xml:6`, `addons/calendar/data/mail_message_subtype_data.xml:13`, `addons/calendar/views/res_config_settings_views.xml:5`, `addons/calendar/views/res_config_settings_views.xml:7`, `addons/calendar/views/calendar_calendar_views.xml:5`, `addons/calendar/views/calendar_calendar_views.xml:6`
- Browser assets: 59; representative files: `addons/calendar/static/tests/activity_widget.test.js`, `addons/calendar/static/tests/messaging_menu.test.js`, `addons/calendar/static/tests/activity.test.js`, `addons/calendar/static/tests/attendee_calendar_views.test.js`, `addons/calendar/static/tests/calendar_notification.test.js`, `addons/calendar/static/tests/calendar.test.js`, `addons/calendar/static/tests/calendar_test_helpers.js`, `addons/calendar/static/tests/activity_menu.test.js`, `addons/calendar/static/src/views/ask_recurrence_update_policy_hook.js`, `addons/calendar/static/src/views/hooks.js`, `addons/calendar/static/src/views/ask_recurrence_update_policy_dialog.js`, `addons/calendar/static/src/js/services/calendar_notification_service.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/calendar/__manifest__.py`
- **HTTP entry points:** `addons/calendar/controllers/main.py:14`, `addons/calendar/controllers/main.py:22`, `addons/calendar/controllers/main.py:36`, `addons/calendar/controllers/main.py:44`, `addons/calendar/controllers/main.py:58`, `addons/calendar/controllers/main.py:87`, `addons/calendar/controllers/main.py:103`, `addons/calendar/controllers/main.py:114`, `addons/calendar/controllers/main.py:118`, `addons/calendar/controllers/main.py:122`
- **Scheduled entry points:** `addons/calendar/__manifest__.py`, `addons/calendar/models/calendar_filter.py`, `addons/calendar/models/calendar_event.py`, `addons/calendar/models/calendar_recurrence.py`, `addons/calendar/data/calendar_cron.xml`, `addons/calendar/tests/test_access_rights.py`, `addons/calendar/tests/test_event_notifications.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 20
- Representative model evidence: inherits `res.partner` (addons/calendar/models/res_partner.py:11); inherits `mail.activity` (addons/calendar/models/mail_activity.py:9); `calendar.event.type` (addons/calendar/models/calendar_event_type.py:8); inherits `discuss.channel` (addons/calendar/models/discuss_channel.py:10); `calendar.filters` (addons/calendar/models/calendar_filter.py:8); inherits `res.users.settings` (addons/calendar/models/res_users_settings.py:6); inherits `mail.activity.mixin` (addons/calendar/models/mail_activity_mixin.py:6); `calendar.event` (addons/calendar/models/calendar_event.py:96); `calendar.user` (addons/calendar/models/calendar_user.py:7); inherits `ir.http` (addons/calendar/models/ir_http.py:9); `calendar.attendee` (addons/calendar/models/calendar_attendee.py:14); `calendar.calendar` (addons/calendar/models/calendar_calendar.py:5); inherits `mail.activity.type` (addons/calendar/models/mail_activity_type.py:6); `calendar.alarm` (addons/calendar/models/calendar_alarm.py:7); `calendar.alarm_manager` (addons/calendar/models/calendar_alarm_manager.py:11); inherits `res.users` (addons/calendar/models/res_users.py:10); `calendar.recurrence` (addons/calendar/models/calendar_recurrence.py:93); `calendar.event.archive.or.unlink.wizard` (addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.py:6); `calendar.event.multi.archive.or.unlink.wizard` (addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.py:4); inherits `mail.activity.schedule` (addons/calendar/wizard/mail_activity_schedule.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 10
- Route evidence: `addons/calendar/controllers/main.py:14`, `addons/calendar/controllers/main.py:22`, `addons/calendar/controllers/main.py:36`, `addons/calendar/controllers/main.py:44`, `addons/calendar/controllers/main.py:58`, `addons/calendar/controllers/main.py:87`, `addons/calendar/controllers/main.py:103`, `addons/calendar/controllers/main.py:114`, `addons/calendar/controllers/main.py:118`, `addons/calendar/controllers/main.py:122`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `mail`
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

- `addons/calendar/__init__.py`
- `addons/calendar/__manifest__.py`
- `addons/calendar/controllers/__init__.py`
- `addons/calendar/controllers/main.py`
- `addons/calendar/data/calendar_cron.xml`
- `addons/calendar/data/calendar_data.xml`
- `addons/calendar/data/calendar_demo.xml`
- `addons/calendar/data/mail_activity_type_data.xml`
- `addons/calendar/data/mail_message_subtype_data.xml`
- `addons/calendar/data/mail_template_data.xml`
- `addons/calendar/data/mail_templates_chatter.xml`
- `addons/calendar/i18n/af.po`
- `addons/calendar/i18n/am.po`
- `addons/calendar/i18n/ar.po`
- `addons/calendar/i18n/az.po`
- `addons/calendar/i18n/bg.po`
- `addons/calendar/i18n/bn.po`
- `addons/calendar/i18n/bs.po`
- `addons/calendar/i18n/ca.po`
- `addons/calendar/i18n/calendar.pot`
- `addons/calendar/i18n/cs.po`
- `addons/calendar/i18n/da.po`
- `addons/calendar/i18n/de.po`
- `addons/calendar/i18n/el.po`
- `addons/calendar/i18n/es.po`
- `addons/calendar/i18n/es_419.po`
- `addons/calendar/i18n/es_CL.po`
- `addons/calendar/i18n/et.po`
- `addons/calendar/i18n/eu.po`
- `addons/calendar/i18n/fa.po`
- `addons/calendar/i18n/fi.po`
- `addons/calendar/i18n/fo.po`
- `addons/calendar/i18n/fr.po`
- `addons/calendar/i18n/fr_BE.po`
- `addons/calendar/i18n/fr_CA.po`
- `addons/calendar/i18n/gl.po`
- `addons/calendar/i18n/gu.po`
- `addons/calendar/i18n/he.po`
- `addons/calendar/i18n/hi.po`
- `addons/calendar/i18n/hr.po`
- `addons/calendar/i18n/hu.po`
- `addons/calendar/i18n/id.po`
- `addons/calendar/i18n/is.po`
- `addons/calendar/i18n/it.po`
- `addons/calendar/i18n/ja.po`
- `addons/calendar/i18n/ka.po`
- `addons/calendar/i18n/kab.po`
- `addons/calendar/i18n/km.po`
- `addons/calendar/i18n/ko.po`
- `addons/calendar/i18n/ku.po`
- `addons/calendar/i18n/lo.po`
- `addons/calendar/i18n/lt.po`
- `addons/calendar/i18n/lv.po`
- `addons/calendar/i18n/mk.po`
- `addons/calendar/i18n/mn.po`
- `addons/calendar/i18n/my.po`
- `addons/calendar/i18n/nb.po`
- `addons/calendar/i18n/nl.po`
- `addons/calendar/i18n/pl.po`
- `addons/calendar/i18n/pt.po`
- `addons/calendar/i18n/pt_BR.po`
- `addons/calendar/i18n/ro.po`
- `addons/calendar/i18n/ru.po`
- `addons/calendar/i18n/sk.po`
- `addons/calendar/i18n/sl.po`
- `addons/calendar/i18n/sq.po`
- `addons/calendar/i18n/sr@latin.po`
- `addons/calendar/i18n/sv.po`
- `addons/calendar/i18n/th.po`
- `addons/calendar/i18n/tr.po`
- `addons/calendar/i18n/uk.po`
- `addons/calendar/i18n/uz.po`
- `addons/calendar/i18n/vi.po`
- `addons/calendar/i18n/zh_CN.po`
- `addons/calendar/i18n/zh_TW.po`
- `addons/calendar/models/__init__.py`
- `addons/calendar/models/calendar_alarm.py`
- `addons/calendar/models/calendar_alarm_manager.py`
- `addons/calendar/models/calendar_attendee.py`
- `addons/calendar/models/calendar_calendar.py`
- `addons/calendar/models/calendar_event.py`
- `addons/calendar/models/calendar_event_type.py`
- `addons/calendar/models/calendar_filter.py`
- `addons/calendar/models/calendar_recurrence.py`
- `addons/calendar/models/calendar_user.py`
- `addons/calendar/models/discuss_channel.py`
- `addons/calendar/models/ir_http.py`
- `addons/calendar/models/mail_activity.py`
- `addons/calendar/models/mail_activity_mixin.py`
- `addons/calendar/models/mail_activity_type.py`
- `addons/calendar/models/res_partner.py`
- `addons/calendar/models/res_users.py`
- `addons/calendar/models/res_users_settings.py`
- `addons/calendar/models/utils.py`
- `addons/calendar/security/ir.access.csv`
- `addons/calendar/static/description/icon.png`
- `addons/calendar/static/description/icon.svg`
- `addons/calendar/static/description/icon_hi.png`
- `addons/calendar/static/src/core/common/@types/models.d.ts`
- `addons/calendar/static/src/core/common/calendar_event_model.js`
- `addons/calendar/static/src/core/web/@types/models.d.ts`
- `addons/calendar/static/src/core/web/activity_list_popover_item_patch.js`
- `addons/calendar/static/src/core/web/activity_list_popover_item_patch.xml`
- `addons/calendar/static/src/core/web/activity_menu_patch.js`
- `addons/calendar/static/src/core/web/activity_menu_patch.xml`
- `addons/calendar/static/src/core/web/activity_model_patch.js`
- `addons/calendar/static/src/core/web/activity_patch.js`
- `addons/calendar/static/src/core/web/activity_patch.xml`
- `addons/calendar/static/src/core/web/messaging_menu_model_patch.js`
- `addons/calendar/static/src/core/web/schedule_meeting.js`
- `addons/calendar/static/src/core/web/store_service_patch.js`
- `addons/calendar/static/src/img/apple-calendar-128.png`
- `addons/calendar/static/src/img/bell.png`
- `addons/calendar/static/src/img/check-circle.png`
- `addons/calendar/static/src/img/google-calendar-128.png`
- `addons/calendar/static/src/img/outlook-calendar-128.png`
- `addons/calendar/static/src/img/state_accepted.png`
- `addons/calendar/static/src/img/state_declined.png`
- `addons/calendar/static/src/img/state_needsAction.png`
- `addons/calendar/static/src/img/state_tentative.png`
- `addons/calendar/static/src/img/sync.png`
- `addons/calendar/static/src/img/times-circle.png`
- `addons/calendar/static/src/js/services/calendar_notification_service.js`
- `addons/calendar/static/src/scss/calendar.scss`
- `addons/calendar/static/src/scss/calendar_event_views.scss`
- `addons/calendar/static/src/scss/res_partner.scss`
- `addons/calendar/static/src/views/ask_recurrence_update_policy_dialog.js`
- `addons/calendar/static/src/views/ask_recurrence_update_policy_dialog.xml`
- `addons/calendar/static/src/views/ask_recurrence_update_policy_hook.js`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_common_renderer.js`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_common_renderer.xml`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_list_popover.js`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_list_popover.xml`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_list_popover_item.js`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_list_popover_item.xml`
- `addons/calendar/static/src/views/attendee_calendar/activity/attendee_calendar_activity_model.js`
- `addons/calendar/static/src/views/attendee_calendar/attendee_calendar_controller.js`
- `addons/calendar/static/src/views/attendee_calendar/attendee_calendar_controller.xml`
- `addons/calendar/static/src/views/attendee_calendar/attendee_calendar_model.js`
- `addons/calendar/static/src/views/attendee_calendar/attendee_calendar_renderer.js`
- `addons/calendar/static/src/views/attendee_calendar/attendee_calendar_view.js`
- `addons/calendar/static/src/views/attendee_calendar/common/attendee_calendar_common_popover.js`
- `addons/calendar/static/src/views/attendee_calendar/common/attendee_calendar_common_popover.xml`
- `addons/calendar/static/src/views/attendee_calendar/common/attendee_calendar_common_renderer.js`
- `addons/calendar/static/src/views/attendee_calendar/common/attendee_calendar_common_renderer.xml`
- `addons/calendar/static/src/views/attendee_calendar/filter_section/attendee_calendar_calendar_filter_section.js`
- `addons/calendar/static/src/views/attendee_calendar/filter_section/attendee_calendar_calendar_filter_section.xml`
- `addons/calendar/static/src/views/attendee_calendar/filter_section/attendee_calendar_filter_section.js`
- `addons/calendar/static/src/views/attendee_calendar/filter_section/attendee_calendar_filter_section.scss`
- `addons/calendar/static/src/views/attendee_calendar/filter_section/attendee_calendar_filter_section.xml`
- `addons/calendar/static/src/views/attendee_calendar/side_panel/attendee_calendar_side_panel.js`
- `addons/calendar/static/src/views/attendee_calendar/side_panel/attendee_calendar_side_panel.xml`
- `addons/calendar/static/src/views/attendee_calendar/year/attendee_calendar_year_popover.js`
- `addons/calendar/static/src/views/attendee_calendar/year/attendee_calendar_year_popover.xml`
- `addons/calendar/static/src/views/attendee_calendar/year/attendee_calendar_year_renderer.js`
- `addons/calendar/static/src/views/calendar_form/calendar_event_form_controller.js`
- `addons/calendar/static/src/views/calendar_form/calendar_event_form_model.js`
- `addons/calendar/static/src/views/calendar_form/calendar_event_form_view.js`
- `addons/calendar/static/src/views/calendar_form/calendar_event_quick_create.js`
- `addons/calendar/static/src/views/calendar_form/calendar_event_quick_create.xml`
- `addons/calendar/static/src/views/calendar_form/calendar_form_dialog.js`
- `addons/calendar/static/src/views/calendar_form/calendar_form_dialog.xml`
- `addons/calendar/static/src/views/fields/calendar_notes_html_field.js`
- `addons/calendar/static/src/views/fields/calendar_open_event_field.js`
- `addons/calendar/static/src/views/fields/calendar_open_event_field.xml`
- `addons/calendar/static/src/views/fields/many2many_attendee.js`
- `addons/calendar/static/src/views/fields/many2many_attendee.scss`
- `addons/calendar/static/src/views/fields/many2many_attendee.xml`
- `addons/calendar/static/src/views/fields/many2many_attendee_email.js`
- `addons/calendar/static/src/views/fields/many2many_attendee_email.xml`
- `addons/calendar/static/src/views/fields/many2many_attendee_expandable.js`
- `addons/calendar/static/src/views/fields/many2many_attendee_expandable.xml`
- `addons/calendar/static/src/views/hooks.js`
- `addons/calendar/static/src/views/list_view/calendar_list_controller.js`
- `addons/calendar/static/src/views/list_view/calendar_list_view.js`
- `addons/calendar/static/src/views/widgets/calendar_week_days.js`
- `addons/calendar/static/src/views/widgets/calendar_week_days.scss`
- `addons/calendar/static/src/views/widgets/calendar_week_days.xml`
- `addons/calendar/static/tests/activity.test.js`
- `addons/calendar/static/tests/activity_menu.test.js`
- `addons/calendar/static/tests/activity_widget.test.js`
- `addons/calendar/static/tests/attendee_calendar_views.test.js`
- `addons/calendar/static/tests/calendar.test.js`
- `addons/calendar/static/tests/calendar_notification.test.js`
- `addons/calendar/static/tests/calendar_test_helpers.js`
- `addons/calendar/static/tests/messaging_menu.test.js`
- `addons/calendar/static/tests/mock_server/mock_models/calendar_attendee.js`
- `addons/calendar/static/tests/mock_server/mock_models/calendar_calendar.js`
- `addons/calendar/static/tests/mock_server/mock_models/calendar_event.js`
- `addons/calendar/static/tests/mock_server/mock_models/calendar_filters.js`
- `addons/calendar/static/tests/mock_server/mock_models/calendar_user.js`
- `addons/calendar/static/tests/mock_server/mock_models/discuss_channel.js`
- `addons/calendar/static/tests/mock_server/mock_models/mail_activity.js`
- `addons/calendar/static/tests/mock_server/mock_models/res_users.js`
- `addons/calendar/static/tests/tours/calendar_tour.js`
- `addons/calendar/tests/__init__.py`
- `addons/calendar/tests/test_access_rights.py`
- `addons/calendar/tests/test_attendees.py`
- `addons/calendar/tests/test_calendar.py`
- `addons/calendar/tests/test_calendar_activity.py`
- `addons/calendar/tests/test_calendar_calendar.py`
- `addons/calendar/tests/test_calendar_controller.py`
- `addons/calendar/tests/test_calendar_event_calendar.py`
- `addons/calendar/tests/test_calendar_event_time_extraction.py`
- `addons/calendar/tests/test_calendar_recurrent_event_case2.py`
- `addons/calendar/tests/test_calendar_tour.py`
- `addons/calendar/tests/test_calendar_user.py`
- `addons/calendar/tests/test_discuss_meetings.py`
- `addons/calendar/tests/test_event_notifications.py`
- `addons/calendar/tests/test_event_recurrence.py`
- `addons/calendar/tests/test_mail_activity_mixin.py`
- `addons/calendar/tests/test_recurrence_rule.py`
- `addons/calendar/tests/test_res_partner.py`
- `addons/calendar/tests/test_res_users.py`
- `addons/calendar/tests/test_res_users_calendars.py`
- `addons/calendar/views/calendar_calendar_views.xml`
- `addons/calendar/views/calendar_templates.xml`
- `addons/calendar/views/calendar_user_views.xml`
- `addons/calendar/views/calendar_views.xml`
- `addons/calendar/views/mail_activity_views.xml`
- `addons/calendar/views/res_config_settings_views.xml`
- `addons/calendar/views/res_partner_views.xml`
- `addons/calendar/views/res_users_views.xml`
- `addons/calendar/wizard/__init__.py`
- `addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.py`
- `addons/calendar/wizard/calendar_event_archive_or_unlink_wizard.xml`
- `addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.py`
- `addons/calendar/wizard/calendar_event_multi_archive_or_unlink_wizard.xml`
- `addons/calendar/wizard/mail_activity_schedule.py`
- `addons/calendar/wizard/mail_activity_schedule_views.xml`
