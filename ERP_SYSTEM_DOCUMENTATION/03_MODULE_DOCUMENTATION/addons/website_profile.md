# Module: website_profile

- **Module ID:** MOD-632
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_profile`
- **Manifest:** `addons/website_profile/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Access the website profile of the users

**Manifest description:**

Allows to access the website profile of the users and see their statistics (karma, badges, etc..)

**Scope evidence:** The module contains 79 files, including 12 Python, 5 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `html_editor`, `website_partner`, `gamification`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 3
- XML/data/view/template files: 5
- Browser asset files: 5
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_profile/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 28 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_profile/models/gamification_badge.py:7`, `addons/website_profile/models/res_users.py:15`, `addons/website_profile/models/website.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 8 route declarations.
- **Evidence:** `addons/website_profile/controllers/main.py:84`, `addons/website_profile/controllers/main.py:114`, `addons/website_profile/controllers/main.py:129`, `addons/website_profile/controllers/main.py:187`, `addons/website_profile/controllers/main.py:211`, `addons/website_profile/controllers/main.py:319`, `addons/website_profile/controllers/main.py:326`, `addons/website_profile/controllers/main.py:334`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 5 JavaScript/TypeScript files; static XML analysis found 20 record/template/menu identifiers.
- **Evidence:** `addons/website_profile/data/mail_template_data.xml:6`, `addons/website_profile/views/gamification_badge_views.xml:3`, `addons/website_profile/views/website_views.xml:4`, `addons/website_profile/views/website_profile.xml:4`, `addons/website_profile/views/website_profile.xml:82`, `addons/website_profile/views/website_profile.xml:92`, `addons/website_profile/views/website_profile.xml:141`, `addons/website_profile/views/website_profile.xml:213`, `addons/website_profile/views/website_profile.xml:265`, `addons/website_profile/views/website_profile.xml:309`, `addons/website_profile/views/website_profile.xml:354`, `addons/website_profile/views/website_profile.xml:381`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_profile/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/website_profile/tests/test_website_profile.py`, `addons/website_profile/tests/__init__.py`, `addons/website_profile/tests/test_website_profile_technical_page.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `validation_email`, `gamification_badge_view_form`, `website_view_form`, `User profile subnav`, `Profile Page`, `Profile Page Header`, `Profile Page Content`, `Profile Next Rank Card`, `User Bagdes`, `Ranks Page`, `Badges Page content`, `badge_header`, `Access Denied - Profile Page`, `Users Page`, `Users Page Header`, `users_page_content`, `Top 3 User Card`, `All User Card`, `Pager (not box display)`, `email_validation_banner`
- Menus: 0; representative evidence: Not found in module
- Templates: 17; representative evidence: `addons/website_profile/views/website_profile.xml:4`, `addons/website_profile/views/website_profile.xml:82`, `addons/website_profile/views/website_profile.xml:92`, `addons/website_profile/views/website_profile.xml:141`, `addons/website_profile/views/website_profile.xml:213`, `addons/website_profile/views/website_profile.xml:265`, `addons/website_profile/views/website_profile.xml:309`, `addons/website_profile/views/website_profile.xml:354`, `addons/website_profile/views/website_profile.xml:381`, `addons/website_profile/views/website_profile.xml:393`, `addons/website_profile/views/website_profile.xml:407`, `addons/website_profile/views/website_profile.xml:424`
- View/action field declarations: 4; representative evidence: `addons/website_profile/views/gamification_badge_views.xml:5`, `addons/website_profile/views/gamification_badge_views.xml:7`, `addons/website_profile/views/website_views.xml:6`, `addons/website_profile/views/website_views.xml:8`
- Browser assets: 5; representative files: `addons/website_profile/static/src/interactions/profile_editor.js`, `addons/website_profile/static/src/interactions/profile_editor.edit.js`, `addons/website_profile/static/src/interactions/profile_validation.js`, `addons/website_profile/static/src/components/profile_dialog/profile_dialog.js`, `addons/website_profile/static/tests/tours/tour_website_profile_description.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_profile/__manifest__.py`
- **HTTP entry points:** `addons/website_profile/controllers/main.py:84`, `addons/website_profile/controllers/main.py:114`, `addons/website_profile/controllers/main.py:129`, `addons/website_profile/controllers/main.py:187`, `addons/website_profile/controllers/main.py:211`, `addons/website_profile/controllers/main.py:319`, `addons/website_profile/controllers/main.py:326`, `addons/website_profile/controllers/main.py:334`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: `gamification.badge` (addons/website_profile/models/gamification_badge.py:7); inherits `res.users` (addons/website_profile/models/res_users.py:15); inherits `website` (addons/website_profile/models/website.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 8
- Route evidence: `addons/website_profile/controllers/main.py:84`, `addons/website_profile/controllers/main.py:114`, `addons/website_profile/controllers/main.py:129`, `addons/website_profile/controllers/main.py:187`, `addons/website_profile/controllers/main.py:211`, `addons/website_profile/controllers/main.py:319`, `addons/website_profile/controllers/main.py:326`, `addons/website_profile/controllers/main.py:334`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `html_editor`, `website_partner`, `gamification`
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

- `addons/website_profile/__init__.py`
- `addons/website_profile/__manifest__.py`
- `addons/website_profile/controllers/__init__.py`
- `addons/website_profile/controllers/main.py`
- `addons/website_profile/controllers/portal.py`
- `addons/website_profile/data/mail_template_data.xml`
- `addons/website_profile/i18n/ar.po`
- `addons/website_profile/i18n/az.po`
- `addons/website_profile/i18n/bg.po`
- `addons/website_profile/i18n/bs.po`
- `addons/website_profile/i18n/ca.po`
- `addons/website_profile/i18n/cs.po`
- `addons/website_profile/i18n/da.po`
- `addons/website_profile/i18n/de.po`
- `addons/website_profile/i18n/el.po`
- `addons/website_profile/i18n/es.po`
- `addons/website_profile/i18n/es_419.po`
- `addons/website_profile/i18n/et.po`
- `addons/website_profile/i18n/fa.po`
- `addons/website_profile/i18n/fi.po`
- `addons/website_profile/i18n/fr.po`
- `addons/website_profile/i18n/he.po`
- `addons/website_profile/i18n/hi.po`
- `addons/website_profile/i18n/hr.po`
- `addons/website_profile/i18n/hu.po`
- `addons/website_profile/i18n/id.po`
- `addons/website_profile/i18n/it.po`
- `addons/website_profile/i18n/ja.po`
- `addons/website_profile/i18n/kab.po`
- `addons/website_profile/i18n/ko.po`
- `addons/website_profile/i18n/ku.po`
- `addons/website_profile/i18n/lo.po`
- `addons/website_profile/i18n/lt.po`
- `addons/website_profile/i18n/lv.po`
- `addons/website_profile/i18n/mn.po`
- `addons/website_profile/i18n/my.po`
- `addons/website_profile/i18n/nb.po`
- `addons/website_profile/i18n/nl.po`
- `addons/website_profile/i18n/pl.po`
- `addons/website_profile/i18n/pt.po`
- `addons/website_profile/i18n/pt_BR.po`
- `addons/website_profile/i18n/ro.po`
- `addons/website_profile/i18n/ru.po`
- `addons/website_profile/i18n/sk.po`
- `addons/website_profile/i18n/sl.po`
- `addons/website_profile/i18n/sr@latin.po`
- `addons/website_profile/i18n/sv.po`
- `addons/website_profile/i18n/th.po`
- `addons/website_profile/i18n/tr.po`
- `addons/website_profile/i18n/uk.po`
- `addons/website_profile/i18n/uz.po`
- `addons/website_profile/i18n/vi.po`
- `addons/website_profile/i18n/website_profile.pot`
- `addons/website_profile/i18n/zh_CN.po`
- `addons/website_profile/i18n/zh_TW.po`
- `addons/website_profile/models/__init__.py`
- `addons/website_profile/models/gamification_badge.py`
- `addons/website_profile/models/res_users.py`
- `addons/website_profile/models/website.py`
- `addons/website_profile/security/ir.access.csv`
- `addons/website_profile/static/src/components/profile_dialog/profile_dialog.js`
- `addons/website_profile/static/src/components/profile_dialog/profile_dialog.xml`
- `addons/website_profile/static/src/img/badge_bronze.svg`
- `addons/website_profile/static/src/img/badge_gold.svg`
- `addons/website_profile/static/src/img/badge_silver.svg`
- `addons/website_profile/static/src/img/rank_1.svg`
- `addons/website_profile/static/src/img/rank_2.svg`
- `addons/website_profile/static/src/img/rank_3.svg`
- `addons/website_profile/static/src/interactions/profile_editor.edit.js`
- `addons/website_profile/static/src/interactions/profile_editor.js`
- `addons/website_profile/static/src/interactions/profile_validation.js`
- `addons/website_profile/static/src/scss/website_profile.scss`
- `addons/website_profile/static/tests/tours/tour_website_profile_description.js`
- `addons/website_profile/tests/__init__.py`
- `addons/website_profile/tests/test_website_profile.py`
- `addons/website_profile/tests/test_website_profile_technical_page.py`
- `addons/website_profile/views/gamification_badge_views.xml`
- `addons/website_profile/views/website_profile.xml`
- `addons/website_profile/views/website_views.xml`
