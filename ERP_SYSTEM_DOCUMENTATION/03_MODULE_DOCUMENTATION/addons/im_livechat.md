# Module: im_livechat

- **Module ID:** MOD-111
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/im_livechat`
- **Manifest:** `addons/im_livechat/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Website/Live Chat`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Chat with your website visitors

**Manifest description:**

Live Chat Support
==========================

Allow to drop instant messaging widgets on any web page that will communicate
with the current server and dispatch visitors request amongst several live
chat operators.
Help your customers with this chat, and analyse their feedback.

**Scope evidence:** The module contains 423 files, including 70 Python, 78 XML, and 185 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `digest`, `utm`, `phone_validation`.

## 2. Module structure

- Model/business logic files: 23
- Controller/API files: 20
- XML/data/view/template files: 78
- Browser asset files: 185
- Security files: 2
- Test files: 24
- Scheduled/automation evidence files: 2
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/im_livechat/security/im_livechat_channel_security.xml`, `addons/im_livechat/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 23 model declarations, 407 methods, 4 constraint handlers, 1 onchange handlers, and 50 dependency declarations.
- **Evidence:** `addons/im_livechat/models/res_partner.py:12`, `addons/im_livechat/models/im_livechat_expertise.py:8`, `addons/im_livechat/models/im_livechat_channel.py:17`, `addons/im_livechat/models/im_livechat_channel.py:639`, `addons/im_livechat/models/mail_message.py:5`, `addons/im_livechat/models/discuss_channel.py:32`, `addons/im_livechat/models/digest.py:7`, `addons/im_livechat/models/res_groups.py:7`, `addons/im_livechat/models/chatbot_script.py:14`, `addons/im_livechat/models/discuss_channel_member.py:10`, `addons/im_livechat/models/ir_qweb.py:5`, `addons/im_livechat/models/ir_websocket.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 20 controller files and 38 route declarations.
- **Evidence:** `addons/im_livechat/controllers/webclient.py:11`, `addons/im_livechat/controllers/thread.py:8`, `addons/im_livechat/controllers/main.py:20`, `addons/im_livechat/controllers/main.py:38`, `addons/im_livechat/controllers/main.py:49`, `addons/im_livechat/controllers/main.py:53`, `addons/im_livechat/controllers/main.py:57`, `addons/im_livechat/controllers/main.py:64`, `addons/im_livechat/controllers/main.py:69`, `addons/im_livechat/controllers/main.py:204`, `addons/im_livechat/controllers/main.py:211`, `addons/im_livechat/controllers/main.py:219`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 78 XML files and 185 JavaScript/TypeScript files; static XML analysis found 435 record/template/menu identifiers.
- **Evidence:** `addons/im_livechat/security/im_livechat_channel_security.xml:2`, `addons/im_livechat/security/im_livechat_channel_security.xml:8`, `addons/im_livechat/security/im_livechat_channel_security.xml:16`, `addons/im_livechat/report/im_livechat_conversation_report.xml:4`, `addons/im_livechat/report/im_livechat_conversation_report.xml:12`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:5`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:22`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:39`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:47`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:62`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:112`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:130`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/im_livechat/security/im_livechat_channel_security.xml`, `addons/im_livechat/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/im_livechat/models/discuss_channel.py`, `addons/im_livechat/models/discuss_channel_member.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/im_livechat/controllers/main.py`, `addons/im_livechat/report/im_livechat_conversation_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 24 test files are present.
- **Evidence:** `addons/im_livechat/tests/test_chatbot_internals.py`, `addons/im_livechat/tests/test_im_livechat_report.py`, `addons/im_livechat/tests/test_discuss_channel.py`, `addons/im_livechat/tests/test_res_users.py`, `addons/im_livechat/tests/test_im_livechat_support_page.py`, `addons/im_livechat/tests/chatbot_common.py`, `addons/im_livechat/tests/test_call.py`, `addons/im_livechat/tests/test_transcript.py`, `addons/im_livechat/tests/test_chatbot_form_ui.py`, `addons/im_livechat/tests/common.py`, `addons/im_livechat/tests/test_digest.py`, `addons/im_livechat/tests/test_im_livechat_calls.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 78; representative identifiers: `res_groups_privilege_live_chat`, `im_livechat_group_user`, `im_livechat_group_manager`, `action_report_livechat_conversation`, `report_livechat_conversation`, `im_livechat_report_channel_view_pivot`, `im_livechat_report_channel_view_list`, `im_livechat_report_channel_view_form`, `im_livechat_report_channel_view_graph`, `im_livechat_report_channel_view_search`, `im_livechat_report_channel_action`, `im_livechat_report_channel_time_to_answer_action`, `Sessions Analysis`, `digest.digest_digest_default`, `digest_tip_im_livechat_0`, `im_livechat_channel_data`, `utm_source_chatbot`, `chatbot_script_welcome_bot`, `chatbot_script_welcome_step_welcome`, `chatbot_script_welcome_step_dispatch`
- Menus: 13; representative evidence: `addons/im_livechat/report/im_livechat_report_channel_views.xml:141`, `addons/im_livechat/views/im_livechat_expertise_views.xml:38`, `addons/im_livechat/views/im_livechat_channel_views.xml:312`, `addons/im_livechat/views/im_livechat_channel_views.xml:319`, `addons/im_livechat/views/im_livechat_channel_views.xml:327`, `addons/im_livechat/views/im_livechat_channel_views.xml:335`, `addons/im_livechat/views/im_livechat_channel_views.xml:342`, `addons/im_livechat/views/im_livechat_channel_views.xml:348`, `addons/im_livechat/views/im_livechat_channel_views.xml:354`, `addons/im_livechat/views/im_livechat_channel_views.xml:362`, `addons/im_livechat/views/im_livechat_channel_member_history_views.xml:39`, `addons/im_livechat/views/im_livechat_channel_member_history_views.xml:142`
- Templates: 7; representative evidence: `addons/im_livechat/report/im_livechat_conversation_report.xml:12`, `addons/im_livechat/data/mail_templates.xml:4`, `addons/im_livechat/views/im_livechat_channel_templates.xml:11`, `addons/im_livechat/views/im_livechat_channel_templates.xml:88`, `addons/im_livechat/views/im_livechat_channel_templates.xml:96`, `addons/im_livechat/views/webclient_templates.xml:3`, `addons/im_livechat/views/im_livechat_chatbot_templates.xml:4`
- View/action field declarations: 221; representative evidence: `addons/im_livechat/report/im_livechat_conversation_report.xml:6`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:7`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:8`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:24`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:25`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:41`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:42`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:49`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:50`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:64`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:65`, `addons/im_livechat/report/im_livechat_report_channel_views.xml:114`
- Browser assets: 185; representative files: `addons/im_livechat/static/tests/visitor_disconnection.test.js`, `addons/im_livechat/static/tests/livechat_channel_info_list.test.js`, `addons/im_livechat/static/tests/messaging_menu_livechat_tab.test.js`, `addons/im_livechat/static/tests/im_livechat_shared_tests.js`, `addons/im_livechat/static/tests/mobile_messaging_menu_patch.test.js`, `addons/im_livechat/static/tests/go_to_oldest_unread_thread.test.js`, `addons/im_livechat/static/tests/translation.test.js`, `addons/im_livechat/static/tests/looking_for_help.test.js`, `addons/im_livechat/static/tests/chat_window_patch.test.js`, `addons/im_livechat/static/tests/call.test.js`, `addons/im_livechat/static/tests/suggestions.test.js`, `addons/im_livechat/static/tests/chat_hub_compact.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/im_livechat/__manifest__.py`
- **HTTP entry points:** `addons/im_livechat/controllers/webclient.py:11`, `addons/im_livechat/controllers/thread.py:8`, `addons/im_livechat/controllers/main.py:20`, `addons/im_livechat/controllers/main.py:38`, `addons/im_livechat/controllers/main.py:49`, `addons/im_livechat/controllers/main.py:53`, `addons/im_livechat/controllers/main.py:57`, `addons/im_livechat/controllers/main.py:64`, `addons/im_livechat/controllers/main.py:69`, `addons/im_livechat/controllers/main.py:204`, `addons/im_livechat/controllers/main.py:211`, `addons/im_livechat/controllers/main.py:219`
- **Scheduled entry points:** `addons/im_livechat/models/discuss_channel.py`, `addons/im_livechat/models/discuss_channel_member.py`
- **Report entry points:** `addons/im_livechat/controllers/main.py`, `addons/im_livechat/report/im_livechat_conversation_report.xml`

## 7. Database interactions

- Model declarations: 23
- Representative model evidence: inherits `res.partner` (addons/im_livechat/models/res_partner.py:12); `im_livechat.expertise` (addons/im_livechat/models/im_livechat_expertise.py:8); `im_livechat.channel` (addons/im_livechat/models/im_livechat_channel.py:17); `im_livechat.channel.rule` (addons/im_livechat/models/im_livechat_channel.py:639); inherits `mail.message` (addons/im_livechat/models/mail_message.py:5); `discuss.channel` (addons/im_livechat/models/discuss_channel.py:32); inherits `digest.digest` (addons/im_livechat/models/digest.py:7); inherits `res.groups` (addons/im_livechat/models/res_groups.py:7); `chatbot.script` (addons/im_livechat/models/chatbot_script.py:14); inherits `discuss.channel.member` (addons/im_livechat/models/discuss_channel_member.py:10); inherits `ir.qweb` (addons/im_livechat/models/ir_qweb.py:5); inherits `ir.websocket` (addons/im_livechat/models/ir_websocket.py:6); `chatbot.message` (addons/im_livechat/models/chatbot_message.py:8); inherits `res.users.settings` (addons/im_livechat/models/res_users_settings.py:8); `chatbot.script.answer` (addons/im_livechat/models/chatbot_script_answer.py:10); inherits `ir.http` (addons/im_livechat/models/ir_http.py:9); inherits `utm.mixin` (addons/im_livechat/models/utm.py:6); inherits `discuss.channel.rtc.session` (addons/im_livechat/models/discuss_channel_rtc_session.py:6); inherits `res.users` (addons/im_livechat/models/res_users.py:12); `chatbot.script.step` (addons/im_livechat/models/chatbot_script_step.py:14); inherits `discuss.call.history` (addons/im_livechat/models/discuss_call_history.py:6); `im_livechat.channel.member.history` (addons/im_livechat/models/im_livechat_channel_member_history.py:7); `im_livechat.report.channel` (addons/im_livechat/report/im_livechat_report_channel.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 20
- Route declarations: 38
- Route evidence: `addons/im_livechat/controllers/webclient.py:11`, `addons/im_livechat/controllers/thread.py:8`, `addons/im_livechat/controllers/main.py:20`, `addons/im_livechat/controllers/main.py:38`, `addons/im_livechat/controllers/main.py:49`, `addons/im_livechat/controllers/main.py:53`, `addons/im_livechat/controllers/main.py:57`, `addons/im_livechat/controllers/main.py:64`, `addons/im_livechat/controllers/main.py:69`, `addons/im_livechat/controllers/main.py:204`, `addons/im_livechat/controllers/main.py:211`, `addons/im_livechat/controllers/main.py:219`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `digest`, `utm`, `phone_validation`
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

- `addons/im_livechat/__init__.py`
- `addons/im_livechat/__manifest__.py`
- `addons/im_livechat/controllers/__init__.py`
- `addons/im_livechat/controllers/attachment.py`
- `addons/im_livechat/controllers/channel.py`
- `addons/im_livechat/controllers/chatbot.py`
- `addons/im_livechat/controllers/cors/__init__.py`
- `addons/im_livechat/controllers/cors/attachment.py`
- `addons/im_livechat/controllers/cors/channel.py`
- `addons/im_livechat/controllers/cors/chatbot.py`
- `addons/im_livechat/controllers/cors/google_translate.py`
- `addons/im_livechat/controllers/cors/link_preview.py`
- `addons/im_livechat/controllers/cors/main.py`
- `addons/im_livechat/controllers/cors/message_reaction.py`
- `addons/im_livechat/controllers/cors/rtc.py`
- `addons/im_livechat/controllers/cors/thread.py`
- `addons/im_livechat/controllers/cors/webclient.py`
- `addons/im_livechat/controllers/main.py`
- `addons/im_livechat/controllers/messaging_menu.py`
- `addons/im_livechat/controllers/rtc.py`
- `addons/im_livechat/controllers/thread.py`
- `addons/im_livechat/controllers/webclient.py`
- `addons/im_livechat/data/digest_data.xml`
- `addons/im_livechat/data/im_livechat_channel_data.xml`
- `addons/im_livechat/data/im_livechat_chatbot_data.xml`
- `addons/im_livechat/data/mail_templates.xml`
- `addons/im_livechat/data/utm_data.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_channel.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_chatbot.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_chatbot_session_1.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_chatbot_session_2.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_chatbot_session_3.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_1.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_10.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_11.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_12.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_13.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_14.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_15.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_2.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_3.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_4.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_5.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_6.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_7.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_8.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_session_9.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_1.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_2.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_3.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_4.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_5.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_6.xml`
- `addons/im_livechat/demo/im_livechat_channel/im_livechat_support_bot_session_7.xml`
- `addons/im_livechat/i18n/af.po`
- `addons/im_livechat/i18n/ar.po`
- `addons/im_livechat/i18n/az.po`
- `addons/im_livechat/i18n/bg.po`
- `addons/im_livechat/i18n/bs.po`
- `addons/im_livechat/i18n/ca.po`
- `addons/im_livechat/i18n/cs.po`
- `addons/im_livechat/i18n/da.po`
- `addons/im_livechat/i18n/de.po`
- `addons/im_livechat/i18n/el.po`
- `addons/im_livechat/i18n/es.po`
- `addons/im_livechat/i18n/es_419.po`
- `addons/im_livechat/i18n/es_CL.po`
- `addons/im_livechat/i18n/et.po`
- `addons/im_livechat/i18n/eu.po`
- `addons/im_livechat/i18n/fa.po`
- `addons/im_livechat/i18n/fi.po`
- `addons/im_livechat/i18n/fo.po`
- `addons/im_livechat/i18n/fr.po`
- `addons/im_livechat/i18n/fr_CA.po`
- `addons/im_livechat/i18n/gl.po`
- `addons/im_livechat/i18n/gu.po`
- `addons/im_livechat/i18n/he.po`
- `addons/im_livechat/i18n/hi.po`
- `addons/im_livechat/i18n/hr.po`
- `addons/im_livechat/i18n/hu.po`
- `addons/im_livechat/i18n/id.po`
- `addons/im_livechat/i18n/im_livechat.pot`
- `addons/im_livechat/i18n/is.po`
- `addons/im_livechat/i18n/it.po`
- `addons/im_livechat/i18n/ja.po`
- `addons/im_livechat/i18n/ka.po`
- `addons/im_livechat/i18n/kab.po`
- `addons/im_livechat/i18n/km.po`
- `addons/im_livechat/i18n/ko.po`
- `addons/im_livechat/i18n/ku.po`
- `addons/im_livechat/i18n/lb.po`
- `addons/im_livechat/i18n/lo.po`
- `addons/im_livechat/i18n/lt.po`
- `addons/im_livechat/i18n/lv.po`
- `addons/im_livechat/i18n/mk.po`
- `addons/im_livechat/i18n/mn.po`
- `addons/im_livechat/i18n/my.po`
- `addons/im_livechat/i18n/nb.po`
- `addons/im_livechat/i18n/nl.po`
- `addons/im_livechat/i18n/pl.po`
- `addons/im_livechat/i18n/pt.po`
- `addons/im_livechat/i18n/pt_BR.po`
- `addons/im_livechat/i18n/ro.po`
- `addons/im_livechat/i18n/ru.po`
- `addons/im_livechat/i18n/sk.po`
- `addons/im_livechat/i18n/sl.po`
- `addons/im_livechat/i18n/sq.po`
- `addons/im_livechat/i18n/sr@latin.po`
- `addons/im_livechat/i18n/sv.po`
- `addons/im_livechat/i18n/ta.po`
- `addons/im_livechat/i18n/th.po`
- `addons/im_livechat/i18n/tr.po`
- `addons/im_livechat/i18n/uk.po`
- `addons/im_livechat/i18n/uz.po`
- `addons/im_livechat/i18n/vi.po`
- `addons/im_livechat/i18n/zh_CN.po`
- `addons/im_livechat/i18n/zh_TW.po`
- `addons/im_livechat/models/__init__.py`
- `addons/im_livechat/models/chatbot_message.py`
- `addons/im_livechat/models/chatbot_script.py`
- `addons/im_livechat/models/chatbot_script_answer.py`
- `addons/im_livechat/models/chatbot_script_step.py`
- `addons/im_livechat/models/digest.py`
- `addons/im_livechat/models/discuss_call_history.py`
- `addons/im_livechat/models/discuss_channel.py`
- `addons/im_livechat/models/discuss_channel_member.py`
- `addons/im_livechat/models/discuss_channel_rtc_session.py`
- `addons/im_livechat/models/im_livechat_channel.py`
- `addons/im_livechat/models/im_livechat_channel_member_history.py`
- `addons/im_livechat/models/im_livechat_expertise.py`
- `addons/im_livechat/models/ir_http.py`
- `addons/im_livechat/models/ir_qweb.py`
- `addons/im_livechat/models/ir_websocket.py`
- `addons/im_livechat/models/mail_message.py`
- `addons/im_livechat/models/res_groups.py`
- `addons/im_livechat/models/res_partner.py`
- `addons/im_livechat/models/res_users.py`
- `addons/im_livechat/models/res_users_settings.py`
- `addons/im_livechat/models/utm.py`
- `addons/im_livechat/report/__init__.py`
- `addons/im_livechat/report/im_livechat_conversation_report.xml`
- `addons/im_livechat/report/im_livechat_report_channel.py`
- `addons/im_livechat/report/im_livechat_report_channel_views.xml`
- `addons/im_livechat/security/im_livechat_channel_security.xml`
- `addons/im_livechat/security/ir.access.csv`
- `addons/im_livechat/static/description/icon.png`
- `addons/im_livechat/static/description/icon.svg`
- `addons/im_livechat/static/description/icon_hi.png`
- `addons/im_livechat/static/src/core/common/@types/models.d.ts`
- `addons/im_livechat/static/src/core/common/channel_member_list_patch.js`
- `addons/im_livechat/static/src/core/common/chat_window_model_patch.js`
- `addons/im_livechat/static/src/core/common/chat_window_patch.js`
- `addons/im_livechat/static/src/core/common/chat_window_patch.xml`
- `addons/im_livechat/static/src/core/common/chatbot_message_model.js`
- `addons/im_livechat/static/src/core/common/chatbot_model.js`
- `addons/im_livechat/static/src/core/common/chatbot_script_model.js`
- `addons/im_livechat/static/src/core/common/chatbot_script_step_answer_model.js`
- `addons/im_livechat/static/src/core/common/chatbot_script_step_model.js`
- `addons/im_livechat/static/src/core/common/chatbot_step_model.js`
- `addons/im_livechat/static/src/core/common/close_confirmation.js`
- `addons/im_livechat/static/src/core/common/close_confirmation.scss`
- `addons/im_livechat/static/src/core/common/close_confirmation.xml`
- `addons/im_livechat/static/src/core/common/data_response_model_patch.js`
- `addons/im_livechat/static/src/core/common/discuss_channel_member_model_patch.js`
- `addons/im_livechat/static/src/core/common/discuss_channel_model_patch.js`
- `addons/im_livechat/static/src/core/common/expirable_storage.js`
- `addons/im_livechat/static/src/core/common/livechat_channel_member_history_model.js`
- `addons/im_livechat/static/src/core/common/livechat_channel_model.js`
- `addons/im_livechat/static/src/core/common/livechat_channel_model_patch.js`
- `addons/im_livechat/static/src/core/common/livechat_channel_rule_model.js`
- `addons/im_livechat/static/src/core/common/livechat_command_dialog.js`
- `addons/im_livechat/static/src/core/common/livechat_command_dialog.scss`
- `addons/im_livechat/static/src/core/common/livechat_command_dialog.xml`
- `addons/im_livechat/static/src/core/common/livechat_expertise_model.js`
- `addons/im_livechat/static/src/core/common/message_model_patch.js`
- `addons/im_livechat/static/src/core/common/misc.js`
- `addons/im_livechat/static/src/core/common/res_partner_model_patch.js`
- `addons/im_livechat/static/src/core/common/res_users_model_patch.js`
- `addons/im_livechat/static/src/core/common/res_users_settings_model_patch.js`
- `addons/im_livechat/static/src/core/common/store_service_patch.js`
- `addons/im_livechat/static/src/core/common/suggestion_service_patch.js`
- `addons/im_livechat/static/src/core/common/thread_actions_patch.js`
- `addons/im_livechat/static/src/core/common/thread_model_patch.js`
- `addons/im_livechat/static/src/core/common/thread_patch.js`
- `addons/im_livechat/static/src/core/common/thread_patch.xml`
- `addons/im_livechat/static/src/core/common/transcript_sender.js`
- `addons/im_livechat/static/src/core/common/transcript_sender.scss`
- `addons/im_livechat/static/src/core/common/transcript_sender.xml`
- `addons/im_livechat/static/src/core/public_web/@types/menu_tabs.d.ts`
- `addons/im_livechat/static/src/core/public_web/@types/models.d.ts`
- `addons/im_livechat/static/src/core/public_web/discuss_app/@types/models.d.ts`
- `addons/im_livechat/static/src/core/public_web/discuss_app/discuss_app_model_patch.js`
- `addons/im_livechat/static/src/core/public_web/discuss_channel_model_patch.js`
- `addons/im_livechat/static/src/core/public_web/livechat_leave_dialog.js`
- `addons/im_livechat/static/src/core/public_web/livechat_leave_dialog.xml`
- `addons/im_livechat/static/src/core/public_web/livechat_rating_notification_message.xml`
- `addons/im_livechat/static/src/core/public_web/livechat_rating_notification_service.js`
- `addons/im_livechat/static/src/core/public_web/message.scss`
- `addons/im_livechat/static/src/core/public_web/messaging_menu_item_patch.js`
- `addons/im_livechat/static/src/core/public_web/messaging_menu_item_patch.xml`
- `addons/im_livechat/static/src/core/public_web/messaging_menu_model_patch.js`
- `addons/im_livechat/static/src/core/public_web/messaging_menu_patch.js`
- `addons/im_livechat/static/src/core/public_web/thread_compare_patch.js`
- `addons/im_livechat/static/src/core/public_web/upgrade_19_1.js`
- `addons/im_livechat/static/src/core/public_web/upgrade_19_2.js`
- `addons/im_livechat/static/src/core/web/@types/models.d.ts`
- `addons/im_livechat/static/src/core/web/channel_commands_patch.js`
- `addons/im_livechat/static/src/core/web/channel_invitation_patch.scss`
- `addons/im_livechat/static/src/core/web/channel_invitation_patch.xml`
- `addons/im_livechat/static/src/core/web/channel_member_patch.js`
- `addons/im_livechat/static/src/core/web/channel_member_patch.xml`
- `addons/im_livechat/static/src/core/web/chat_bubble_patch.xml`
- `addons/im_livechat/static/src/core/web/chat_window_patch.xml`
- `addons/im_livechat/static/src/core/web/command_palette.xml`
- `addons/im_livechat/static/src/core/web/composer_patch.js`
- `addons/im_livechat/static/src/core/web/discuss_app/client_action_patch.js`
- `addons/im_livechat/static/src/core/web/discuss_command_patch.js`
- `addons/im_livechat/static/src/core/web/discuss_content_patch.js`
- `addons/im_livechat/static/src/core/web/expertise_tags_autocomplete.js`
- `addons/im_livechat/static/src/core/web/expertise_tags_autocomplete.xml`
- `addons/im_livechat/static/src/core/web/livechat_channel_command_provider.js`
- `addons/im_livechat/static/src/core/web/livechat_channel_info_list.dark.scss`
- `addons/im_livechat/static/src/core/web/livechat_channel_info_list.js`
- `addons/im_livechat/static/src/core/web/livechat_channel_info_list.scss`
- `addons/im_livechat/static/src/core/web/livechat_channel_info_list.xml`
- `addons/im_livechat/static/src/core/web/livechat_channel_model_patch.js`
- `addons/im_livechat/static/src/core/web/livechat_status.xml`
- `addons/im_livechat/static/src/core/web/notification_item.dark.scss`
- `addons/im_livechat/static/src/core/web/notification_item.scss`
- `addons/im_livechat/static/src/core/web/notification_item_patch.js`
- `addons/im_livechat/static/src/core/web/notification_item_patch.xml`
- `addons/im_livechat/static/src/core/web/partner_compare.js`
- `addons/im_livechat/static/src/core/web/store_service_patch.js`
- `addons/im_livechat/static/src/core/web/suggestion_service_patch.js`
- `addons/im_livechat/static/src/core/web/thread_actions.js`
- `addons/im_livechat/static/src/core/web/thread_icon_patch.js`
- `addons/im_livechat/static/src/core/web/thread_model_patch.js`
- `addons/im_livechat/static/src/embed/common/@types/models.d.ts`
- `addons/im_livechat/static/src/embed/common/attachment_model_patch.js`
- `addons/im_livechat/static/src/embed/common/attachment_upload_service_patch.js`
- `addons/im_livechat/static/src/embed/common/autopopup_service.js`
- `addons/im_livechat/static/src/embed/common/boot_helpers.js`
- `addons/im_livechat/static/src/embed/common/chat_hub_patch.js`
- `addons/im_livechat/static/src/embed/common/chat_hub_patch.xml`
- `addons/im_livechat/static/src/embed/common/chat_window_model_patch.js`
- `addons/im_livechat/static/src/embed/common/chat_window_patch.js`
- `addons/im_livechat/static/src/embed/common/chat_window_patch.scss`
- `addons/im_livechat/static/src/embed/common/chat_window_patch.xml`
- `addons/im_livechat/static/src/embed/common/composer.scss`
- Additional source files not expanded in this page: 173; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
