# Module: crm_livechat

- **Module ID:** MOD-057
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/crm_livechat`
- **Manifest:** `addons/crm_livechat/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Create lead from livechat conversation

**Manifest description:**

Create new lead with using /lead command in the channel

**Scope evidence:** The module contains 85 files, including 15 Python, 6 XML, and 14 JavaScript/TypeScript files. The manifest declares dependencies: `crm`, `im_livechat`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 14
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/crm_livechat/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 29 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/crm_livechat/models/discuss_channel.py:9`, `addons/crm_livechat/models/chatbot_script.py:7`, `addons/crm_livechat/models/res_users.py:5`, `addons/crm_livechat/models/crm_lead.py:7`, `addons/crm_livechat/models/chatbot_script_step.py:7`, `addons/crm_livechat/report/im_livechat_report_channel.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 14 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:10`, `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:15`, `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:22`, `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:28`, `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:35`, `addons/crm_livechat/data/crm_livechat_chatbot_data.xml:42`, `addons/crm_livechat/views/discuss_channel_views.xml:4`, `addons/crm_livechat/views/crm_lead_views.xml:3`, `addons/crm_livechat/views/chatbot_script_views.xml:4`, `addons/crm_livechat/views/chatbot_script_step_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/crm_livechat/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/crm_livechat/tests/test_chatbot_lead.py`, `addons/crm_livechat/tests/test_discuss_channel_access.py`, `addons/crm_livechat/tests/chatbot_common.py`, `addons/crm_livechat/tests/test_crm_lead.py`, `addons/crm_livechat/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `chatbot_script_lead_generation_bot`, `chatbot_script_lead_generation_step_welcome`, `chatbot_script_lead_generation_step_forward_operator`, `chatbot_script_lead_generation_step_noone_available`, `chatbot_script_welcome_step_pricing_email`, `chatbot_script_welcome_step_just_looking`, `discuss_channel_view_form`, `crm_lead_view_form`, `chatbot_script_view_form`, `chatbot_script_step_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/crm_livechat/views/discuss_channel_views.xml:6`, `addons/crm_livechat/views/discuss_channel_views.xml:8`, `addons/crm_livechat/views/crm_lead_views.xml:5`, `addons/crm_livechat/views/crm_lead_views.xml:7`, `addons/crm_livechat/views/chatbot_script_views.xml:6`, `addons/crm_livechat/views/chatbot_script_views.xml:8`, `addons/crm_livechat/views/chatbot_script_step_views.xml:6`, `addons/crm_livechat/views/chatbot_script_step_views.xml:8`
- Browser assets: 14; representative files: `addons/crm_livechat/static/tests/create_lead.test.js`, `addons/crm_livechat/static/tests/crm_livechat_test_helpers.js`, `addons/crm_livechat/static/tests/composer.test.js`, `addons/crm_livechat/static/tests/message.test.js`, `addons/crm_livechat/static/tests/livechat_channel_info_list_patch.test.js`, `addons/crm_livechat/static/src/core/thread_actions.js`, `addons/crm_livechat/static/src/core/thread_action_patch.js`, `addons/crm_livechat/static/src/core/channel_commands.js`, `addons/crm_livechat/static/src/core/common/store_service_patch.js`, `addons/crm_livechat/static/src/core/common/message_model_patch.js`, `addons/crm_livechat/static/src/core/common/@types/models.d.ts`, `addons/crm_livechat/static/tests/mock_server/mock_models/res_users.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/crm_livechat/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `discuss.channel` (addons/crm_livechat/models/discuss_channel.py:9); inherits `chatbot.script` (addons/crm_livechat/models/chatbot_script.py:7); inherits `res.users` (addons/crm_livechat/models/res_users.py:5); inherits `crm.lead` (addons/crm_livechat/models/crm_lead.py:7); inherits `chatbot.script.step` (addons/crm_livechat/models/chatbot_script_step.py:7); inherits `im_livechat.report.channel` (addons/crm_livechat/report/im_livechat_report_channel.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `crm`, `im_livechat`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/crm_livechat/__init__.py`
- `addons/crm_livechat/__manifest__.py`
- `addons/crm_livechat/data/crm_livechat_chatbot_data.xml`
- `addons/crm_livechat/i18n/ar.po`
- `addons/crm_livechat/i18n/az.po`
- `addons/crm_livechat/i18n/bg.po`
- `addons/crm_livechat/i18n/bs.po`
- `addons/crm_livechat/i18n/ca.po`
- `addons/crm_livechat/i18n/crm_livechat.pot`
- `addons/crm_livechat/i18n/cs.po`
- `addons/crm_livechat/i18n/da.po`
- `addons/crm_livechat/i18n/de.po`
- `addons/crm_livechat/i18n/el.po`
- `addons/crm_livechat/i18n/es.po`
- `addons/crm_livechat/i18n/es_419.po`
- `addons/crm_livechat/i18n/et.po`
- `addons/crm_livechat/i18n/fa.po`
- `addons/crm_livechat/i18n/fi.po`
- `addons/crm_livechat/i18n/fr.po`
- `addons/crm_livechat/i18n/he.po`
- `addons/crm_livechat/i18n/hi.po`
- `addons/crm_livechat/i18n/hr.po`
- `addons/crm_livechat/i18n/hu.po`
- `addons/crm_livechat/i18n/id.po`
- `addons/crm_livechat/i18n/it.po`
- `addons/crm_livechat/i18n/ja.po`
- `addons/crm_livechat/i18n/kab.po`
- `addons/crm_livechat/i18n/ko.po`
- `addons/crm_livechat/i18n/ku.po`
- `addons/crm_livechat/i18n/lo.po`
- `addons/crm_livechat/i18n/lt.po`
- `addons/crm_livechat/i18n/lv.po`
- `addons/crm_livechat/i18n/mn.po`
- `addons/crm_livechat/i18n/my.po`
- `addons/crm_livechat/i18n/nb.po`
- `addons/crm_livechat/i18n/nl.po`
- `addons/crm_livechat/i18n/pl.po`
- `addons/crm_livechat/i18n/pt.po`
- `addons/crm_livechat/i18n/pt_BR.po`
- `addons/crm_livechat/i18n/ro.po`
- `addons/crm_livechat/i18n/ru.po`
- `addons/crm_livechat/i18n/sk.po`
- `addons/crm_livechat/i18n/sl.po`
- `addons/crm_livechat/i18n/sr@latin.po`
- `addons/crm_livechat/i18n/sv.po`
- `addons/crm_livechat/i18n/th.po`
- `addons/crm_livechat/i18n/tr.po`
- `addons/crm_livechat/i18n/uk.po`
- `addons/crm_livechat/i18n/uz.po`
- `addons/crm_livechat/i18n/vi.po`
- `addons/crm_livechat/i18n/zh_CN.po`
- `addons/crm_livechat/i18n/zh_TW.po`
- `addons/crm_livechat/models/__init__.py`
- `addons/crm_livechat/models/chatbot_script.py`
- `addons/crm_livechat/models/chatbot_script_step.py`
- `addons/crm_livechat/models/crm_lead.py`
- `addons/crm_livechat/models/discuss_channel.py`
- `addons/crm_livechat/models/res_users.py`
- `addons/crm_livechat/report/__init__.py`
- `addons/crm_livechat/report/im_livechat_report_channel.py`
- `addons/crm_livechat/security/ir.access.csv`
- `addons/crm_livechat/static/src/core/channel_commands.js`
- `addons/crm_livechat/static/src/core/common/@types/models.d.ts`
- `addons/crm_livechat/static/src/core/common/message_model_patch.js`
- `addons/crm_livechat/static/src/core/common/store_service_patch.js`
- `addons/crm_livechat/static/src/core/thread_action_patch.js`
- `addons/crm_livechat/static/src/core/thread_actions.js`
- `addons/crm_livechat/static/src/core/web/livechat_channel_info_list_patch.xml`
- `addons/crm_livechat/static/tests/composer.test.js`
- `addons/crm_livechat/static/tests/create_lead.test.js`
- `addons/crm_livechat/static/tests/crm_livechat_test_helpers.js`
- `addons/crm_livechat/static/tests/livechat_channel_info_list_patch.test.js`
- `addons/crm_livechat/static/tests/message.test.js`
- `addons/crm_livechat/static/tests/mock_server/mock_models/discuss_channel.js`
- `addons/crm_livechat/static/tests/mock_server/mock_models/res_users.js`
- `addons/crm_livechat/static/tests/tours/support/crm_livechat_create_lead_from_chatbot.js`
- `addons/crm_livechat/tests/__init__.py`
- `addons/crm_livechat/tests/chatbot_common.py`
- `addons/crm_livechat/tests/test_chatbot_lead.py`
- `addons/crm_livechat/tests/test_crm_lead.py`
- `addons/crm_livechat/tests/test_discuss_channel_access.py`
- `addons/crm_livechat/views/chatbot_script_step_views.xml`
- `addons/crm_livechat/views/chatbot_script_views.xml`
- `addons/crm_livechat/views/crm_lead_views.xml`
- `addons/crm_livechat/views/discuss_channel_views.xml`
