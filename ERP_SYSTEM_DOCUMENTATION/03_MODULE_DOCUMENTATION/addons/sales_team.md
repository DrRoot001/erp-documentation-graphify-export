# Module: sales_team

- **Module ID:** MOD-538
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sales_team`
- **Manifest:** `addons/sales_team/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Sales Teams

**Manifest description:**

Using this application you can manage Sales Teams with CRM and/or Sales
=======================================================================

**Scope evidence:** The module contains 91 files, including 12 Python, 8 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `mail`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 4
- Security files: 2
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sales_team/security/sales_team_security.xml`, `addons/sales_team/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 59 methods, 3 constraint handlers, 0 onchange handlers, and 10 dependency declarations.
- **Evidence:** `addons/sales_team/models/crm_team.py:8`, `addons/sales_team/models/res_users.py:6`, `addons/sales_team/models/crm_team_member.py:6`, `addons/sales_team/models/crm_tag.py:8`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 4 JavaScript/TypeScript files; static XML analysis found 40 record/template/menu identifiers.
- **Evidence:** `addons/sales_team/security/sales_team_security.xml:2`, `addons/sales_team/security/sales_team_security.xml:8`, `addons/sales_team/security/sales_team_security.xml:16`, `addons/sales_team/security/sales_team_security.xml:24`, `addons/sales_team/data/crm_team_demo.xml:4`, `addons/sales_team/data/crm_team_demo.xml:11`, `addons/sales_team/data/crm_team_demo.xml:15`, `addons/sales_team/data/crm_team_demo.xml:19`, `addons/sales_team/data/crm_team_demo.xml:24`, `addons/sales_team/data/crm_team_data.xml:4`, `addons/sales_team/data/crm_team_data.xml:10`, `addons/sales_team/data/crm_team_data.xml:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/sales_team/security/sales_team_security.xml`, `addons/sales_team/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/sales_team/tests/test_sales_team.py`, `addons/sales_team/tests/test_sales_team_membership.py`, `addons/sales_team/tests/test_sales_team_internals.py`, `addons/sales_team/tests/common.py`, `addons/sales_team/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `res_groups_privilege_sales`, `group_sale_salesman`, `group_sale_salesman_all_leads`, `group_sale_manager`, `base.user_demo`, `base.default_user_group`, `team_sales_department`, `crm_team_1`, `crm_team_member_demo_team_1`, `team_sales_department`, `crm_team_member_admin_sales`, `salesteam_website_sales`, `pos_sales_team`, `categ_oppor1`, `categ_oppor2`, `categ_oppor3`, `categ_oppor4`, `categ_oppor5`, `categ_oppor6`, `categ_oppor7`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 37; representative evidence: `addons/sales_team/views/crm_team_views.xml:6`, `addons/sales_team/views/crm_team_views.xml:7`, `addons/sales_team/views/crm_team_views.xml:23`, `addons/sales_team/views/crm_team_views.xml:24`, `addons/sales_team/views/crm_team_views.xml:97`, `addons/sales_team/views/crm_team_views.xml:98`, `addons/sales_team/views/crm_team_views.xml:111`, `addons/sales_team/views/crm_team_views.xml:112`, `addons/sales_team/views/crm_team_views.xml:129`, `addons/sales_team/views/crm_team_views.xml:131`, `addons/sales_team/views/crm_team_views.xml:182`, `addons/sales_team/views/crm_team_views.xml:183`
- Browser assets: 4; representative files: `addons/sales_team/static/tests/crm_team_form.test.js`, `addons/sales_team/static/tests/crm_team_test_helpers.js`, `addons/sales_team/static/src/js/crm_team_form.js`, `addons/sales_team/static/tests/mock_server/mock_models/crm_team.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sales_team/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `crm.team` (addons/sales_team/models/crm_team.py:8); inherits `res.users` (addons/sales_team/models/res_users.py:6); `crm.team.member` (addons/sales_team/models/crm_team_member.py:6); `crm.tag` (addons/sales_team/models/crm_tag.py:8)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `mail`
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

- `addons/sales_team/__init__.py`
- `addons/sales_team/__manifest__.py`
- `addons/sales_team/data/crm_tag_demo.xml`
- `addons/sales_team/data/crm_team_data.xml`
- `addons/sales_team/data/crm_team_demo.xml`
- `addons/sales_team/i18n/af.po`
- `addons/sales_team/i18n/am.po`
- `addons/sales_team/i18n/ar.po`
- `addons/sales_team/i18n/az.po`
- `addons/sales_team/i18n/bg.po`
- `addons/sales_team/i18n/bs.po`
- `addons/sales_team/i18n/ca.po`
- `addons/sales_team/i18n/cs.po`
- `addons/sales_team/i18n/da.po`
- `addons/sales_team/i18n/de.po`
- `addons/sales_team/i18n/el.po`
- `addons/sales_team/i18n/es.po`
- `addons/sales_team/i18n/es_419.po`
- `addons/sales_team/i18n/es_CL.po`
- `addons/sales_team/i18n/et.po`
- `addons/sales_team/i18n/eu.po`
- `addons/sales_team/i18n/fa.po`
- `addons/sales_team/i18n/fi.po`
- `addons/sales_team/i18n/fo.po`
- `addons/sales_team/i18n/fr.po`
- `addons/sales_team/i18n/fr_BE.po`
- `addons/sales_team/i18n/fr_CA.po`
- `addons/sales_team/i18n/gl.po`
- `addons/sales_team/i18n/gu.po`
- `addons/sales_team/i18n/he.po`
- `addons/sales_team/i18n/hi.po`
- `addons/sales_team/i18n/hr.po`
- `addons/sales_team/i18n/hu.po`
- `addons/sales_team/i18n/id.po`
- `addons/sales_team/i18n/is.po`
- `addons/sales_team/i18n/it.po`
- `addons/sales_team/i18n/ja.po`
- `addons/sales_team/i18n/ka.po`
- `addons/sales_team/i18n/kab.po`
- `addons/sales_team/i18n/km.po`
- `addons/sales_team/i18n/ko.po`
- `addons/sales_team/i18n/ku.po`
- `addons/sales_team/i18n/lb.po`
- `addons/sales_team/i18n/lo.po`
- `addons/sales_team/i18n/lt.po`
- `addons/sales_team/i18n/lv.po`
- `addons/sales_team/i18n/mk.po`
- `addons/sales_team/i18n/mn.po`
- `addons/sales_team/i18n/my.po`
- `addons/sales_team/i18n/nb.po`
- `addons/sales_team/i18n/nl.po`
- `addons/sales_team/i18n/pl.po`
- `addons/sales_team/i18n/pt.po`
- `addons/sales_team/i18n/pt_BR.po`
- `addons/sales_team/i18n/ro.po`
- `addons/sales_team/i18n/ru.po`
- `addons/sales_team/i18n/sales_team.pot`
- `addons/sales_team/i18n/sk.po`
- `addons/sales_team/i18n/sl.po`
- `addons/sales_team/i18n/sq.po`
- `addons/sales_team/i18n/sr@latin.po`
- `addons/sales_team/i18n/sv.po`
- `addons/sales_team/i18n/ta.po`
- `addons/sales_team/i18n/th.po`
- `addons/sales_team/i18n/tr.po`
- `addons/sales_team/i18n/uk.po`
- `addons/sales_team/i18n/uz.po`
- `addons/sales_team/i18n/vi.po`
- `addons/sales_team/i18n/zh_CN.po`
- `addons/sales_team/i18n/zh_TW.po`
- `addons/sales_team/models/__init__.py`
- `addons/sales_team/models/crm_tag.py`
- `addons/sales_team/models/crm_team.py`
- `addons/sales_team/models/crm_team_member.py`
- `addons/sales_team/models/res_users.py`
- `addons/sales_team/security/ir.access.csv`
- `addons/sales_team/security/sales_team_security.xml`
- `addons/sales_team/static/src/js/crm_team_form.js`
- `addons/sales_team/static/src/scss/crm_team_views.scss`
- `addons/sales_team/static/tests/crm_team_form.test.js`
- `addons/sales_team/static/tests/crm_team_test_helpers.js`
- `addons/sales_team/static/tests/mock_server/mock_models/crm_team.js`
- `addons/sales_team/tests/__init__.py`
- `addons/sales_team/tests/common.py`
- `addons/sales_team/tests/test_sales_team.py`
- `addons/sales_team/tests/test_sales_team_internals.py`
- `addons/sales_team/tests/test_sales_team_membership.py`
- `addons/sales_team/views/crm_tag_views.xml`
- `addons/sales_team/views/crm_team_member_views.xml`
- `addons/sales_team/views/crm_team_views.xml`
- `addons/sales_team/views/mail_activity_views.xml`
