# Module: gamification

- **Module ID:** MOD-074
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/gamification`
- **Manifest:** `addons/gamification/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Human Resources`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Gamification process
====================
The Gamification module provides ways to evaluate and motivate the users of Odoo.

The users can be evaluated using goals and numerical objectives to reach.
**Goals** are assigned through **challenges** to evaluate and compare members of a team with each others and through time.

For non-numerical achievements, **badges** can be granted to users. From a simple "thank you" to an exceptional achievement, a badge is an easy way to exprimate gratitude to a user for their good work.

Both goals and badges are flexibles and can be adapted to a large range of modules and actions. When installed, this module creates easy goals to help new users to discover Odoo and configure their user profile.

**Scope evidence:** The module contains 123 files, including 19 Python, 19 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `mail`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 0
- XML/data/view/template files: 19
- Browser asset files: 0
- Security files: 1
- Test files: 4
- Scheduled/automation evidence files: 6
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/gamification/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 101 methods, 1 constraint handlers, 0 onchange handlers, and 13 dependency declarations.
- **Evidence:** `addons/gamification/models/gamification_badge.py:14`, `addons/gamification/models/gamification_challenge_line.py:7`, `addons/gamification/models/gamification_badge_user.py:9`, `addons/gamification/models/gamification_goal_definition.py:10`, `addons/gamification/models/gamification_karma_rank.py:7`, `addons/gamification/models/gamification_challenge.py:50`, `addons/gamification/models/gamification_goal.py:14`, `addons/gamification/models/gamification_karma_tracking.py:10`, `addons/gamification/models/res_users.py:8`, `addons/gamification/wizard/update_goal.py:7`, `addons/gamification/wizard/grant_badge.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 19 XML files and 0 JavaScript/TypeScript files; static XML analysis found 89 record/template/menu identifiers.
- **Evidence:** `addons/gamification/wizard/grant_badge.xml:2`, `addons/gamification/wizard/grant_badge.xml:21`, `addons/gamification/wizard/update_goal.xml:2`, `addons/gamification/data/mail_template_data.xml:4`, `addons/gamification/data/mail_template_data.xml:45`, `addons/gamification/data/mail_template_data.xml:67`, `addons/gamification/data/mail_template_data.xml:268`, `addons/gamification/data/gamification_badge_data.xml:4`, `addons/gamification/data/gamification_badge_data.xml:11`, `addons/gamification/data/gamification_badge_data.xml:18`, `addons/gamification/data/gamification_badge_data.xml:26`, `addons/gamification/data/gamification_challenge_data.xml:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/gamification/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/gamification/__manifest__.py`, `addons/gamification/models/gamification_challenge.py`, `addons/gamification/models/gamification_karma_tracking.py`, `addons/gamification/data/ir_cron_data.xml`, `addons/gamification/tests/test_challenge.py`, `addons/gamification/tests/test_karma_tracking.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/gamification/tests/test_challenge.py`, `addons/gamification/tests/test_karma_tracking.py`, `addons/gamification/tests/common.py`, `addons/gamification/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 19; representative identifiers: `view_badge_wizard_grant`, `action_grant_wizard`, `view_goal_wizard_update_current`, `email_template_badge_received`, `email_template_goal_reminder`, `simple_report_template`, `mail_template_data_new_rank_reached`, `badge_good_job`, `badge_problem_solver`, `badge_hidden`, `badge_idea`, `definition_base_timezone`, `definition_base_company_data`, `definition_base_company_logo`, `definition_base_invite`, `challenge_base_discover`, `challenge_base_configure`, `line_base_discover1`, `line_base_admin2`, `line_base_admin1`
- Menus: 7; representative evidence: `addons/gamification/views/gamification_menus.xml:4`, `addons/gamification/views/gamification_menus.xml:9`, `addons/gamification/views/gamification_menus.xml:13`, `addons/gamification/views/gamification_menus.xml:17`, `addons/gamification/views/gamification_menus.xml:21`, `addons/gamification/views/gamification_menus.xml:25`, `addons/gamification/views/gamification_menus.xml:29`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 72; representative evidence: `addons/gamification/wizard/grant_badge.xml:4`, `addons/gamification/wizard/grant_badge.xml:5`, `addons/gamification/wizard/grant_badge.xml:23`, `addons/gamification/wizard/update_goal.xml:4`, `addons/gamification/wizard/update_goal.xml:5`, `addons/gamification/views/gamification_challenge_line_views.xml:6`, `addons/gamification/views/gamification_challenge_line_views.xml:7`, `addons/gamification/views/gamification_badge_views.xml:6`, `addons/gamification/views/gamification_badge_views.xml:7`, `addons/gamification/views/gamification_badge_views.xml:18`, `addons/gamification/views/gamification_badge_views.xml:20`, `addons/gamification/views/gamification_badge_views.xml:36`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/gamification/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/gamification/__manifest__.py`, `addons/gamification/models/gamification_challenge.py`, `addons/gamification/models/gamification_karma_tracking.py`, `addons/gamification/data/ir_cron_data.xml`, `addons/gamification/tests/test_challenge.py`, `addons/gamification/tests/test_karma_tracking.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: `gamification.badge` (addons/gamification/models/gamification_badge.py:14); `gamification.challenge.line` (addons/gamification/models/gamification_challenge_line.py:7); `gamification.badge.user` (addons/gamification/models/gamification_badge_user.py:9); `gamification.goal.definition` (addons/gamification/models/gamification_goal_definition.py:10); `gamification.karma.rank` (addons/gamification/models/gamification_karma_rank.py:7); `gamification.challenge` (addons/gamification/models/gamification_challenge.py:50); `gamification.goal` (addons/gamification/models/gamification_goal.py:14); `gamification.karma.tracking` (addons/gamification/models/gamification_karma_tracking.py:10); inherits `res.users` (addons/gamification/models/res_users.py:8); `gamification.goal.wizard` (addons/gamification/wizard/update_goal.py:7); `gamification.badge.user.wizard` (addons/gamification/wizard/grant_badge.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `mail`
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

- `addons/gamification/__init__.py`
- `addons/gamification/__manifest__.py`
- `addons/gamification/data/gamification_badge_data.xml`
- `addons/gamification/data/gamification_challenge_data.xml`
- `addons/gamification/data/gamification_karma_rank_data.xml`
- `addons/gamification/data/gamification_karma_rank_demo.xml`
- `addons/gamification/data/gamification_karma_tracking_demo.xml`
- `addons/gamification/data/ir_cron_data.xml`
- `addons/gamification/data/mail_template_data.xml`
- `addons/gamification/i18n/af.po`
- `addons/gamification/i18n/am.po`
- `addons/gamification/i18n/ar.po`
- `addons/gamification/i18n/az.po`
- `addons/gamification/i18n/bg.po`
- `addons/gamification/i18n/bs.po`
- `addons/gamification/i18n/ca.po`
- `addons/gamification/i18n/cs.po`
- `addons/gamification/i18n/da.po`
- `addons/gamification/i18n/de.po`
- `addons/gamification/i18n/el.po`
- `addons/gamification/i18n/es.po`
- `addons/gamification/i18n/es_419.po`
- `addons/gamification/i18n/es_CL.po`
- `addons/gamification/i18n/et.po`
- `addons/gamification/i18n/eu.po`
- `addons/gamification/i18n/fa.po`
- `addons/gamification/i18n/fi.po`
- `addons/gamification/i18n/fo.po`
- `addons/gamification/i18n/fr.po`
- `addons/gamification/i18n/fr_CA.po`
- `addons/gamification/i18n/gamification.pot`
- `addons/gamification/i18n/gl.po`
- `addons/gamification/i18n/gu.po`
- `addons/gamification/i18n/he.po`
- `addons/gamification/i18n/hi.po`
- `addons/gamification/i18n/hr.po`
- `addons/gamification/i18n/hu.po`
- `addons/gamification/i18n/id.po`
- `addons/gamification/i18n/is.po`
- `addons/gamification/i18n/it.po`
- `addons/gamification/i18n/ja.po`
- `addons/gamification/i18n/ka.po`
- `addons/gamification/i18n/kab.po`
- `addons/gamification/i18n/km.po`
- `addons/gamification/i18n/ko.po`
- `addons/gamification/i18n/ku.po`
- `addons/gamification/i18n/lo.po`
- `addons/gamification/i18n/lt.po`
- `addons/gamification/i18n/lv.po`
- `addons/gamification/i18n/mk.po`
- `addons/gamification/i18n/mn.po`
- `addons/gamification/i18n/my.po`
- `addons/gamification/i18n/nb.po`
- `addons/gamification/i18n/nl.po`
- `addons/gamification/i18n/pl.po`
- `addons/gamification/i18n/pt.po`
- `addons/gamification/i18n/pt_BR.po`
- `addons/gamification/i18n/ro.po`
- `addons/gamification/i18n/ru.po`
- `addons/gamification/i18n/sk.po`
- `addons/gamification/i18n/sl.po`
- `addons/gamification/i18n/sq.po`
- `addons/gamification/i18n/sr@latin.po`
- `addons/gamification/i18n/sv.po`
- `addons/gamification/i18n/th.po`
- `addons/gamification/i18n/tr.po`
- `addons/gamification/i18n/uk.po`
- `addons/gamification/i18n/uz.po`
- `addons/gamification/i18n/vi.po`
- `addons/gamification/i18n/zh_CN.po`
- `addons/gamification/i18n/zh_TW.po`
- `addons/gamification/models/__init__.py`
- `addons/gamification/models/gamification_badge.py`
- `addons/gamification/models/gamification_badge_user.py`
- `addons/gamification/models/gamification_challenge.py`
- `addons/gamification/models/gamification_challenge_line.py`
- `addons/gamification/models/gamification_goal.py`
- `addons/gamification/models/gamification_goal_definition.py`
- `addons/gamification/models/gamification_karma_rank.py`
- `addons/gamification/models/gamification_karma_tracking.py`
- `addons/gamification/models/res_users.py`
- `addons/gamification/security/ir.access.csv`
- `addons/gamification/static/description/icon.png`
- `addons/gamification/static/description/icon.svg`
- `addons/gamification/static/description/icon_hi.png`
- `addons/gamification/static/img/badge_good_job-image.png`
- `addons/gamification/static/img/badge_hidden-image.png`
- `addons/gamification/static/img/badge_idea-image.png`
- `addons/gamification/static/img/badge_problem_solver-image.png`
- `addons/gamification/static/img/rank_bachelor.png`
- `addons/gamification/static/img/rank_bachelor_badge.svg`
- `addons/gamification/static/img/rank_doctor.png`
- `addons/gamification/static/img/rank_doctor_badge.svg`
- `addons/gamification/static/img/rank_master.png`
- `addons/gamification/static/img/rank_master_badge.svg`
- `addons/gamification/static/img/rank_misc_hat.png`
- `addons/gamification/static/img/rank_misc_mug.png`
- `addons/gamification/static/img/rank_misc_unicorn.png`
- `addons/gamification/static/img/rank_misc_wand.png`
- `addons/gamification/static/img/rank_misc_world.png`
- `addons/gamification/static/img/rank_newbie.png`
- `addons/gamification/static/img/rank_newbie_badge.svg`
- `addons/gamification/static/img/rank_student.png`
- `addons/gamification/static/img/rank_student_badge.svg`
- `addons/gamification/tests/__init__.py`
- `addons/gamification/tests/common.py`
- `addons/gamification/tests/test_challenge.py`
- `addons/gamification/tests/test_karma_tracking.py`
- `addons/gamification/views/gamification_badge_user_views.xml`
- `addons/gamification/views/gamification_badge_views.xml`
- `addons/gamification/views/gamification_challenge_line_views.xml`
- `addons/gamification/views/gamification_challenge_views.xml`
- `addons/gamification/views/gamification_goal_definition_views.xml`
- `addons/gamification/views/gamification_goal_views.xml`
- `addons/gamification/views/gamification_karma_rank_views.xml`
- `addons/gamification/views/gamification_karma_tracking_views.xml`
- `addons/gamification/views/gamification_menus.xml`
- `addons/gamification/views/res_users_views.xml`
- `addons/gamification/wizard/__init__.py`
- `addons/gamification/wizard/grant_badge.py`
- `addons/gamification/wizard/grant_badge.xml`
- `addons/gamification/wizard/update_goal.py`
- `addons/gamification/wizard/update_goal.xml`
