# Module: contacts

- **Module ID:** MOD-053
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/contacts`
- **Manifest:** `addons/contacts/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Centralize your address book

**Manifest description:**

This module gives you a quick view of your contacts directory, accessible from your home page.
You can track your vendors, customers and other contacts.

**Scope evidence:** The module contains 68 files, including 7 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `base_address_extended`, `mail`, `web_hierarchy`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 4 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/contacts/models/res_partner.py:6`, `addons/contacts/models/res_users.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 18 record/template/menu identifiers.
- **Evidence:** `addons/contacts/data/mail_demo.xml:5`, `addons/contacts/data/mail_demo.xml:14`, `addons/contacts/views/contact_views.xml:3`, `addons/contacts/views/contact_views.xml:52`, `addons/contacts/views/contact_views.xml:68`, `addons/contacts/views/contact_views.xml:74`, `addons/contacts/views/contact_views.xml:80`, `addons/contacts/views/contact_views.xml:88`, `addons/contacts/views/contact_views.xml:94`, `addons/contacts/views/contact_views.xml:100`, `addons/contacts/views/contact_views.xml:106`, `addons/contacts/views/contact_views.xml:111`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/contacts/tests/test_ui.py`, `addons/contacts/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `message_demo_partner_2_0`, `message_demo_partner_1_5_notif_0`, `res_partner_view_hierarchy`, `action_contacts`, `action_contacts_view_kanban`, `action_contacts_view_tree`, `action_contacts_view_form`, `menu_contacts`, `Contacts`, `Configuration`, `Contact Tags`, `Industries`, `menu_action_res_partner_bank_form`, `Localization`, `menu_country_partner`, `menu_country_state_partner`, `menu_res_city`, `Country Group`
- Menus: 11; representative evidence: `addons/contacts/views/contact_views.xml:88`, `addons/contacts/views/contact_views.xml:94`, `addons/contacts/views/contact_views.xml:100`, `addons/contacts/views/contact_views.xml:106`, `addons/contacts/views/contact_views.xml:111`, `addons/contacts/views/contact_views.xml:115`, `addons/contacts/views/contact_views.xml:121`, `addons/contacts/views/contact_views.xml:127`, `addons/contacts/views/contact_views.xml:132`, `addons/contacts/views/contact_views.xml:137`, `addons/contacts/views/contact_views.xml:142`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 8; representative evidence: `addons/contacts/data/mail_demo.xml:9`, `addons/contacts/views/contact_views.xml:5`, `addons/contacts/views/contact_views.xml:6`, `addons/contacts/views/contact_views.xml:56`, `addons/contacts/views/contact_views.xml:57`, `addons/contacts/views/contact_views.xml:70`, `addons/contacts/views/contact_views.xml:76`, `addons/contacts/views/contact_views.xml:82`
- Browser assets: 1; representative files: `addons/contacts/static/tests/tours/debug_menu_set_defaults.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/contacts/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.partner` (addons/contacts/models/res_partner.py:6); inherits `res.users` (addons/contacts/models/res_users.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base_address_extended`, `mail`, `web_hierarchy`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/contacts/__init__.py`
- `addons/contacts/__manifest__.py`
- `addons/contacts/data/mail_demo.xml`
- `addons/contacts/i18n/af.po`
- `addons/contacts/i18n/ar.po`
- `addons/contacts/i18n/az.po`
- `addons/contacts/i18n/bg.po`
- `addons/contacts/i18n/bs.po`
- `addons/contacts/i18n/ca.po`
- `addons/contacts/i18n/contacts.pot`
- `addons/contacts/i18n/cs.po`
- `addons/contacts/i18n/da.po`
- `addons/contacts/i18n/de.po`
- `addons/contacts/i18n/el.po`
- `addons/contacts/i18n/es.po`
- `addons/contacts/i18n/es_419.po`
- `addons/contacts/i18n/et.po`
- `addons/contacts/i18n/fa.po`
- `addons/contacts/i18n/fi.po`
- `addons/contacts/i18n/fr.po`
- `addons/contacts/i18n/gu.po`
- `addons/contacts/i18n/he.po`
- `addons/contacts/i18n/hi.po`
- `addons/contacts/i18n/hr.po`
- `addons/contacts/i18n/hu.po`
- `addons/contacts/i18n/id.po`
- `addons/contacts/i18n/is.po`
- `addons/contacts/i18n/it.po`
- `addons/contacts/i18n/ja.po`
- `addons/contacts/i18n/kab.po`
- `addons/contacts/i18n/km.po`
- `addons/contacts/i18n/ko.po`
- `addons/contacts/i18n/ku.po`
- `addons/contacts/i18n/lb.po`
- `addons/contacts/i18n/lo.po`
- `addons/contacts/i18n/lt.po`
- `addons/contacts/i18n/lv.po`
- `addons/contacts/i18n/mn.po`
- `addons/contacts/i18n/my.po`
- `addons/contacts/i18n/nb.po`
- `addons/contacts/i18n/nl.po`
- `addons/contacts/i18n/pl.po`
- `addons/contacts/i18n/pt.po`
- `addons/contacts/i18n/pt_BR.po`
- `addons/contacts/i18n/ro.po`
- `addons/contacts/i18n/ru.po`
- `addons/contacts/i18n/sk.po`
- `addons/contacts/i18n/sl.po`
- `addons/contacts/i18n/sr@latin.po`
- `addons/contacts/i18n/sv.po`
- `addons/contacts/i18n/th.po`
- `addons/contacts/i18n/tr.po`
- `addons/contacts/i18n/uk.po`
- `addons/contacts/i18n/uz.po`
- `addons/contacts/i18n/vi.po`
- `addons/contacts/i18n/zh_CN.po`
- `addons/contacts/i18n/zh_TW.po`
- `addons/contacts/models/__init__.py`
- `addons/contacts/models/res_partner.py`
- `addons/contacts/models/res_users.py`
- `addons/contacts/static/description/icon.png`
- `addons/contacts/static/description/icon.svg`
- `addons/contacts/static/description/icon_hi.png`
- `addons/contacts/static/src/views/contacts_hierarchy/contacts_hierarchy_card.scss`
- `addons/contacts/static/tests/tours/debug_menu_set_defaults.js`
- `addons/contacts/tests/__init__.py`
- `addons/contacts/tests/test_ui.py`
- `addons/contacts/views/contact_views.xml`
