# Module: hr_gamification

- **Module ID:** MOD-088
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_gamification`
- **Manifest:** `addons/hr_gamification/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Use the HR resources for the gamification process.

The HR officer can now manage challenges and badges.
This allow the user to send badges to employees instead of simple users.
Badge received are displayed on the user profile.

**Scope evidence:** The module contains 85 files, including 11 Python, 4 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `gamification`, `hr`.

## 2. Module structure

- Model/business logic files: 6
- Controller/API files: 0
- XML/data/view/template files: 4
- Browser asset files: 6
- Security files: 2
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_gamification/security/ir.access.csv`, `addons/hr_gamification/security/gamification_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 6 model declarations, 15 methods, 1 constraint handlers, 0 onchange handlers, and 4 dependency declarations.
- **Evidence:** `addons/hr_gamification/models/gamification.py:8`, `addons/hr_gamification/models/gamification.py:59`, `addons/hr_gamification/models/hr_employee_public.py:4`, `addons/hr_gamification/models/res_users.py:7`, `addons/hr_gamification/models/hr_employee.py:6`, `addons/hr_gamification/wizard/gamification_badge_user_wizard.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 6 JavaScript/TypeScript files; static XML analysis found 16 record/template/menu identifiers.
- **Evidence:** `addons/hr_gamification/security/gamification_security.xml:3`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:4`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:18`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:51`, `addons/hr_gamification/views/gamification_views.xml:4`, `addons/hr_gamification/views/gamification_views.xml:17`, `addons/hr_gamification/views/gamification_views.xml:91`, `addons/hr_gamification/views/gamification_views.xml:108`, `addons/hr_gamification/views/gamification_views.xml:124`, `addons/hr_gamification/views/gamification_views.xml:130`, `addons/hr_gamification/views/gamification_views.xml:137`, `addons/hr_gamification/views/gamification_views.xml:139`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_gamification/security/ir.access.csv`, `addons/hr_gamification/security/gamification_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/hr_gamification/tests/__init__.py`, `addons/hr_gamification/tests/test_gamification_current_badge.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `gamification.gamification_badge_user_access`, `view_badge_wizard_grant_employee`, `view_badge_wizard_reward`, `action_reward_wizard`, `hr_badge_form_view`, `view_current_badge_form`, `goals_menu_groupby_action2`, `challenge_list_action2`, `challenge_list_action2_view1`, `challenge_list_action2_view2`, `Challenges`, `gamification_badge_menu_hr`, `gamification_challenge_menu_hr`, `gamification_goal_menu_hr`, `hr_hr_employee_view_form`, `hr_employee_public_view_form`
- Menus: 4; representative evidence: `addons/hr_gamification/views/gamification_views.xml:137`, `addons/hr_gamification/views/gamification_views.xml:139`, `addons/hr_gamification/views/gamification_views.xml:140`, `addons/hr_gamification/views/gamification_views.xml:141`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 20; representative evidence: `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:6`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:8`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:20`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:21`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:53`, `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml:54`, `addons/hr_gamification/views/gamification_views.xml:6`, `addons/hr_gamification/views/gamification_views.xml:8`, `addons/hr_gamification/views/gamification_views.xml:19`, `addons/hr_gamification/views/gamification_views.xml:20`, `addons/hr_gamification/views/gamification_views.xml:92`, `addons/hr_gamification/views/gamification_views.xml:94`
- Browser assets: 6; representative files: `addons/hr_gamification/static/src/messaging_menu_patch.js`, `addons/hr_gamification/static/src/form_view.js`, `addons/hr_gamification/static/tests/messaging_menu_patch.test.js`, `addons/hr_gamification/static/tests/hr_gamification_test_helpers.js`, `addons/hr_gamification/static/tests/mock_server/mock_models/gamification_badge_user.js`, `addons/hr_gamification/static/tests/mock_server/mock_models/gamification_badge.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_gamification/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 6
- Representative model evidence: inherits `gamification.badge.user` (addons/hr_gamification/models/gamification.py:8); inherits `gamification.badge` (addons/hr_gamification/models/gamification.py:59); inherits `hr.employee.public` (addons/hr_gamification/models/hr_employee_public.py:4); inherits `res.users` (addons/hr_gamification/models/res_users.py:7); inherits `hr.employee` (addons/hr_gamification/models/hr_employee.py:6); inherits `gamification.badge.user.wizard` (addons/hr_gamification/wizard/gamification_badge_user_wizard.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `gamification`, `hr`
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

- `addons/hr_gamification/__init__.py`
- `addons/hr_gamification/__manifest__.py`
- `addons/hr_gamification/i18n/af.po`
- `addons/hr_gamification/i18n/am.po`
- `addons/hr_gamification/i18n/ar.po`
- `addons/hr_gamification/i18n/az.po`
- `addons/hr_gamification/i18n/bg.po`
- `addons/hr_gamification/i18n/bs.po`
- `addons/hr_gamification/i18n/ca.po`
- `addons/hr_gamification/i18n/cs.po`
- `addons/hr_gamification/i18n/da.po`
- `addons/hr_gamification/i18n/de.po`
- `addons/hr_gamification/i18n/el.po`
- `addons/hr_gamification/i18n/es.po`
- `addons/hr_gamification/i18n/es_419.po`
- `addons/hr_gamification/i18n/es_CL.po`
- `addons/hr_gamification/i18n/et.po`
- `addons/hr_gamification/i18n/eu.po`
- `addons/hr_gamification/i18n/fa.po`
- `addons/hr_gamification/i18n/fi.po`
- `addons/hr_gamification/i18n/fo.po`
- `addons/hr_gamification/i18n/fr.po`
- `addons/hr_gamification/i18n/fr_CA.po`
- `addons/hr_gamification/i18n/gl.po`
- `addons/hr_gamification/i18n/gu.po`
- `addons/hr_gamification/i18n/he.po`
- `addons/hr_gamification/i18n/hi.po`
- `addons/hr_gamification/i18n/hr.po`
- `addons/hr_gamification/i18n/hr_gamification.pot`
- `addons/hr_gamification/i18n/hu.po`
- `addons/hr_gamification/i18n/id.po`
- `addons/hr_gamification/i18n/is.po`
- `addons/hr_gamification/i18n/it.po`
- `addons/hr_gamification/i18n/ja.po`
- `addons/hr_gamification/i18n/ka.po`
- `addons/hr_gamification/i18n/kab.po`
- `addons/hr_gamification/i18n/km.po`
- `addons/hr_gamification/i18n/ko.po`
- `addons/hr_gamification/i18n/ku.po`
- `addons/hr_gamification/i18n/lo.po`
- `addons/hr_gamification/i18n/lt.po`
- `addons/hr_gamification/i18n/lv.po`
- `addons/hr_gamification/i18n/mk.po`
- `addons/hr_gamification/i18n/mn.po`
- `addons/hr_gamification/i18n/my.po`
- `addons/hr_gamification/i18n/nb.po`
- `addons/hr_gamification/i18n/nl.po`
- `addons/hr_gamification/i18n/pl.po`
- `addons/hr_gamification/i18n/pt.po`
- `addons/hr_gamification/i18n/pt_BR.po`
- `addons/hr_gamification/i18n/ro.po`
- `addons/hr_gamification/i18n/ru.po`
- `addons/hr_gamification/i18n/sk.po`
- `addons/hr_gamification/i18n/sl.po`
- `addons/hr_gamification/i18n/sq.po`
- `addons/hr_gamification/i18n/sr@latin.po`
- `addons/hr_gamification/i18n/sv.po`
- `addons/hr_gamification/i18n/th.po`
- `addons/hr_gamification/i18n/tr.po`
- `addons/hr_gamification/i18n/uk.po`
- `addons/hr_gamification/i18n/uz.po`
- `addons/hr_gamification/i18n/vi.po`
- `addons/hr_gamification/i18n/zh_CN.po`
- `addons/hr_gamification/i18n/zh_TW.po`
- `addons/hr_gamification/models/__init__.py`
- `addons/hr_gamification/models/gamification.py`
- `addons/hr_gamification/models/hr_employee.py`
- `addons/hr_gamification/models/hr_employee_public.py`
- `addons/hr_gamification/models/res_users.py`
- `addons/hr_gamification/security/gamification_security.xml`
- `addons/hr_gamification/security/ir.access.csv`
- `addons/hr_gamification/static/src/form_view.js`
- `addons/hr_gamification/static/src/messaging_menu_patch.js`
- `addons/hr_gamification/static/src/scss/hr_gamification.scss`
- `addons/hr_gamification/static/tests/hr_gamification_test_helpers.js`
- `addons/hr_gamification/static/tests/messaging_menu_patch.test.js`
- `addons/hr_gamification/static/tests/mock_server/mock_models/gamification_badge.js`
- `addons/hr_gamification/static/tests/mock_server/mock_models/gamification_badge_user.js`
- `addons/hr_gamification/tests/__init__.py`
- `addons/hr_gamification/tests/test_gamification_current_badge.py`
- `addons/hr_gamification/views/gamification_views.xml`
- `addons/hr_gamification/views/hr_employee_views.xml`
- `addons/hr_gamification/wizard/__init__.py`
- `addons/hr_gamification/wizard/gamification_badge_user_wizard.py`
- `addons/hr_gamification/wizard/gamification_badge_user_wizard_views.xml`
