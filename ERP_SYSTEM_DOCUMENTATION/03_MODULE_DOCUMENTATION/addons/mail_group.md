# Module: mail_group

- **Module ID:** MOD-354
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mail_group`
- **Manifest:** `addons/mail_group/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `not declared`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Manage your mailing lists

**Manifest description:**

Manage your mailing lists from Odoo.

**Scope evidence:** The module contains 88 files, including 18 Python, 14 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `mail`, `portal`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 2
- XML/data/view/template files: 14
- Browser asset files: 2
- Security files: 1
- Test files: 7
- Scheduled/automation evidence files: 3
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mail_group/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 112 methods, 6 constraint handlers, 2 onchange handlers, and 15 dependency declarations.
- **Evidence:** `addons/mail_group/models/mail_group_moderation.py:8`, `addons/mail_group/models/mail_group.py:27`, `addons/mail_group/models/mail_group_member.py:12`, `addons/mail_group/models/mail_group_message.py:16`, `addons/mail_group/wizard/mail_group_message_reject.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 9 route declarations.
- **Evidence:** `addons/mail_group/controllers/portal.py:63`, `addons/mail_group/controllers/portal.py:104`, `addons/mail_group/controllers/portal.py:146`, `addons/mail_group/controllers/portal.py:183`, `addons/mail_group/controllers/portal.py:218`, `addons/mail_group/controllers/portal.py:242`, `addons/mail_group/controllers/portal.py:276`, `addons/mail_group/controllers/portal.py:344`, `addons/mail_group/controllers/portal.py:360`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 2 JavaScript/TypeScript files; static XML analysis found 59 record/template/menu identifiers.
- **Evidence:** `addons/mail_group/wizard/mail_group_message_reject_views.xml:3`, `addons/mail_group/wizard/mail_group_message_reject_views.xml:36`, `addons/mail_group/data/mail_template_data.xml:3`, `addons/mail_group/data/mail_template_data.xml:22`, `addons/mail_group/data/mail_template_data.xml:44`, `addons/mail_group/data/mail_template_email_layouts.xml:4`, `addons/mail_group/data/mail_group_demo.xml:4`, `addons/mail_group/data/mail_group_demo.xml:14`, `addons/mail_group/data/mail_group_demo.xml:19`, `addons/mail_group/data/mail_group_demo.xml:25`, `addons/mail_group/data/mail_group_demo.xml:29`, `addons/mail_group/data/mail_group_demo.xml:34`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/mail_group/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 3 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mail_group/__manifest__.py`, `addons/mail_group/models/mail_group.py`, `addons/mail_group/data/ir_cron_data.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 7 test files are present.
- **Evidence:** `addons/mail_group/tests/test_mail_group_mailing.py`, `addons/mail_group/tests/test_mail_group_message.py`, `addons/mail_group/tests/test_mail_group_moderation.py`, `addons/mail_group/tests/common.py`, `addons/mail_group/tests/__init__.py`, `addons/mail_group/tests/test_mail_group.py`, `addons/mail_group/tests/data.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `mail_group_message_reject_form`, `mail_group_message_reject_action`, `mail_template_guidelines`, `mail_template_list_subscribe`, `mail_template_list_unsubscribe`, `email_template_mail_group_closed`, `mail_group_1`, `mail_group_member_1`, `mail_group_member_2`, `ir_attachment_mail_group_message_1`, `ir_attachment_mail_group_message_2`, `mail_group_message_1`, `mail_group_message_1_1`, `mail_group_message_1_1_1`, `mail_group_message_1_2`, `mail_group_message_1_2_1`, `mail_group_message_2`, `mail_group_message_3`, `mail_group_message_3_1`, `mail_group_message_3_1_1`
- Menus: 2; representative evidence: `addons/mail_group/views/mail_group_menus.xml:3`, `addons/mail_group/views/mail_group_menus.xml:8`
- Templates: 14; representative evidence: `addons/mail_group/data/mail_template_email_layouts.xml:4`, `addons/mail_group/data/mail_templates.xml:4`, `addons/mail_group/data/mail_templates.xml:13`, `addons/mail_group/views/portal_templates.xml:8`, `addons/mail_group/views/portal_templates.xml:75`, `addons/mail_group/views/portal_templates.xml:102`, `addons/mail_group/views/portal_templates.xml:159`, `addons/mail_group/views/portal_templates.xml:213`, `addons/mail_group/views/portal_templates.xml:243`, `addons/mail_group/views/portal_templates.xml:259`, `addons/mail_group/views/portal_templates.xml:285`, `addons/mail_group/views/portal_templates.xml:296`
- View/action field declarations: 36; representative evidence: `addons/mail_group/wizard/mail_group_message_reject_views.xml:5`, `addons/mail_group/wizard/mail_group_message_reject_views.xml:6`, `addons/mail_group/wizard/mail_group_message_reject_views.xml:38`, `addons/mail_group/wizard/mail_group_message_reject_views.xml:39`, `addons/mail_group/views/mail_group_message_views.xml:5`, `addons/mail_group/views/mail_group_message_views.xml:6`, `addons/mail_group/views/mail_group_message_views.xml:40`, `addons/mail_group/views/mail_group_message_views.xml:41`, `addons/mail_group/views/mail_group_message_views.xml:94`, `addons/mail_group/views/mail_group_message_views.xml:95`, `addons/mail_group/views/mail_group_message_views.xml:110`, `addons/mail_group/views/mail_group_message_views.xml:111`
- Browser assets: 2; representative files: `addons/mail_group/static/src/interactions/mail_group_message.js`, `addons/mail_group/static/src/interactions/mail_group.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mail_group/__manifest__.py`
- **HTTP entry points:** `addons/mail_group/controllers/portal.py:63`, `addons/mail_group/controllers/portal.py:104`, `addons/mail_group/controllers/portal.py:146`, `addons/mail_group/controllers/portal.py:183`, `addons/mail_group/controllers/portal.py:218`, `addons/mail_group/controllers/portal.py:242`, `addons/mail_group/controllers/portal.py:276`, `addons/mail_group/controllers/portal.py:344`, `addons/mail_group/controllers/portal.py:360`
- **Scheduled entry points:** `addons/mail_group/__manifest__.py`, `addons/mail_group/models/mail_group.py`, `addons/mail_group/data/ir_cron_data.xml`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: `mail.group.moderation` (addons/mail_group/models/mail_group_moderation.py:8); `mail.group` (addons/mail_group/models/mail_group.py:27); `mail.group.member` (addons/mail_group/models/mail_group_member.py:12); `mail.group.message` (addons/mail_group/models/mail_group_message.py:16); `mail.group.message.reject` (addons/mail_group/wizard/mail_group_message_reject.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 9
- Route evidence: `addons/mail_group/controllers/portal.py:63`, `addons/mail_group/controllers/portal.py:104`, `addons/mail_group/controllers/portal.py:146`, `addons/mail_group/controllers/portal.py:183`, `addons/mail_group/controllers/portal.py:218`, `addons/mail_group/controllers/portal.py:242`, `addons/mail_group/controllers/portal.py:276`, `addons/mail_group/controllers/portal.py:344`, `addons/mail_group/controllers/portal.py:360`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`, `portal`
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

- `addons/mail_group/__init__.py`
- `addons/mail_group/__manifest__.py`
- `addons/mail_group/controllers/__init__.py`
- `addons/mail_group/controllers/portal.py`
- `addons/mail_group/data/ir_cron_data.xml`
- `addons/mail_group/data/mail_group_demo.xml`
- `addons/mail_group/data/mail_template_data.xml`
- `addons/mail_group/data/mail_template_email_layouts.xml`
- `addons/mail_group/data/mail_templates.xml`
- `addons/mail_group/data/res_groups.xml`
- `addons/mail_group/i18n/ar.po`
- `addons/mail_group/i18n/az.po`
- `addons/mail_group/i18n/bg.po`
- `addons/mail_group/i18n/bs.po`
- `addons/mail_group/i18n/ca.po`
- `addons/mail_group/i18n/cs.po`
- `addons/mail_group/i18n/da.po`
- `addons/mail_group/i18n/de.po`
- `addons/mail_group/i18n/el.po`
- `addons/mail_group/i18n/es.po`
- `addons/mail_group/i18n/es_419.po`
- `addons/mail_group/i18n/et.po`
- `addons/mail_group/i18n/fa.po`
- `addons/mail_group/i18n/fi.po`
- `addons/mail_group/i18n/fr.po`
- `addons/mail_group/i18n/he.po`
- `addons/mail_group/i18n/hi.po`
- `addons/mail_group/i18n/hr.po`
- `addons/mail_group/i18n/hu.po`
- `addons/mail_group/i18n/id.po`
- `addons/mail_group/i18n/it.po`
- `addons/mail_group/i18n/ja.po`
- `addons/mail_group/i18n/kab.po`
- `addons/mail_group/i18n/ko.po`
- `addons/mail_group/i18n/ku.po`
- `addons/mail_group/i18n/lo.po`
- `addons/mail_group/i18n/lt.po`
- `addons/mail_group/i18n/lv.po`
- `addons/mail_group/i18n/mail_group.pot`
- `addons/mail_group/i18n/mn.po`
- `addons/mail_group/i18n/my.po`
- `addons/mail_group/i18n/nb.po`
- `addons/mail_group/i18n/nl.po`
- `addons/mail_group/i18n/pl.po`
- `addons/mail_group/i18n/pt.po`
- `addons/mail_group/i18n/pt_BR.po`
- `addons/mail_group/i18n/ro.po`
- `addons/mail_group/i18n/ru.po`
- `addons/mail_group/i18n/sk.po`
- `addons/mail_group/i18n/sl.po`
- `addons/mail_group/i18n/sr@latin.po`
- `addons/mail_group/i18n/sv.po`
- `addons/mail_group/i18n/th.po`
- `addons/mail_group/i18n/tr.po`
- `addons/mail_group/i18n/uk.po`
- `addons/mail_group/i18n/uz.po`
- `addons/mail_group/i18n/vi.po`
- `addons/mail_group/i18n/zh_CN.po`
- `addons/mail_group/i18n/zh_TW.po`
- `addons/mail_group/models/__init__.py`
- `addons/mail_group/models/mail_group.py`
- `addons/mail_group/models/mail_group_member.py`
- `addons/mail_group/models/mail_group_message.py`
- `addons/mail_group/models/mail_group_moderation.py`
- `addons/mail_group/security/ir.access.csv`
- `addons/mail_group/static/src/css/mail_group.scss`
- `addons/mail_group/static/src/css/mail_group_backend.scss`
- `addons/mail_group/static/src/img/fa_envelope_square.svg`
- `addons/mail_group/static/src/img/mail_group_portal.jpg`
- `addons/mail_group/static/src/interactions/mail_group.js`
- `addons/mail_group/static/src/interactions/mail_group_message.js`
- `addons/mail_group/tests/__init__.py`
- `addons/mail_group/tests/common.py`
- `addons/mail_group/tests/data.py`
- `addons/mail_group/tests/test_mail_group.py`
- `addons/mail_group/tests/test_mail_group_mailing.py`
- `addons/mail_group/tests/test_mail_group_message.py`
- `addons/mail_group/tests/test_mail_group_moderation.py`
- `addons/mail_group/views/mail_compose_message_views.xml`
- `addons/mail_group/views/mail_group_member_views.xml`
- `addons/mail_group/views/mail_group_menus.xml`
- `addons/mail_group/views/mail_group_message_views.xml`
- `addons/mail_group/views/mail_group_moderation_views.xml`
- `addons/mail_group/views/mail_group_views.xml`
- `addons/mail_group/views/portal_templates.xml`
- `addons/mail_group/wizard/__init__.py`
- `addons/mail_group/wizard/mail_group_message_reject.py`
- `addons/mail_group/wizard/mail_group_message_reject_views.xml`
