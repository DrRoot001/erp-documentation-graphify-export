# Module: portal

- **Module ID:** MOD-419
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/portal`
- **Manifest:** `addons/portal/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Customer Portal

**Manifest description:**

This module adds required base code for a fully integrated customer portal.
It contains the base controller class and base templates. Business addons
will add their specific templates and controllers to extend the customer
portal.

This module contains most code coming from odoo v10 website_portal. Purpose
of this module is to allow the display of a customer portal without having
a dependency towards website editing and customization capabilities.

**Scope evidence:** The module contains 142 files, including 32 Python, 14 XML, and 33 JavaScript/TypeScript files. The manifest declares dependencies: `auth_signup`, `base_address_extended`, `html_editor`, `http_routing`, `mail`, `web`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 6
- XML/data/view/template files: 14
- Browser asset files: 33
- Security files: 1
- Test files: 8
- Scheduled/automation evidence files: 2
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/portal/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 164 methods, 0 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/portal/models/res_partner.py:7`, `addons/portal/models/mail_message.py:8`, `addons/portal/models/ir_ui_view.py:7`, `addons/portal/models/portal_mixin.py:9`, `addons/portal/models/res_config_settings.py:7`, `addons/portal/models/ir_qweb.py:8`, `addons/portal/models/portal_entry.py:4`, `addons/portal/models/ir_http.py:7`, `addons/portal/models/res_country.py:7`, `addons/portal/models/mail_thread.py:10`, `addons/portal/models/res_users_apikeys_description.py:8`, `addons/portal/wizard/portal_wizard.py:16`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 6 controller files and 16 route declarations.
- **Evidence:** `addons/portal/controllers/portal.py:203`, `addons/portal/controllers/portal.py:229`, `addons/portal/controllers/portal.py:235`, `addons/portal/controllers/portal.py:264`, `addons/portal/controllers/portal.py:326`, `addons/portal/controllers/portal.py:485`, `addons/portal/controllers/portal.py:515`, `addons/portal/controllers/portal.py:933`, `addons/portal/controllers/portal.py:968`, `addons/portal/controllers/portal.py:987`, `addons/portal/controllers/portal.py:1000`, `addons/portal/controllers/portal.py:1043`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 33 JavaScript/TypeScript files; static XML analysis found 45 record/template/menu identifiers.
- **Evidence:** `addons/portal/wizard/portal_wizard_views.xml:4`, `addons/portal/wizard/portal_wizard_views.xml:12`, `addons/portal/wizard/portal_wizard_views.xml:21`, `addons/portal/wizard/portal_share_views.xml:3`, `addons/portal/wizard/portal_share_views.xml:24`, `addons/portal/data/portal_entry_data.xml:3`, `addons/portal/data/portal_entry_data.xml:11`, `addons/portal/data/mail_templates.xml:4`, `addons/portal/views/res_config_settings_views.xml:5`, `addons/portal/views/portal_templates.xml:3`, `addons/portal/views/portal_templates.xml:81`, `addons/portal/views/portal_templates.xml:92`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/portal/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/portal/wizard/portal_wizard_views.xml`, `addons/portal/tests/test_portal.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/portal/controllers/portal.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 8 test files are present.
- **Evidence:** `addons/portal/tests/test_login.py`, `addons/portal/tests/test_message_format_portal.py`, `addons/portal/tests/test_portal_wizard.py`, `addons/portal/tests/test_portal.py`, `addons/portal/tests/test_pager.py`, `addons/portal/tests/test_addresses.py`, `addons/portal/tests/test_tours.py`, `addons/portal/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `partner_wizard_action_create_and_open`, `partner_wizard_action`, `wizard_view`, `portal_share_wizard`, `portal_share_action`, `portal_entry_addresses`, `portal_entry_base`, `portal_share_template`, `res_config_settings_view_form`, `Main Frontend Layout`, `Footer Language Selector`, `Language Selector`, `Portal User Dropdown`, `Portal Breadcrumbs`, `Back to edit mode`, `Portal Layout`, `User Sign In Placeholder`, `User Sign In`, `User Sign In redirect`, `My Portal`
- Menus: 0; representative evidence: Not found in module
- Templates: 37; representative evidence: `addons/portal/data/mail_templates.xml:4`, `addons/portal/views/portal_templates.xml:3`, `addons/portal/views/portal_templates.xml:81`, `addons/portal/views/portal_templates.xml:92`, `addons/portal/views/portal_templates.xml:116`, `addons/portal/views/portal_templates.xml:144`, `addons/portal/views/portal_templates.xml:157`, `addons/portal/views/portal_templates.xml:166`, `addons/portal/views/portal_templates.xml:207`, `addons/portal/views/portal_templates.xml:209`, `addons/portal/views/portal_templates.xml:217`, `addons/portal/views/portal_templates.xml:223`
- View/action field declarations: 11; representative evidence: `addons/portal/wizard/portal_wizard_views.xml:14`, `addons/portal/wizard/portal_wizard_views.xml:15`, `addons/portal/wizard/portal_wizard_views.xml:23`, `addons/portal/wizard/portal_wizard_views.xml:24`, `addons/portal/wizard/portal_share_views.xml:5`, `addons/portal/wizard/portal_share_views.xml:6`, `addons/portal/wizard/portal_share_views.xml:10`, `addons/portal/wizard/portal_share_views.xml:26`, `addons/portal/wizard/portal_share_views.xml:28`, `addons/portal/views/res_config_settings_views.xml:7`, `addons/portal/views/res_config_settings_views.xml:10`
- Browser assets: 33; representative files: `addons/portal/static/src/signature_form/signature_form.js`, `addons/portal/static/src/interactions/portal_composer.js`, `addons/portal/static/src/interactions/portal_security.js`, `addons/portal/static/src/interactions/sidebar.js`, `addons/portal/static/src/interactions/address.js`, `addons/portal/static/src/interactions/bootstrap_tooltip.js`, `addons/portal/static/src/interactions/address_card.js`, `addons/portal/static/src/interactions/portal_home_counters.js`, `addons/portal/static/src/interactions/portal_profile_editor.js`, `addons/portal/static/src/interactions/portal_search_panel.js`, `addons/portal/static/src/js/components/input_confirmation_dialog/input_confirmation_dialog.js`, `addons/portal/static/src/chatter/portal/suggestion_service_patch.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/portal/__manifest__.py`
- **HTTP entry points:** `addons/portal/controllers/portal.py:203`, `addons/portal/controllers/portal.py:229`, `addons/portal/controllers/portal.py:235`, `addons/portal/controllers/portal.py:264`, `addons/portal/controllers/portal.py:326`, `addons/portal/controllers/portal.py:485`, `addons/portal/controllers/portal.py:515`, `addons/portal/controllers/portal.py:933`, `addons/portal/controllers/portal.py:968`, `addons/portal/controllers/portal.py:987`, `addons/portal/controllers/portal.py:1000`, `addons/portal/controllers/portal.py:1043`
- **Scheduled entry points:** `addons/portal/wizard/portal_wizard_views.xml`, `addons/portal/tests/test_portal.py`
- **Report entry points:** `addons/portal/controllers/portal.py`

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/portal/models/res_partner.py:7); inherits `mail.message` (addons/portal/models/mail_message.py:8); inherits `ir.ui.view` (addons/portal/models/ir_ui_view.py:7); `portal.mixin` (addons/portal/models/portal_mixin.py:9); inherits `res.config.settings` (addons/portal/models/res_config_settings.py:7); inherits `ir.qweb` (addons/portal/models/ir_qweb.py:8); `portal.entry` (addons/portal/models/portal_entry.py:4); inherits `ir.http` (addons/portal/models/ir_http.py:7); inherits `res.country` (addons/portal/models/res_country.py:7); inherits `mail.thread` (addons/portal/models/mail_thread.py:10); inherits `res.users.apikeys.description` (addons/portal/models/res_users_apikeys_description.py:8); `portal.wizard` (addons/portal/wizard/portal_wizard.py:16); `portal.wizard.user` (addons/portal/wizard/portal_wizard.py:74); `portal.share` (addons/portal/wizard/portal_share.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 6
- Route declarations: 16
- Route evidence: `addons/portal/controllers/portal.py:203`, `addons/portal/controllers/portal.py:229`, `addons/portal/controllers/portal.py:235`, `addons/portal/controllers/portal.py:264`, `addons/portal/controllers/portal.py:326`, `addons/portal/controllers/portal.py:485`, `addons/portal/controllers/portal.py:515`, `addons/portal/controllers/portal.py:933`, `addons/portal/controllers/portal.py:968`, `addons/portal/controllers/portal.py:987`, `addons/portal/controllers/portal.py:1000`, `addons/portal/controllers/portal.py:1043`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `auth_signup`, `base_address_extended`, `html_editor`, `http_routing`, `mail`, `web`
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

- `addons/portal/__init__.py`
- `addons/portal/__manifest__.py`
- `addons/portal/controllers/__init__.py`
- `addons/portal/controllers/mail.py`
- `addons/portal/controllers/message_reaction.py`
- `addons/portal/controllers/portal.py`
- `addons/portal/controllers/thread.py`
- `addons/portal/controllers/web.py`
- `addons/portal/data/mail_templates.xml`
- `addons/portal/data/portal_entry_data.xml`
- `addons/portal/i18n/ar.po`
- `addons/portal/i18n/az.po`
- `addons/portal/i18n/bg.po`
- `addons/portal/i18n/bs.po`
- `addons/portal/i18n/ca.po`
- `addons/portal/i18n/cs.po`
- `addons/portal/i18n/da.po`
- `addons/portal/i18n/de.po`
- `addons/portal/i18n/el.po`
- `addons/portal/i18n/es.po`
- `addons/portal/i18n/es_419.po`
- `addons/portal/i18n/et.po`
- `addons/portal/i18n/fa.po`
- `addons/portal/i18n/fi.po`
- `addons/portal/i18n/fr.po`
- `addons/portal/i18n/gu.po`
- `addons/portal/i18n/he.po`
- `addons/portal/i18n/hi.po`
- `addons/portal/i18n/hr.po`
- `addons/portal/i18n/hu.po`
- `addons/portal/i18n/id.po`
- `addons/portal/i18n/is.po`
- `addons/portal/i18n/it.po`
- `addons/portal/i18n/ja.po`
- `addons/portal/i18n/kab.po`
- `addons/portal/i18n/km.po`
- `addons/portal/i18n/ko.po`
- `addons/portal/i18n/ku.po`
- `addons/portal/i18n/lo.po`
- `addons/portal/i18n/lt.po`
- `addons/portal/i18n/lv.po`
- `addons/portal/i18n/mn.po`
- `addons/portal/i18n/my.po`
- `addons/portal/i18n/nb.po`
- `addons/portal/i18n/nl.po`
- `addons/portal/i18n/pl.po`
- `addons/portal/i18n/portal.pot`
- `addons/portal/i18n/pt.po`
- `addons/portal/i18n/pt_BR.po`
- `addons/portal/i18n/ro.po`
- `addons/portal/i18n/ru.po`
- `addons/portal/i18n/sk.po`
- `addons/portal/i18n/sl.po`
- `addons/portal/i18n/sr@latin.po`
- `addons/portal/i18n/sv.po`
- `addons/portal/i18n/th.po`
- `addons/portal/i18n/tr.po`
- `addons/portal/i18n/uk.po`
- `addons/portal/i18n/uz.po`
- `addons/portal/i18n/vi.po`
- `addons/portal/i18n/zh_CN.po`
- `addons/portal/i18n/zh_TW.po`
- `addons/portal/models/__init__.py`
- `addons/portal/models/ir_http.py`
- `addons/portal/models/ir_qweb.py`
- `addons/portal/models/ir_ui_view.py`
- `addons/portal/models/mail_message.py`
- `addons/portal/models/mail_thread.py`
- `addons/portal/models/portal_entry.py`
- `addons/portal/models/portal_mixin.py`
- `addons/portal/models/res_config_settings.py`
- `addons/portal/models/res_country.py`
- `addons/portal/models/res_partner.py`
- `addons/portal/models/res_users_apikeys_description.py`
- `addons/portal/security/ir.access.csv`
- `addons/portal/static/src/chatter/frontend/portal_chatter_boot.js`
- `addons/portal/static/src/chatter/portal/@types/models.d.ts`
- `addons/portal/static/src/chatter/portal/attachment_upload_service_patch.js`
- `addons/portal/static/src/chatter/portal/chat_hub_service_patch.js`
- `addons/portal/static/src/chatter/portal/chatter_patch.js`
- `addons/portal/static/src/chatter/portal/composer_model_patch.js`
- `addons/portal/static/src/chatter/portal/composer_patch.js`
- `addons/portal/static/src/chatter/portal/message_model_patch.js`
- `addons/portal/static/src/chatter/portal/message_patch.js`
- `addons/portal/static/src/chatter/portal/portal_chatter.js`
- `addons/portal/static/src/chatter/portal/portal_chatter_plugin.js`
- `addons/portal/static/src/chatter/portal/portal_chatter_service.js`
- `addons/portal/static/src/chatter/portal/scss/portal_chatter.scss`
- `addons/portal/static/src/chatter/portal/scss/primary_variables.scss`
- `addons/portal/static/src/chatter/portal/scss/shadow.scss`
- `addons/portal/static/src/chatter/portal/suggestion_service_patch.js`
- `addons/portal/static/src/chatter/portal/thread_model_patch.js`
- `addons/portal/static/src/chatter/portal_project/chatter_patch.js`
- `addons/portal/static/src/chatter/portal_project/message_patch.xml`
- `addons/portal/static/src/chatter/portal_project/portal_chatter.xml`
- `addons/portal/static/src/chatter/portal_project/thread_model_patch.js`
- `addons/portal/static/src/core/common/@types/models.d.ts`
- `addons/portal/static/src/core/common/message_model_patch.js`
- `addons/portal/static/src/img/portal-addresses.svg`
- `addons/portal/static/src/img/portal-connection.svg`
- `addons/portal/static/src/interactions/address.js`
- `addons/portal/static/src/interactions/address_card.js`
- `addons/portal/static/src/interactions/bootstrap_tooltip.js`
- `addons/portal/static/src/interactions/portal_composer.js`
- `addons/portal/static/src/interactions/portal_home_counters.js`
- `addons/portal/static/src/interactions/portal_profile_editor.js`
- `addons/portal/static/src/interactions/portal_search_panel.js`
- `addons/portal/static/src/interactions/portal_security.js`
- `addons/portal/static/src/interactions/sidebar.js`
- `addons/portal/static/src/js/components/input_confirmation_dialog/input_confirmation_dialog.js`
- `addons/portal/static/src/js/components/input_confirmation_dialog/input_confirmation_dialog.xml`
- `addons/portal/static/src/scss/bootstrap_overridden.scss`
- `addons/portal/static/src/scss/portal.edit.scss`
- `addons/portal/static/src/scss/portal.scss`
- `addons/portal/static/src/scss/primary_variables.scss`
- `addons/portal/static/src/signature_form/signature_form.js`
- `addons/portal/static/src/signature_form/signature_form.xml`
- `addons/portal/static/src/views/fields/portal_wizard_user_one2many.js`
- `addons/portal/static/src/views/fields/portal_wizard_user_one2many.scss`
- `addons/portal/static/src/views/list/portal_wizard_user_list_controller.js`
- `addons/portal/static/src/xml/portal_chatter.xml`
- `addons/portal/static/src/xml/portal_security.xml`
- `addons/portal/static/tests/tours/portal.js`
- `addons/portal/static/tests/tours/skip_to_content.js`
- `addons/portal/tests/__init__.py`
- `addons/portal/tests/test_addresses.py`
- `addons/portal/tests/test_login.py`
- `addons/portal/tests/test_message_format_portal.py`
- `addons/portal/tests/test_pager.py`
- `addons/portal/tests/test_portal.py`
- `addons/portal/tests/test_portal_wizard.py`
- `addons/portal/tests/test_tours.py`
- `addons/portal/utils.py`
- `addons/portal/views/address_templates.xml`
- `addons/portal/views/mail_templates_public.xml`
- `addons/portal/views/portal_templates.xml`
- `addons/portal/views/res_config_settings_views.xml`
- `addons/portal/wizard/__init__.py`
- `addons/portal/wizard/portal_share.py`
- `addons/portal/wizard/portal_share_views.xml`
- `addons/portal/wizard/portal_wizard.py`
- `addons/portal/wizard/portal_wizard_views.xml`
