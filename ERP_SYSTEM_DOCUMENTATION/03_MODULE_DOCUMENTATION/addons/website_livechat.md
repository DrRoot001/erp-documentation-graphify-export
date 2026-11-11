# Module: website_livechat

- **Module ID:** MOD-623
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_livechat`
- **Manifest:** `addons/website_livechat/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Live Chat`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Chat with your website visitors

**Manifest description:**

Allow website visitors to chat with the collaborators.

**Scope evidence:** The module contains 136 files, including 28 Python, 9 XML, and 37 JavaScript/TypeScript files. The manifest declares dependencies: `website`, `im_livechat`.

## 2. Module structure

- Model/business logic files: 9
- Controller/API files: 5
- XML/data/view/template files: 9
- Browser asset files: 37
- Security files: 1
- Test files: 11
- Scheduled/automation evidence files: 1
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_livechat/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 9 model declarations, 85 methods, 0 constraint handlers, 0 onchange handlers, and 2 dependency declarations.
- **Evidence:** `addons/website_livechat/models/im_livechat_channel.py:6`, `addons/website_livechat/models/discuss_channel.py:9`, `addons/website_livechat/models/chatbot_script.py:7`, `addons/website_livechat/models/discuss_channel_member.py:6`, `addons/website_livechat/models/res_config_settings.py:7`, `addons/website_livechat/models/website_visitor.py:11`, `addons/website_livechat/models/ir_http.py:7`, `addons/website_livechat/models/chatbot_script_step.py:7`, `addons/website_livechat/models/website.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 5 controller files and 2 route declarations.
- **Evidence:** `addons/website_livechat/controllers/chatbot.py:11`, `addons/website_livechat/controllers/website.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 9 XML files and 37 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/website_livechat/demo/im_livechat_session_11.xml:4`, `addons/website_livechat/demo/im_livechat_session_11.xml:9`, `addons/website_livechat/data/website_livechat_chatbot_demo.xml:6`, `addons/website_livechat/data/website_livechat_data.xml:10`, `addons/website_livechat/views/website_livechat.xml:8`, `addons/website_livechat/views/website_visitor_views.xml:3`, `addons/website_livechat/views/website_visitor_views.xml:15`, `addons/website_livechat/views/website_visitor_views.xml:22`, `addons/website_livechat/views/website_visitor_views.xml:30`, `addons/website_livechat/views/website_visitor_views.xml:65`, `addons/website_livechat/views/website_visitor_views.xml:88`, `addons/website_livechat/views/website_visitor_views.xml:102`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_livechat/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 1 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/website_livechat/views/website_visitor_views.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 11 test files are present.
- **Evidence:** `addons/website_livechat/tests/test_fw_operator.py`, `addons/website_livechat/tests/test_livechat_basic_flow.py`, `addons/website_livechat/tests/test_website_visitor.py`, `addons/website_livechat/tests/test_livechat_request.py`, `addons/website_livechat/tests/common.py`, `addons/website_livechat/tests/test_lazy_frontend_bus.py`, `addons/website_livechat/tests/test_ui.py`, `addons/website_livechat/tests/test_chatbot_ui.py`, `addons/website_livechat/tests/test_cors_livechat.py`, `addons/website_livechat/tests/__init__.py`, `addons/website_livechat/tests/test_livechat_session_user_changes.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 9; representative identifiers: `website_livechat_visitor_11_demo`, `im_livechat.livechat_channel_session_11`, `website_livechat_channel_rule_chatbot`, `base.default_website`, `Livechat : include loader on Website`, `website_visitor_livechat_session_action`, `website_visitor_livechat_session_action_tree`, `website_visitor_livechat_session_action_form`, `website_visitor_view_kanban`, `website_visitor_view_form`, `website_visitor_view_tree`, `website_visitor_view_search`, `website_livechat_send_chat_request_action_server`, `Visitors`, `chatbot_script_view_form`, `res_config_settings_view_form`, `im_livechat_channel_view_form_add`, `im_livechat_channel_action_add`
- Menus: 1; representative evidence: `addons/website_livechat/views/website_visitor_views.xml:127`
- Templates: 1; representative evidence: `addons/website_livechat/views/website_livechat.xml:8`
- View/action field declarations: 20; representative evidence: `addons/website_livechat/views/website_visitor_views.xml:5`, `addons/website_livechat/views/website_visitor_views.xml:6`, `addons/website_livechat/views/website_visitor_views.xml:17`, `addons/website_livechat/views/website_visitor_views.xml:24`, `addons/website_livechat/views/website_visitor_views.xml:32`, `addons/website_livechat/views/website_visitor_views.xml:34`, `addons/website_livechat/views/website_visitor_views.xml:67`, `addons/website_livechat/views/website_visitor_views.xml:69`, `addons/website_livechat/views/website_visitor_views.xml:90`, `addons/website_livechat/views/website_visitor_views.xml:92`, `addons/website_livechat/views/website_visitor_views.xml:104`, `addons/website_livechat/views/website_visitor_views.xml:106`
- Browser assets: 37; representative files: `addons/website_livechat/static/tests/website_livechat_test_helpers.js`, `addons/website_livechat/static/tests/thread_patch.test.js`, `addons/website_livechat/static/tests/discuss_content_patch.test.js`, `addons/website_livechat/static/tests/messaging_service_patch.test.js`, `addons/website_livechat/static/tests/livechat_channel_info_list_patch.test.js`, `addons/website_livechat/static/src/js/systray_items/new_content.js`, `addons/website_livechat/static/src/core/web/website_visitor_model_patch.js`, `addons/website_livechat/static/src/core/web/livechat_channel_info_list_patch.js`, `addons/website_livechat/static/src/core/web/channel_member_model_patch.js`, `addons/website_livechat/static/src/core/common/thread_model_patch.js`, `addons/website_livechat/static/src/core/common/website_visitor_model_patch.js`, `addons/website_livechat/static/src/core/common/discuss_channel_model_patch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_livechat/__manifest__.py`
- **HTTP entry points:** `addons/website_livechat/controllers/chatbot.py:11`, `addons/website_livechat/controllers/website.py:9`
- **Scheduled entry points:** `addons/website_livechat/views/website_visitor_views.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 9
- Representative model evidence: inherits `im_livechat.channel` (addons/website_livechat/models/im_livechat_channel.py:6); inherits `discuss.channel` (addons/website_livechat/models/discuss_channel.py:9); inherits `chatbot.script` (addons/website_livechat/models/chatbot_script.py:7); inherits `discuss.channel.member` (addons/website_livechat/models/discuss_channel_member.py:6); inherits `res.config.settings` (addons/website_livechat/models/res_config_settings.py:7); inherits `website.visitor` (addons/website_livechat/models/website_visitor.py:11); inherits `ir.http` (addons/website_livechat/models/ir_http.py:7); inherits `chatbot.script.step` (addons/website_livechat/models/chatbot_script_step.py:7); inherits `website` (addons/website_livechat/models/website.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 5
- Route declarations: 2
- Route evidence: `addons/website_livechat/controllers/chatbot.py:11`, `addons/website_livechat/controllers/website.py:9`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website`, `im_livechat`
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

- `addons/website_livechat/__init__.py`
- `addons/website_livechat/__manifest__.py`
- `addons/website_livechat/controllers/__init__.py`
- `addons/website_livechat/controllers/chatbot.py`
- `addons/website_livechat/controllers/main.py`
- `addons/website_livechat/controllers/webclient.py`
- `addons/website_livechat/controllers/website.py`
- `addons/website_livechat/data/website_livechat_chatbot_demo.xml`
- `addons/website_livechat/data/website_livechat_data.xml`
- `addons/website_livechat/demo/im_livechat_session_11.xml`
- `addons/website_livechat/i18n/af.po`
- `addons/website_livechat/i18n/ar.po`
- `addons/website_livechat/i18n/az.po`
- `addons/website_livechat/i18n/bg.po`
- `addons/website_livechat/i18n/bs.po`
- `addons/website_livechat/i18n/ca.po`
- `addons/website_livechat/i18n/cs.po`
- `addons/website_livechat/i18n/da.po`
- `addons/website_livechat/i18n/de.po`
- `addons/website_livechat/i18n/el.po`
- `addons/website_livechat/i18n/es.po`
- `addons/website_livechat/i18n/es_419.po`
- `addons/website_livechat/i18n/et.po`
- `addons/website_livechat/i18n/fa.po`
- `addons/website_livechat/i18n/fi.po`
- `addons/website_livechat/i18n/fr.po`
- `addons/website_livechat/i18n/fr_BE.po`
- `addons/website_livechat/i18n/gl.po`
- `addons/website_livechat/i18n/gu.po`
- `addons/website_livechat/i18n/he.po`
- `addons/website_livechat/i18n/hi.po`
- `addons/website_livechat/i18n/hr.po`
- `addons/website_livechat/i18n/hu.po`
- `addons/website_livechat/i18n/id.po`
- `addons/website_livechat/i18n/is.po`
- `addons/website_livechat/i18n/it.po`
- `addons/website_livechat/i18n/ja.po`
- `addons/website_livechat/i18n/kab.po`
- `addons/website_livechat/i18n/km.po`
- `addons/website_livechat/i18n/ko.po`
- `addons/website_livechat/i18n/ku.po`
- `addons/website_livechat/i18n/lo.po`
- `addons/website_livechat/i18n/lt.po`
- `addons/website_livechat/i18n/lv.po`
- `addons/website_livechat/i18n/mk.po`
- `addons/website_livechat/i18n/mn.po`
- `addons/website_livechat/i18n/my.po`
- `addons/website_livechat/i18n/nb.po`
- `addons/website_livechat/i18n/nl.po`
- `addons/website_livechat/i18n/pl.po`
- `addons/website_livechat/i18n/pt.po`
- `addons/website_livechat/i18n/pt_BR.po`
- `addons/website_livechat/i18n/ro.po`
- `addons/website_livechat/i18n/ru.po`
- `addons/website_livechat/i18n/sk.po`
- `addons/website_livechat/i18n/sl.po`
- `addons/website_livechat/i18n/sr@latin.po`
- `addons/website_livechat/i18n/sv.po`
- `addons/website_livechat/i18n/ta.po`
- `addons/website_livechat/i18n/th.po`
- `addons/website_livechat/i18n/tr.po`
- `addons/website_livechat/i18n/uk.po`
- `addons/website_livechat/i18n/uz.po`
- `addons/website_livechat/i18n/vi.po`
- `addons/website_livechat/i18n/website_livechat.pot`
- `addons/website_livechat/i18n/zh_CN.po`
- `addons/website_livechat/i18n/zh_TW.po`
- `addons/website_livechat/models/__init__.py`
- `addons/website_livechat/models/chatbot_script.py`
- `addons/website_livechat/models/chatbot_script_step.py`
- `addons/website_livechat/models/discuss_channel.py`
- `addons/website_livechat/models/discuss_channel_member.py`
- `addons/website_livechat/models/im_livechat_channel.py`
- `addons/website_livechat/models/ir_http.py`
- `addons/website_livechat/models/res_config_settings.py`
- `addons/website_livechat/models/website.py`
- `addons/website_livechat/models/website_visitor.py`
- `addons/website_livechat/security/ir.access.csv`
- `addons/website_livechat/static/description/icon.png`
- `addons/website_livechat/static/description/icon.svg`
- `addons/website_livechat/static/description/icon_hi.png`
- `addons/website_livechat/static/src/core/common/@types/models.d.ts`
- `addons/website_livechat/static/src/core/common/discuss_channel_model_patch.js`
- `addons/website_livechat/static/src/core/common/thread_model_patch.js`
- `addons/website_livechat/static/src/core/common/website_livechat_edit_mode.scss`
- `addons/website_livechat/static/src/core/common/website_visitor_model_patch.js`
- `addons/website_livechat/static/src/core/web/@types/models.d.ts`
- `addons/website_livechat/static/src/core/web/channel_member_model_patch.js`
- `addons/website_livechat/static/src/core/web/livechat_channel_info_list_patch.js`
- `addons/website_livechat/static/src/core/web/livechat_channel_info_list_patch.xml`
- `addons/website_livechat/static/src/core/web/website_visitor_model_patch.js`
- `addons/website_livechat/static/src/js/systray_items/new_content.js`
- `addons/website_livechat/static/tests/discuss_content_patch.test.js`
- `addons/website_livechat/static/tests/livechat_channel_info_list_patch.test.js`
- `addons/website_livechat/static/tests/messaging_service_patch.test.js`
- `addons/website_livechat/static/tests/mock_server/mock_models/discuss_channel.js`
- `addons/website_livechat/static/tests/mock_server/mock_models/website_visitor.js`
- `addons/website_livechat/static/tests/thread_patch.test.js`
- `addons/website_livechat/static/tests/tours/lazy_frontend_bus_tour.js`
- `addons/website_livechat/static/tests/tours/website_livechat_as_portal.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_after_reload.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_continue.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_continue_after_login.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_flow.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_forward.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_fw_operator_matching_lang.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_redirect.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_restart.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_stops_when_agent_joins_tour.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_test_page_tour.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_trigger_selection_tour.js`
- `addons/website_livechat/static/tests/tours/website_livechat_chatbot_user_input_tour.js`
- `addons/website_livechat/static/tests/tours/website_livechat_common.js`
- `addons/website_livechat/static/tests/tours/website_livechat_no_new_session_with_hide_rule.js`
- `addons/website_livechat/static/tests/tours/website_livechat_question_selection_overlapping_answers.js`
- `addons/website_livechat/static/tests/tours/website_livechat_rating.js`
- `addons/website_livechat/static/tests/tours/website_livechat_request.js`
- `addons/website_livechat/static/tests/tours/website_livechat_session_user_changes.js`
- `addons/website_livechat/static/tests/tours/website_livechat_user_known_after_reload.js`
- `addons/website_livechat/static/tests/website_livechat_test_helpers.js`
- `addons/website_livechat/tests/__init__.py`
- `addons/website_livechat/tests/common.py`
- `addons/website_livechat/tests/test_chatbot_ui.py`
- `addons/website_livechat/tests/test_cors_livechat.py`
- `addons/website_livechat/tests/test_fw_operator.py`
- `addons/website_livechat/tests/test_lazy_frontend_bus.py`
- `addons/website_livechat/tests/test_livechat_basic_flow.py`
- `addons/website_livechat/tests/test_livechat_request.py`
- `addons/website_livechat/tests/test_livechat_session_user_changes.py`
- `addons/website_livechat/tests/test_ui.py`
- `addons/website_livechat/tests/test_website_visitor.py`
- `addons/website_livechat/views/im_livechat_channel_add.xml`
- `addons/website_livechat/views/im_livechat_chatbot_script_view.xml`
- `addons/website_livechat/views/res_config_settings_views.xml`
- `addons/website_livechat/views/website_livechat.xml`
- `addons/website_livechat/views/website_visitor_views.xml`
