# Module: mail

- **Module ID:** MOD-351
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mail`
- **Manifest:** `addons/mail/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Productivity/Discuss`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Chat, mail gateway and private channels

**Manifest description:**

Chat, mail gateway and private channel.
=======================================

Communicate with your colleagues/customers/guest within Odoo.

Discuss/Chat
------------
User-friendly "Discuss" features that allows one 2 one or group communication
(text chat/voice call/video call), invite guests and share documents with
them, all real-time.

Mail gateway
------------
Sending information and documents made simplified. You can send emails
from Odoo itself, and that too with great possibilities. For example,
design a beautiful email template for the invoices, and use the same
for all your customers, no need to do the same exercise every time.

Chatter
-------
Do all the contextual conversation on a document. For example on an
applicant, directly post an update to send email to the applicant,
schedule the next interview call, attach the contract, add HR officer
to the follower list to notify them for important events(with help of
subtypes),...


Retrieve incoming email on POP/IMAP servers.
============================================
Enter the parameters of your POP/IMAP account(s), and any incoming emails on
these accounts will be automatically downloaded into your Odoo system. All
POP3/IMAP-compatible servers are supported, included those that require an
encrypted SSL/TLS connection.
This can be used to easily create email-based workflows for many email-enabled Odoo documents, such as:

* CRM Leads/Opportunities
* CRM Claims
* Project Issues
* Project Tasks
* Human Resource Recruitment (Applicants)

Just install the relevant application, and you can assign any of these document
types (Leads, Project Issues) to your incoming email accounts. New emails will
automatically spawn new documents of the chosen type, so it's a snap to create a
mailbox-to-Odoo integration. Even better: these documents directly act as mini
conversations synchronized by email. You can reply from within Odoo, and the
answers will automatically be collected when they come back, and attached to the
same *conversation* document.
For more specific needs, you may also assign custom-defined actions
(technically: Server Actions) to be triggered for each incoming mail.

**Scope evidence:** The module contains 1444 files, including 201 Python, 271 XML, and 688 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `base_setup`, `bus`, `web_tour`, `html_editor`.

## 2. Module structure

- Model/business logic files: 94
- Controller/API files: 26
- XML/data/view/template files: 271
- Browser asset files: 688
- Security files: 1
- Test files: 66
- Scheduled/automation evidence files: 29
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mail/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 94 model declarations, 2053 methods, 26 constraint handlers, 9 onchange handlers, and 177 dependency declarations.
- **Evidence:** `addons/mail/models/res_partner.py:12`, `addons/mail/models/kpi_provider.py:6`, `addons/mail/models/ir_access.py:6`, `addons/mail/models/mail_mail.py:28`, `addons/mail/models/mail_message.py:100`, `addons/mail/models/ir_config_parameter.py:7`, `addons/mail/models/mail_activity.py:24`, `addons/mail/models/fetchmail.py:89`, `addons/mail/models/mail_thread_main_attachment.py:8`, `addons/mail/models/mail_poll.py:7`, `addons/mail/models/mail_message_translation.py:8`, `addons/mail/models/ir_ui_view.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 26 controller files and 20 route declarations.
- **Evidence:** `addons/mail/controllers/home.py:10`, `addons/mail/controllers/attachment.py:203`, `addons/mail/controllers/attachment.py:265`, `addons/mail/controllers/websocket.py:13`, `addons/mail/controllers/websocket.py:18`, `addons/mail/controllers/mail.py:216`, `addons/mail/controllers/mail.py:252`, `addons/mail/controllers/mail.py:272`, `addons/mail/controllers/mail.py:284`, `addons/mail/controllers/mail.py:373`, `addons/mail/controllers/discuss/rtc.py:58`, `addons/mail/controllers/discuss/rtc.py:156`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 271 XML files and 688 JavaScript/TypeScript files; static XML analysis found 365 record/template/menu identifiers.
- **Evidence:** `addons/mail/demo/mail_canned_response_demo.xml:5`, `addons/mail/demo/mail_activity_demo.xml:4`, `addons/mail/demo/mail_activity_demo.xml:10`, `addons/mail/demo/discuss_channel_demo.xml:5`, `addons/mail/demo/discuss_channel_demo.xml:9`, `addons/mail/demo/discuss_channel_demo.xml:13`, `addons/mail/demo/discuss_channel_demo.xml:17`, `addons/mail/demo/discuss_channel_demo.xml:22`, `addons/mail/demo/discuss_channel_demo.xml:25`, `addons/mail/demo/discuss_channel_demo.xml:30`, `addons/mail/demo/discuss_channel_demo.xml:35`, `addons/mail/demo/discuss_channel_demo.xml:40`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/mail/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 29 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mail/__manifest__.py`, `addons/mail/models/mail_mail.py`, `addons/mail/models/mail_activity.py`, `addons/mail/models/fetchmail.py`, `addons/mail/models/mail_message_translation.py`, `addons/mail/models/mail_push.py`, `addons/mail/models/mail_message_schedule.py`, `addons/mail/models/mail_presence.py`, `addons/mail/models/mail_thread.py`, `addons/mail/models/res_users.py`, `addons/mail/models/res_role.py`, `addons/mail/models/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/mail/models/mail_template.py`, `addons/mail/wizard/mail_compose_message.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 66 test files are present.
- **Evidence:** `addons/mail/tests/test_mail_message.py`, `addons/mail/tests/test_mail_template.py`, `addons/mail/tests/test_websocket_controller.py`, `addons/mail/tests/test_mail_message_search.py`, `addons/mail/tests/test_res_users.py`, `addons/mail/tests/test_mail_tools.py`, `addons/mail/tests/test_mail_poll.py`, `addons/mail/tests/test_font_to_img.py`, `addons/mail/tests/test_ir_mail_server.py`, `addons/mail/tests/test_res_role.py`, `addons/mail/tests/common_controllers.py`, `addons/mail/tests/test_mail_blacklist.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 271; representative identifiers: `mail_canned_response_bye`, `mail_activity_demo_admin_email`, `mail_activity_demo_admin_todo`, `mail.discuss_category_favorites`, `mail.discuss_category_products_services`, `mail.discuss_category_community`, `mail.discuss_category_admin`, `mail.channel_all_employees`, `mail.channel_admin`, `mail.channel_1`, `mail.channel_2`, `mail.channel_3`, `mail_message_channel_1_1`, `mail_message_channel_1_2`, `mail_message_channel_1_2_1`, `mail_message_channel_whole_1`, `mail_message_channel_whole_2`, `mail_message_channel_whole_2_1`, `mail_message_channel_whole_2_2`, `mail_message_channel_2_1`
- Menus: 39; representative evidence: `addons/mail/views/mail_menus.xml:3`, `addons/mail/views/mail_menus.xml:10`, `addons/mail/views/mail_menus.xml:17`, `addons/mail/views/mail_menus.xml:24`, `addons/mail/views/mail_menus.xml:30`, `addons/mail/views/mail_menus.xml:37`, `addons/mail/views/mail_menus.xml:43`, `addons/mail/views/mail_menus.xml:49`, `addons/mail/views/mail_menus.xml:55`, `addons/mail/views/mail_menus.xml:61`, `addons/mail/views/mail_menus.xml:67`, `addons/mail/views/mail_menus.xml:80`
- Templates: 24; representative evidence: `addons/mail/data/security_notifications_templates.xml:5`, `addons/mail/data/mail_templates_invite.xml:4`, `addons/mail/data/mail_templates_invite.xml:30`, `addons/mail/data/mail_templates_mailgateway.xml:4`, `addons/mail/data/mail_templates_mailgateway.xml:16`, `addons/mail/data/mail_templates_mailgateway.xml:25`, `addons/mail/data/mail_templates_mailgateway.xml:38`, `addons/mail/data/mail_templates_mailgateway.xml:43`, `addons/mail/data/mail_templates_chatter.xml:5`, `addons/mail/data/mail_templates_chatter.xml:12`, `addons/mail/data/mail_templates_chatter.xml:31`, `addons/mail/data/mail_templates_chatter.xml:52`
- View/action field declarations: 400; representative evidence: `addons/mail/demo/discuss_channel_demo.xml:48`, `addons/mail/demo/discuss_channel_demo.xml:57`, `addons/mail/demo/discuss_channel_demo.xml:66`, `addons/mail/demo/discuss_channel_demo.xml:78`, `addons/mail/demo/discuss_channel_demo.xml:94`, `addons/mail/demo/discuss_channel_demo.xml:104`, `addons/mail/demo/discuss_channel_demo.xml:114`, `addons/mail/demo/discuss_channel_demo.xml:126`, `addons/mail/demo/discuss_channel_demo.xml:208`, `addons/mail/demo/discuss_channel_demo.xml:223`, `addons/mail/demo/discuss_channel_demo.xml:233`, `addons/mail/demo/discuss_channel_demo.xml:242`
- Browser assets: 688; representative files: `addons/mail/push-to-talk-extension/background.js`, `addons/mail/push-to-talk-extension/utils.js`, `addons/mail/push-to-talk-extension/content.js`, `addons/mail/static/src/service_worker.js`, `addons/mail/static/tests/mail_test_helpers.js`, `addons/mail/static/tests/mail_test_helpers_contains.js`, `addons/mail/static/tests/mail_test_helpers_html.js`, `addons/mail/static/tests/mail_utils.test.js`, `addons/mail/static/tests/mail_shared_tests.js`, `addons/mail/static/tests/search.test.js`, `addons/mail/static/lib/idb-keyval/idb-keyval.js`, `addons/mail/static/lib/lame/lame.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mail/__manifest__.py`
- **HTTP entry points:** `addons/mail/controllers/home.py:10`, `addons/mail/controllers/attachment.py:203`, `addons/mail/controllers/attachment.py:265`, `addons/mail/controllers/websocket.py:13`, `addons/mail/controllers/websocket.py:18`, `addons/mail/controllers/mail.py:216`, `addons/mail/controllers/mail.py:252`, `addons/mail/controllers/mail.py:272`, `addons/mail/controllers/mail.py:284`, `addons/mail/controllers/mail.py:373`, `addons/mail/controllers/discuss/rtc.py:58`, `addons/mail/controllers/discuss/rtc.py:156`
- **Scheduled entry points:** `addons/mail/__manifest__.py`, `addons/mail/models/mail_mail.py`, `addons/mail/models/mail_activity.py`, `addons/mail/models/fetchmail.py`, `addons/mail/models/mail_message_translation.py`, `addons/mail/models/mail_push.py`, `addons/mail/models/mail_message_schedule.py`, `addons/mail/models/mail_presence.py`, `addons/mail/models/mail_thread.py`, `addons/mail/models/res_users.py`, `addons/mail/models/res_role.py`, `addons/mail/models/__init__.py`
- **Report entry points:** `addons/mail/models/mail_template.py`, `addons/mail/wizard/mail_compose_message.py`

## 7. Database interactions

- Model declarations: 94
- Representative model evidence: `res.partner` (addons/mail/models/res_partner.py:12); inherits `kpi.provider` (addons/mail/models/kpi_provider.py:6); `ir.access` (addons/mail/models/ir_access.py:6); `mail.mail` (addons/mail/models/mail_mail.py:28); `mail.message` (addons/mail/models/mail_message.py:100); inherits `ir.config_parameter` (addons/mail/models/ir_config_parameter.py:7); `mail.activity` (addons/mail/models/mail_activity.py:24); `fetchmail.server` (addons/mail/models/fetchmail.py:89); `mail.thread.main.attachment` (addons/mail/models/mail_thread_main_attachment.py:8); `mail.poll` (addons/mail/models/mail_poll.py:7); `mail.message.translation` (addons/mail/models/mail_message_translation.py:8); inherits `ir.ui.view` (addons/mail/models/ir_ui_view.py:5); inherits `res.groups` (addons/mail/models/res_groups.py:6); `mail.ice.server` (addons/mail/models/mail_ice_server.py:11); `mail.template` (addons/mail/models/mail_template.py:15); `mail.followers` (addons/mail/models/mail_followers.py:10); inherits `res.config.settings` (addons/mail/models/res_config_settings.py:15); `mail.link.preview` (addons/mail/models/mail_link_preview.py:17); inherits `ir.qweb` (addons/mail/models/ir_qweb.py:6); inherits `ir.websocket` (addons/mail/models/ir_websocket.py:21); `mail.canned.response` (addons/mail/models/mail_canned_response.py:11); inherits `ir.model` (addons/mail/models/ir_model.py:8); `mail.push` (addons/mail/models/mail_push.py:14); `mail.alias.mixin.optional` (addons/mail/models/mail_alias_mixin_optional.py:11); `mail.message.link.preview` (addons/mail/models/mail_message_link_preview.py:7); `mail.activity.mixin` (addons/mail/models/mail_activity_mixin.py:15); inherits `ir.model.fields` (addons/mail/models/ir_model_fields.py:7); `mail.message.schedule` (addons/mail/models/mail_message_schedule.py:14); `mail.render.mixin` (addons/mail/models/mail_render_mixin.py:59); `mail.composer.mixin` (addons/mail/models/mail_composer_mixin.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 26
- Route declarations: 20
- Route evidence: `addons/mail/controllers/home.py:10`, `addons/mail/controllers/attachment.py:203`, `addons/mail/controllers/attachment.py:265`, `addons/mail/controllers/websocket.py:13`, `addons/mail/controllers/websocket.py:18`, `addons/mail/controllers/mail.py:216`, `addons/mail/controllers/mail.py:252`, `addons/mail/controllers/mail.py:272`, `addons/mail/controllers/mail.py:284`, `addons/mail/controllers/mail.py:373`, `addons/mail/controllers/discuss/rtc.py:58`, `addons/mail/controllers/discuss/rtc.py:156`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `base_setup`, `bus`, `web_tour`, `html_editor`
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

- `addons/mail/README.md`
- `addons/mail/__init__.py`
- `addons/mail/__manifest__.py`
- `addons/mail/controllers/__init__.py`
- `addons/mail/controllers/attachment.py`
- `addons/mail/controllers/discuss/__init__.py`
- `addons/mail/controllers/discuss/channel.py`
- `addons/mail/controllers/discuss/gif.py`
- `addons/mail/controllers/discuss/messaging_menu.py`
- `addons/mail/controllers/discuss/public_page.py`
- `addons/mail/controllers/discuss/rtc.py`
- `addons/mail/controllers/discuss/search.py`
- `addons/mail/controllers/discuss/settings.py`
- `addons/mail/controllers/discuss/voice.py`
- `addons/mail/controllers/google_translate.py`
- `addons/mail/controllers/guest.py`
- `addons/mail/controllers/home.py`
- `addons/mail/controllers/im_status.py`
- `addons/mail/controllers/link_preview.py`
- `addons/mail/controllers/mail.py`
- `addons/mail/controllers/mailbox.py`
- `addons/mail/controllers/message_reaction.py`
- `addons/mail/controllers/messaging_menu.py`
- `addons/mail/controllers/poll.py`
- `addons/mail/controllers/store.py`
- `addons/mail/controllers/thread.py`
- `addons/mail/controllers/webclient.py`
- `addons/mail/controllers/webmanifest.py`
- `addons/mail/controllers/websocket.py`
- `addons/mail/data/discuss_channel_data.xml`
- `addons/mail/data/ir_actions_data.xml`
- `addons/mail/data/ir_config_parameter_data.xml`
- `addons/mail/data/ir_cron_data.xml`
- `addons/mail/data/mail_activity_type_data.xml`
- `addons/mail/data/mail_canned_response_data.xml`
- `addons/mail/data/mail_groups.xml`
- `addons/mail/data/mail_message_subtype_data.xml`
- `addons/mail/data/mail_templates_chatter.xml`
- `addons/mail/data/mail_templates_email_layouts.xml`
- `addons/mail/data/mail_templates_invite.xml`
- `addons/mail/data/mail_templates_mailgateway.xml`
- `addons/mail/data/neutralize.sql`
- `addons/mail/data/res_partner_data.xml`
- `addons/mail/data/security_notifications_templates.xml`
- `addons/mail/data/web_tour_tour.xml`
- `addons/mail/demo/discuss/call_debrief_discuss_demo.xml`
- `addons/mail/demo/discuss/fixtures/audio_opus_60s_long_3s_content.webm`
- `addons/mail/demo/discuss/fixtures/audio_physics_0s_20s_16k.mp3`
- `addons/mail/demo/discuss/fixtures/audio_physics_40s_60s_16k.mp3`
- `addons/mail/demo/discuss/fixtures/video_60s_long_3s_content_av1_opus.webm`
- `addons/mail/demo/discuss/public_channel_demo.xml`
- `addons/mail/demo/discuss/readonly_channel_demo.xml`
- `addons/mail/demo/discuss_channel_chat_demo.xml`
- `addons/mail/demo/discuss_channel_demo.xml`
- `addons/mail/demo/mail_activity_demo.xml`
- `addons/mail/demo/mail_canned_response_demo.xml`
- `addons/mail/demo/mail_poll_demo.xml`
- `addons/mail/demo/res_role_demo.xml`
- `addons/mail/i18n/af.po`
- `addons/mail/i18n/am.po`
- `addons/mail/i18n/ar.po`
- `addons/mail/i18n/az.po`
- `addons/mail/i18n/bg.po`
- `addons/mail/i18n/bs.po`
- `addons/mail/i18n/ca.po`
- `addons/mail/i18n/cs.po`
- `addons/mail/i18n/da.po`
- `addons/mail/i18n/de.po`
- `addons/mail/i18n/el.po`
- `addons/mail/i18n/es.po`
- `addons/mail/i18n/es_419.po`
- `addons/mail/i18n/es_CL.po`
- `addons/mail/i18n/et.po`
- `addons/mail/i18n/eu.po`
- `addons/mail/i18n/fa.po`
- `addons/mail/i18n/fi.po`
- `addons/mail/i18n/fo.po`
- `addons/mail/i18n/fr.po`
- `addons/mail/i18n/fr_CA.po`
- `addons/mail/i18n/gl.po`
- `addons/mail/i18n/gu.po`
- `addons/mail/i18n/he.po`
- `addons/mail/i18n/hi.po`
- `addons/mail/i18n/hr.po`
- `addons/mail/i18n/hu.po`
- `addons/mail/i18n/id.po`
- `addons/mail/i18n/is.po`
- `addons/mail/i18n/it.po`
- `addons/mail/i18n/ja.po`
- `addons/mail/i18n/ka.po`
- `addons/mail/i18n/kab.po`
- `addons/mail/i18n/km.po`
- `addons/mail/i18n/ko.po`
- `addons/mail/i18n/ku.po`
- `addons/mail/i18n/lo.po`
- `addons/mail/i18n/lt.po`
- `addons/mail/i18n/lv.po`
- `addons/mail/i18n/mail.pot`
- `addons/mail/i18n/mk.po`
- `addons/mail/i18n/mn.po`
- `addons/mail/i18n/my.po`
- `addons/mail/i18n/nb.po`
- `addons/mail/i18n/nl.po`
- `addons/mail/i18n/pl.po`
- `addons/mail/i18n/pt.po`
- `addons/mail/i18n/pt_BR.po`
- `addons/mail/i18n/ro.po`
- `addons/mail/i18n/ru.po`
- `addons/mail/i18n/sk.po`
- `addons/mail/i18n/sl.po`
- `addons/mail/i18n/sq.po`
- `addons/mail/i18n/sr@latin.po`
- `addons/mail/i18n/sv.po`
- `addons/mail/i18n/th.po`
- `addons/mail/i18n/tr.po`
- `addons/mail/i18n/uk.po`
- `addons/mail/i18n/uz.po`
- `addons/mail/i18n/vi.po`
- `addons/mail/i18n/zh_CN.po`
- `addons/mail/i18n/zh_TW.po`
- `addons/mail/models/__init__.py`
- `addons/mail/models/discuss/__init__.py`
- `addons/mail/models/discuss/bus.py`
- `addons/mail/models/discuss/bus_listener_mixin.py`
- `addons/mail/models/discuss/bus_sync_mixin.py`
- `addons/mail/models/discuss/discuss_call_history.py`
- `addons/mail/models/discuss/discuss_category.py`
- `addons/mail/models/discuss/discuss_channel.py`
- `addons/mail/models/discuss/discuss_channel_last_interest_update.py`
- `addons/mail/models/discuss/discuss_channel_member.py`
- `addons/mail/models/discuss/discuss_channel_rtc_session.py`
- `addons/mail/models/discuss/discuss_gif_favorite.py`
- `addons/mail/models/discuss/discuss_voice_metadata.py`
- `addons/mail/models/discuss/ir_attachment.py`
- `addons/mail/models/discuss/ir_websocket.py`
- `addons/mail/models/discuss/mail_guest.py`
- `addons/mail/models/discuss/mail_message.py`
- `addons/mail/models/discuss/res_groups.py`
- `addons/mail/models/discuss/res_partner.py`
- `addons/mail/models/discuss/res_users.py`
- `addons/mail/models/discuss/res_users_settings.py`
- `addons/mail/models/discuss/res_users_settings_volumes.py`
- `addons/mail/models/fetchmail.py`
- `addons/mail/models/ir_access.py`
- `addons/mail/models/ir_action_act_window.py`
- `addons/mail/models/ir_actions_server.py`
- `addons/mail/models/ir_attachment.py`
- `addons/mail/models/ir_config_parameter.py`
- `addons/mail/models/ir_cron.py`
- `addons/mail/models/ir_http.py`
- `addons/mail/models/ir_mail_server.py`
- `addons/mail/models/ir_model.py`
- `addons/mail/models/ir_model_fields.py`
- `addons/mail/models/ir_qweb.py`
- `addons/mail/models/ir_ui_menu.py`
- `addons/mail/models/ir_ui_view.py`
- `addons/mail/models/ir_websocket.py`
- `addons/mail/models/kpi_provider.py`
- `addons/mail/models/mail_activity.py`
- `addons/mail/models/mail_activity_mixin.py`
- `addons/mail/models/mail_activity_plan.py`
- `addons/mail/models/mail_activity_plan_template.py`
- `addons/mail/models/mail_activity_type.py`
- `addons/mail/models/mail_alias.py`
- `addons/mail/models/mail_alias_domain.py`
- `addons/mail/models/mail_alias_mixin.py`
- `addons/mail/models/mail_alias_mixin_optional.py`
- `addons/mail/models/mail_blacklist.py`
- `addons/mail/models/mail_call_artifact.py`
- `addons/mail/models/mail_canned_response.py`
- `addons/mail/models/mail_composer_mixin.py`
- `addons/mail/models/mail_followers.py`
- `addons/mail/models/mail_gateway_allowed.py`
- `addons/mail/models/mail_ice_server.py`
- `addons/mail/models/mail_link_preview.py`
- `addons/mail/models/mail_mail.py`
- `addons/mail/models/mail_message.py`
- `addons/mail/models/mail_message_link_preview.py`
- `addons/mail/models/mail_message_reaction.py`
- `addons/mail/models/mail_message_schedule.py`
- `addons/mail/models/mail_message_subtype.py`
- `addons/mail/models/mail_message_translation.py`
- `addons/mail/models/mail_notification.py`
- `addons/mail/models/mail_poll.py`
- `addons/mail/models/mail_poll_option.py`
- `addons/mail/models/mail_poll_vote.py`
- `addons/mail/models/mail_presence.py`
- `addons/mail/models/mail_push.py`
- `addons/mail/models/mail_push_device.py`
- `addons/mail/models/mail_render_mixin.py`
- `addons/mail/models/mail_scheduled_message.py`
- `addons/mail/models/mail_template.py`
- `addons/mail/models/mail_thread.py`
- `addons/mail/models/mail_thread_blacklist.py`
- `addons/mail/models/mail_thread_main_attachment.py`
- `addons/mail/models/mail_thread_subject_suggested.py`
- `addons/mail/models/mail_track_mixin.py`
- `addons/mail/models/mail_tracking_duration_mixin.py`
- `addons/mail/models/models.py`
- `addons/mail/models/res_company.py`
- `addons/mail/models/res_config_settings.py`
- `addons/mail/models/res_groups.py`
- `addons/mail/models/res_partner.py`
- `addons/mail/models/res_role.py`
- `addons/mail/models/res_users.py`
- `addons/mail/models/template_reset_mixin.py`
- `addons/mail/models/update.py`
- `addons/mail/push-to-talk-extension/README.md`
- `addons/mail/push-to-talk-extension/assets/icons/active_icon.png`
- `addons/mail/push-to-talk-extension/assets/icons/inactive_icon.png`
- `addons/mail/push-to-talk-extension/assets/screenshots/ext_store_screenshot.jpg`
- `addons/mail/push-to-talk-extension/background.js`
- `addons/mail/push-to-talk-extension/content.js`
- `addons/mail/push-to-talk-extension/manifest.json`
- `addons/mail/push-to-talk-extension/utils.js`
- `addons/mail/security/ir.access.csv`
- `addons/mail/static/description/icon.png`
- `addons/mail/static/description/icon.svg`
- `addons/mail/static/description/icon_hi.png`
- `addons/mail/static/img/Capture.PNG`
- `addons/mail/static/img/msg_discus4_attach2-datas.jpg`
- `addons/mail/static/img/red_envelope.png`
- `addons/mail/static/lib/idb-keyval/idb-keyval.js`
- `addons/mail/static/lib/lame/lame.js`
- `addons/mail/static/lib/odoo_sfu/odoo_sfu.js`
- `addons/mail/static/lib/odoo_sfu/odoo_sfu.licenses.txt`
- `addons/mail/static/lib/selfie_segmentation/selfie_segmentation.js`
- `addons/mail/static/scripts/odoo-mailgate.py`
- `addons/mail/static/src/audio/call-invitation.mp3`
- `addons/mail/static/src/audio/call-invitation.ogg`
- `addons/mail/static/src/audio/call-join.mp3`
- `addons/mail/static/src/audio/call-join.ogg`
- `addons/mail/static/src/audio/call-leave.mp3`
- `addons/mail/static/src/audio/call-leave.ogg`
- `addons/mail/static/src/audio/channel_01_out.mp3`
- `addons/mail/static/src/audio/channel_01_out.ogg`
- `addons/mail/static/src/audio/earphone-off.mp3`
- `addons/mail/static/src/audio/earphone-off.ogg`
- `addons/mail/static/src/audio/earphone-on.mp3`
- `addons/mail/static/src/audio/earphone-on.ogg`
- `addons/mail/static/src/audio/mic-off.mp3`
- `addons/mail/static/src/audio/mic-off.ogg`
- `addons/mail/static/src/audio/mic-on.mp3`
- `addons/mail/static/src/audio/mic-on.ogg`
- `addons/mail/static/src/audio/new-message.mp3`
- `addons/mail/static/src/audio/new-message.ogg`
- `addons/mail/static/src/audio/ptt-press.mp3`
- `addons/mail/static/src/audio/ptt-press.ogg`
- `addons/mail/static/src/audio/ptt-release.mp3`
- `addons/mail/static/src/audio/ptt-release.ogg`
- Additional source files not expanded in this page: 1194; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
