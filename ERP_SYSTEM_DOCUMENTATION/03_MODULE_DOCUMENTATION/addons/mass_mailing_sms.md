# Module: mass_mailing_sms

- **Module ID:** MOD-372
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mass_mailing_sms`
- **Manifest:** `addons/mass_mailing_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Marketing/Email Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Design, send and track SMS

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 101 files, including 29 Python, 16 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `portal`, `mass_mailing`, `sms`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 2
- XML/data/view/template files: 16
- Browser asset files: 2
- Security files: 1
- Test files: 9
- Scheduled/automation evidence files: 2
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/mass_mailing_sms/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 94 methods, 0 constraint handlers, 0 onchange handlers, and 7 dependency declarations.
- **Evidence:** `addons/mass_mailing_sms/models/res_partner.py:6`, `addons/mass_mailing_sms/models/mailing_trace.py:10`, `addons/mass_mailing_sms/models/sms_sms.py:10`, `addons/mass_mailing_sms/models/utm_mixin.py:6`, `addons/mass_mailing_sms/models/mailing_contact.py:7`, `addons/mass_mailing_sms/models/link_tracker.py:6`, `addons/mass_mailing_sms/models/utm_campaign.py:7`, `addons/mass_mailing_sms/models/res_users.py:7`, `addons/mass_mailing_sms/models/mailing_list.py:8`, `addons/mass_mailing_sms/models/mailing_mailing.py:16`, `addons/mass_mailing_sms/models/sms_tracker.py:6`, `addons/mass_mailing_sms/wizard/mailing_contact_to_list.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/mass_mailing_sms/controllers/main.py:30`, `addons/mass_mailing_sms/controllers/main.py:83`, `addons/mass_mailing_sms/controllers/main.py:125`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 2 JavaScript/TypeScript files; static XML analysis found 73 record/template/menu identifiers.
- **Evidence:** `addons/mass_mailing_sms/demo/mailing_subscription.xml:3`, `addons/mass_mailing_sms/demo/mailing_subscription.xml:7`, `addons/mass_mailing_sms/demo/mailing_subscription.xml:11`, `addons/mass_mailing_sms/demo/mailing_subscription.xml:15`, `addons/mass_mailing_sms/demo/mailing_subscription.xml:19`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:3`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:8`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:14`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:20`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:25`, `addons/mass_mailing_sms/demo/mailing_list_contact.xml:30`, `addons/mass_mailing_sms/demo/mailing_trace.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/mass_mailing_sms/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 2 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/mass_mailing_sms/models/utm_campaign.py`, `addons/mass_mailing_sms/tests/test_mailing_retry.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/mass_mailing_sms/tests/test_mailing_internals.py`, `addons/mass_mailing_sms/tests/test_mailing_contact_to_list.py`, `addons/mass_mailing_sms/tests/common.py`, `addons/mass_mailing_sms/tests/test_mailing_list.py`, `addons/mass_mailing_sms/tests/test_mailing_ui.py`, `addons/mass_mailing_sms/tests/test_mailing_sms_ab_testing.py`, `addons/mass_mailing_sms/tests/test_mailing_controllers.py`, `addons/mass_mailing_sms/tests/test_mailing_retry.py`, `addons/mass_mailing_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `mailing_list_sms_0_sub_contact_0_0`, `mailing_list_sms_0_sub_contact_0_1`, `mailing_list_sms_0_sub_contact_0_2`, `mailing_list_sms_0_sub_contact_0_3`, `mailing_list_sms_0_sub_contact_0_4`, `mailing_list_sms_0`, `mailing_contact_0_0`, `mailing_contact_0_1`, `mailing_contact_0_2`, `mailing_contact_0_3`, `mailing_contact_0_4`, `mailing_sms_0_trace_0`, `mailing_sms_0_trace_1`, `mailing_sms_0_trace_2`, `mailing_sms_0_trace_3`, `mailing_sms_0_trace_4`, `mailing_sms_0_trace_5`, `mailing_sms_0_trace_6`, `mailing_sms_1_trace_0`, `mailing_sms_1_trace_1`
- Menus: 10; representative evidence: `addons/mass_mailing_sms/views/mailing_sms_menus.xml:4`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:11`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:19`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:25`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:32`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:40`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:48`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:56`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:62`, `addons/mass_mailing_sms/views/mailing_sms_menus.xml:69`
- Templates: 2; representative evidence: `addons/mass_mailing_sms/views/mass_mailing_sms_templates_portal.xml:3`, `addons/mass_mailing_sms/views/mass_mailing_sms_templates_portal.xml:34`
- View/action field declarations: 75; representative evidence: `addons/mass_mailing_sms/demo/mailing_trace.xml:8`, `addons/mass_mailing_sms/demo/mailing_trace.xml:18`, `addons/mass_mailing_sms/demo/mailing_trace.xml:28`, `addons/mass_mailing_sms/demo/mailing_trace.xml:38`, `addons/mass_mailing_sms/demo/mailing_trace.xml:48`, `addons/mass_mailing_sms/demo/mailing_trace.xml:59`, `addons/mass_mailing_sms/demo/mailing_trace.xml:70`, `addons/mass_mailing_sms/demo/mailing_trace.xml:116`, `addons/mass_mailing_sms/demo/mailing_trace.xml:125`, `addons/mass_mailing_sms/demo/mailing_trace.xml:134`, `addons/mass_mailing_sms/demo/mailing_trace.xml:143`, `addons/mass_mailing_sms/demo/mailing_trace.xml:152`
- Browser assets: 2; representative files: `addons/mass_mailing_sms/static/src/components/sms_widget/fields_sms_widget.js`, `addons/mass_mailing_sms/static/tests/tours/mailing_activities_split.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mass_mailing_sms/__manifest__.py`
- **HTTP entry points:** `addons/mass_mailing_sms/controllers/main.py:30`, `addons/mass_mailing_sms/controllers/main.py:83`, `addons/mass_mailing_sms/controllers/main.py:125`
- **Scheduled entry points:** `addons/mass_mailing_sms/models/utm_campaign.py`, `addons/mass_mailing_sms/tests/test_mailing_retry.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/mass_mailing_sms/models/res_partner.py:6); inherits `mailing.trace` (addons/mass_mailing_sms/models/mailing_trace.py:10); inherits `sms.sms` (addons/mass_mailing_sms/models/sms_sms.py:10); inherits `utm.mixin` (addons/mass_mailing_sms/models/utm_mixin.py:6); `mailing.contact` (addons/mass_mailing_sms/models/mailing_contact.py:7); inherits `link.tracker.click` (addons/mass_mailing_sms/models/link_tracker.py:6); inherits `utm.campaign` (addons/mass_mailing_sms/models/utm_campaign.py:7); inherits `res.users` (addons/mass_mailing_sms/models/res_users.py:7); inherits `mailing.list` (addons/mass_mailing_sms/models/mailing_list.py:8); inherits `mailing.mailing` (addons/mass_mailing_sms/models/mailing_mailing.py:16); inherits `sms.tracker` (addons/mass_mailing_sms/models/sms_tracker.py:6); inherits `mailing.contact.to.list` (addons/mass_mailing_sms/wizard/mailing_contact_to_list.py:6); inherits `sms.composer` (addons/mass_mailing_sms/wizard/sms_composer.py:7); `mailing.sms.test` (addons/mass_mailing_sms/wizard/mailing_sms_test.py:11)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/mass_mailing_sms/controllers/main.py:30`, `addons/mass_mailing_sms/controllers/main.py:83`, `addons/mass_mailing_sms/controllers/main.py:125`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `portal`, `mass_mailing`, `sms`
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

- `addons/mass_mailing_sms/__init__.py`
- `addons/mass_mailing_sms/__manifest__.py`
- `addons/mass_mailing_sms/controllers/__init__.py`
- `addons/mass_mailing_sms/controllers/main.py`
- `addons/mass_mailing_sms/data/utm_data.xml`
- `addons/mass_mailing_sms/demo/mailing_list_contact.xml`
- `addons/mass_mailing_sms/demo/mailing_mailing.xml`
- `addons/mass_mailing_sms/demo/mailing_subscription.xml`
- `addons/mass_mailing_sms/demo/mailing_trace.xml`
- `addons/mass_mailing_sms/i18n/ar.po`
- `addons/mass_mailing_sms/i18n/az.po`
- `addons/mass_mailing_sms/i18n/bg.po`
- `addons/mass_mailing_sms/i18n/bs.po`
- `addons/mass_mailing_sms/i18n/ca.po`
- `addons/mass_mailing_sms/i18n/cs.po`
- `addons/mass_mailing_sms/i18n/da.po`
- `addons/mass_mailing_sms/i18n/de.po`
- `addons/mass_mailing_sms/i18n/el.po`
- `addons/mass_mailing_sms/i18n/es.po`
- `addons/mass_mailing_sms/i18n/es_419.po`
- `addons/mass_mailing_sms/i18n/et.po`
- `addons/mass_mailing_sms/i18n/fa.po`
- `addons/mass_mailing_sms/i18n/fi.po`
- `addons/mass_mailing_sms/i18n/fr.po`
- `addons/mass_mailing_sms/i18n/he.po`
- `addons/mass_mailing_sms/i18n/hi.po`
- `addons/mass_mailing_sms/i18n/hr.po`
- `addons/mass_mailing_sms/i18n/hu.po`
- `addons/mass_mailing_sms/i18n/id.po`
- `addons/mass_mailing_sms/i18n/it.po`
- `addons/mass_mailing_sms/i18n/ja.po`
- `addons/mass_mailing_sms/i18n/kab.po`
- `addons/mass_mailing_sms/i18n/ko.po`
- `addons/mass_mailing_sms/i18n/ku.po`
- `addons/mass_mailing_sms/i18n/lb.po`
- `addons/mass_mailing_sms/i18n/lo.po`
- `addons/mass_mailing_sms/i18n/lt.po`
- `addons/mass_mailing_sms/i18n/lv.po`
- `addons/mass_mailing_sms/i18n/mass_mailing_sms.pot`
- `addons/mass_mailing_sms/i18n/mn.po`
- `addons/mass_mailing_sms/i18n/my.po`
- `addons/mass_mailing_sms/i18n/nb.po`
- `addons/mass_mailing_sms/i18n/nl.po`
- `addons/mass_mailing_sms/i18n/pl.po`
- `addons/mass_mailing_sms/i18n/pt.po`
- `addons/mass_mailing_sms/i18n/pt_BR.po`
- `addons/mass_mailing_sms/i18n/ro.po`
- `addons/mass_mailing_sms/i18n/ru.po`
- `addons/mass_mailing_sms/i18n/sk.po`
- `addons/mass_mailing_sms/i18n/sl.po`
- `addons/mass_mailing_sms/i18n/sr@latin.po`
- `addons/mass_mailing_sms/i18n/sv.po`
- `addons/mass_mailing_sms/i18n/th.po`
- `addons/mass_mailing_sms/i18n/tr.po`
- `addons/mass_mailing_sms/i18n/uk.po`
- `addons/mass_mailing_sms/i18n/uz.po`
- `addons/mass_mailing_sms/i18n/vi.po`
- `addons/mass_mailing_sms/i18n/zh_CN.po`
- `addons/mass_mailing_sms/i18n/zh_TW.po`
- `addons/mass_mailing_sms/models/__init__.py`
- `addons/mass_mailing_sms/models/link_tracker.py`
- `addons/mass_mailing_sms/models/mailing_contact.py`
- `addons/mass_mailing_sms/models/mailing_list.py`
- `addons/mass_mailing_sms/models/mailing_mailing.py`
- `addons/mass_mailing_sms/models/mailing_trace.py`
- `addons/mass_mailing_sms/models/res_partner.py`
- `addons/mass_mailing_sms/models/res_users.py`
- `addons/mass_mailing_sms/models/sms_sms.py`
- `addons/mass_mailing_sms/models/sms_tracker.py`
- `addons/mass_mailing_sms/models/utm_campaign.py`
- `addons/mass_mailing_sms/models/utm_mixin.py`
- `addons/mass_mailing_sms/report/mailing_trace_report_views.xml`
- `addons/mass_mailing_sms/security/ir.access.csv`
- `addons/mass_mailing_sms/static/description/icon.png`
- `addons/mass_mailing_sms/static/description/icon.svg`
- `addons/mass_mailing_sms/static/description/icon_hi.png`
- `addons/mass_mailing_sms/static/src/components/sms_widget/fields_sms_widget.js`
- `addons/mass_mailing_sms/static/tests/tours/mailing_activities_split.js`
- `addons/mass_mailing_sms/tests/__init__.py`
- `addons/mass_mailing_sms/tests/common.py`
- `addons/mass_mailing_sms/tests/test_mailing_contact_to_list.py`
- `addons/mass_mailing_sms/tests/test_mailing_controllers.py`
- `addons/mass_mailing_sms/tests/test_mailing_internals.py`
- `addons/mass_mailing_sms/tests/test_mailing_list.py`
- `addons/mass_mailing_sms/tests/test_mailing_retry.py`
- `addons/mass_mailing_sms/tests/test_mailing_sms_ab_testing.py`
- `addons/mass_mailing_sms/tests/test_mailing_ui.py`
- `addons/mass_mailing_sms/views/link_tracker_views.xml`
- `addons/mass_mailing_sms/views/mailing_contact_views.xml`
- `addons/mass_mailing_sms/views/mailing_list_views.xml`
- `addons/mass_mailing_sms/views/mailing_mailing_views.xml`
- `addons/mass_mailing_sms/views/mailing_sms_menus.xml`
- `addons/mass_mailing_sms/views/mailing_trace_views.xml`
- `addons/mass_mailing_sms/views/mass_mailing_sms_templates_portal.xml`
- `addons/mass_mailing_sms/views/utm_campaign_views.xml`
- `addons/mass_mailing_sms/wizard/__init__.py`
- `addons/mass_mailing_sms/wizard/mailing_contact_to_list.py`
- `addons/mass_mailing_sms/wizard/mailing_sms_test.py`
- `addons/mass_mailing_sms/wizard/mailing_sms_test_views.xml`
- `addons/mass_mailing_sms/wizard/sms_composer.py`
- `addons/mass_mailing_sms/wizard/sms_composer_views.xml`
