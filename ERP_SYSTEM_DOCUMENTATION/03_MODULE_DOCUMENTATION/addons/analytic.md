# Module: analytic

- **Module ID:** MOD-017
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/analytic`
- **Manifest:** `addons/analytic/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Module for defining analytic accounting object.
===============================================

In Odoo, analytic accounts are linked to general accounts but are treated
totally independently. So, you can enter various different analytic operations
that have no counterpart in the general financial accounts.

**Scope evidence:** The module contains 113 files, including 18 Python, 8 XML, and 18 JavaScript/TypeScript files. The manifest declares dependencies: `base`, `mail`, `uom`.

## 2. Module structure

- Model/business logic files: 10
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 18
- Security files: 2
- Test files: 6
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/analytic/security/ir.access.csv`, `addons/analytic/security/analytic_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 10 model declarations, 123 methods, 4 constraint handlers, 1 onchange handlers, and 9 dependency declarations.
- **Evidence:** `addons/analytic/models/ir_config_parameter.py:7`, `addons/analytic/models/res_groups.py:6`, `addons/analytic/models/res_config_settings.py:7`, `addons/analytic/models/analytic_plan.py:11`, `addons/analytic/models/analytic_plan.py:445`, `addons/analytic/models/analytic_account.py:11`, `addons/analytic/models/analytic_line.py:11`, `addons/analytic/models/analytic_line.py:163`, `addons/analytic/models/analytic_mixin.py:13`, `addons/analytic/models/analytic_distribution_model.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 18 JavaScript/TypeScript files; static XML analysis found 49 record/template/menu identifiers.
- **Evidence:** `addons/analytic/security/analytic_security.xml:3`, `addons/analytic/data/analytic_account_demo.xml:5`, `addons/analytic/data/analytic_account_demo.xml:9`, `addons/analytic/data/analytic_account_demo.xml:14`, `addons/analytic/data/analytic_account_demo.xml:19`, `addons/analytic/data/analytic_account_demo.xml:24`, `addons/analytic/data/analytic_account_demo.xml:30`, `addons/analytic/data/analytic_account_demo.xml:36`, `addons/analytic/data/analytic_account_demo.xml:42`, `addons/analytic/data/analytic_account_demo.xml:48`, `addons/analytic/data/analytic_account_demo.xml:54`, `addons/analytic/data/analytic_account_demo.xml:60`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/analytic/security/ir.access.csv`, `addons/analytic/security/analytic_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 6 test files are present.
- **Evidence:** `addons/analytic/tests/test_plan_operations.py`, `addons/analytic/tests/common.py`, `addons/analytic/tests/test_analytic_mixin.py`, `addons/analytic/tests/__init__.py`, `addons/analytic/tests/test_analytic_account.py`, `addons/analytic/tests/test_analytic_dynamic_update.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `group_analytic_accounting`, `analytic_plan_departments`, `analytic_plan_internal`, `analytic_absences`, `analytic_internal`, `analytic_our_super_product`, `analytic_seagate_p2`, `analytic_millennium_industries`, `analytic_integration_c2c`, `analytic_agrolait`, `analytic_asustek`, `analytic_deltapc`, `analytic_spark`, `analytic_nebula`, `analytic_luminous_technologies`, `analytic_desertic_hispafuentes`, `analytic_think_big_systems`, `analytic_partners_camp_to_camp`, `analytic_active_account`, `analytic_administratif`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 42; representative evidence: `addons/analytic/views/analytic_line_views.xml:5`, `addons/analytic/views/analytic_line_views.xml:6`, `addons/analytic/views/analytic_line_views.xml:29`, `addons/analytic/views/analytic_line_views.xml:30`, `addons/analytic/views/analytic_line_views.xml:47`, `addons/analytic/views/analytic_line_views.xml:48`, `addons/analytic/views/analytic_line_views.xml:72`, `addons/analytic/views/analytic_line_views.xml:74`, `addons/analytic/views/analytic_line_views.xml:99`, `addons/analytic/views/analytic_line_views.xml:100`, `addons/analytic/views/analytic_line_views.xml:112`, `addons/analytic/views/analytic_line_views.xml:113`
- Browser assets: 18; representative files: `addons/analytic/static/tests/batched_orm_service.test.js`, `addons/analytic/static/tests/analytic_distribution.test.js`, `addons/analytic/static/tests/analytic_test_helpers.js`, `addons/analytic/static/tests/analytic_widget.test.js`, `addons/analytic/static/tests/analytic_views.test.js`, `addons/analytic/static/src/services/batched_orm_service.js`, `addons/analytic/static/src/services/reload_analytic_plan_service.js`, `addons/analytic/static/src/views/analytic_search_model.js`, `addons/analytic/static/src/components/analytic_distribution/analytic_distribution.js`, `addons/analytic/static/src/views/pivot/pivot_view.js`, `addons/analytic/static/src/views/pivot/pivot_renderer.js`, `addons/analytic/static/src/views/graph/graph_view.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/analytic/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 10
- Representative model evidence: inherits `ir.config_parameter` (addons/analytic/models/ir_config_parameter.py:7); inherits `res.groups` (addons/analytic/models/res_groups.py:6); inherits `res.config.settings` (addons/analytic/models/res_config_settings.py:7); `account.analytic.plan` (addons/analytic/models/analytic_plan.py:11); `account.analytic.applicability` (addons/analytic/models/analytic_plan.py:445); `account.analytic.account` (addons/analytic/models/analytic_account.py:11); `analytic.plan.fields.mixin` (addons/analytic/models/analytic_line.py:11); `account.analytic.line` (addons/analytic/models/analytic_line.py:163); `analytic.mixin` (addons/analytic/models/analytic_mixin.py:13); `account.analytic.distribution.model` (addons/analytic/models/analytic_distribution_model.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`, `mail`, `uom`
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

- `addons/analytic/__init__.py`
- `addons/analytic/__manifest__.py`
- `addons/analytic/data/analytic_account_demo.xml`
- `addons/analytic/data/analytic_data.xml`
- `addons/analytic/i18n/af.po`
- `addons/analytic/i18n/am.po`
- `addons/analytic/i18n/analytic.pot`
- `addons/analytic/i18n/ar.po`
- `addons/analytic/i18n/az.po`
- `addons/analytic/i18n/bg.po`
- `addons/analytic/i18n/bs.po`
- `addons/analytic/i18n/ca.po`
- `addons/analytic/i18n/cs.po`
- `addons/analytic/i18n/da.po`
- `addons/analytic/i18n/de.po`
- `addons/analytic/i18n/el.po`
- `addons/analytic/i18n/es.po`
- `addons/analytic/i18n/es_419.po`
- `addons/analytic/i18n/es_CL.po`
- `addons/analytic/i18n/et.po`
- `addons/analytic/i18n/eu.po`
- `addons/analytic/i18n/fa.po`
- `addons/analytic/i18n/fi.po`
- `addons/analytic/i18n/fo.po`
- `addons/analytic/i18n/fr.po`
- `addons/analytic/i18n/fr_BE.po`
- `addons/analytic/i18n/fr_CA.po`
- `addons/analytic/i18n/gl.po`
- `addons/analytic/i18n/gu.po`
- `addons/analytic/i18n/he.po`
- `addons/analytic/i18n/hi.po`
- `addons/analytic/i18n/hr.po`
- `addons/analytic/i18n/hu.po`
- `addons/analytic/i18n/hy.po`
- `addons/analytic/i18n/id.po`
- `addons/analytic/i18n/is.po`
- `addons/analytic/i18n/it.po`
- `addons/analytic/i18n/ja.po`
- `addons/analytic/i18n/ka.po`
- `addons/analytic/i18n/kab.po`
- `addons/analytic/i18n/kk.po`
- `addons/analytic/i18n/km.po`
- `addons/analytic/i18n/ko.po`
- `addons/analytic/i18n/ku.po`
- `addons/analytic/i18n/lo.po`
- `addons/analytic/i18n/lt.po`
- `addons/analytic/i18n/lv.po`
- `addons/analytic/i18n/mk.po`
- `addons/analytic/i18n/mn.po`
- `addons/analytic/i18n/my.po`
- `addons/analytic/i18n/nb.po`
- `addons/analytic/i18n/nl.po`
- `addons/analytic/i18n/pl.po`
- `addons/analytic/i18n/pt.po`
- `addons/analytic/i18n/pt_BR.po`
- `addons/analytic/i18n/ro.po`
- `addons/analytic/i18n/ru.po`
- `addons/analytic/i18n/sk.po`
- `addons/analytic/i18n/sl.po`
- `addons/analytic/i18n/sq.po`
- `addons/analytic/i18n/sr@latin.po`
- `addons/analytic/i18n/sv.po`
- `addons/analytic/i18n/ta.po`
- `addons/analytic/i18n/te.po`
- `addons/analytic/i18n/th.po`
- `addons/analytic/i18n/tr.po`
- `addons/analytic/i18n/uk.po`
- `addons/analytic/i18n/uz.po`
- `addons/analytic/i18n/vi.po`
- `addons/analytic/i18n/zh_CN.po`
- `addons/analytic/i18n/zh_TW.po`
- `addons/analytic/migrations/1.2/pre-migrate.py`
- `addons/analytic/models/__init__.py`
- `addons/analytic/models/analytic_account.py`
- `addons/analytic/models/analytic_distribution_model.py`
- `addons/analytic/models/analytic_line.py`
- `addons/analytic/models/analytic_mixin.py`
- `addons/analytic/models/analytic_plan.py`
- `addons/analytic/models/ir_config_parameter.py`
- `addons/analytic/models/res_config_settings.py`
- `addons/analytic/models/res_groups.py`
- `addons/analytic/security/analytic_security.xml`
- `addons/analytic/security/ir.access.csv`
- `addons/analytic/static/src/components/analytic_distribution/analytic_distribution.js`
- `addons/analytic/static/src/components/analytic_distribution/analytic_distribution.scss`
- `addons/analytic/static/src/components/analytic_distribution/analytic_distribution.xml`
- `addons/analytic/static/src/services/batched_orm_service.js`
- `addons/analytic/static/src/services/reload_analytic_plan_service.js`
- `addons/analytic/static/src/views/analytic_search_model.js`
- `addons/analytic/static/src/views/graph/graph_view.js`
- `addons/analytic/static/src/views/kanban/kanban_view.js`
- `addons/analytic/static/src/views/list/list_view.js`
- `addons/analytic/static/src/views/pivot/pivot_renderer.js`
- `addons/analytic/static/src/views/pivot/pivot_view.js`
- `addons/analytic/static/tests/analytic_distribution.test.js`
- `addons/analytic/static/tests/analytic_test_helpers.js`
- `addons/analytic/static/tests/analytic_views.test.js`
- `addons/analytic/static/tests/analytic_widget.test.js`
- `addons/analytic/static/tests/batched_orm_service.test.js`
- `addons/analytic/static/tests/mock_server/mock_models/account_analytic_account.js`
- `addons/analytic/static/tests/mock_server/mock_models/account_analytic_distribution_model.js`
- `addons/analytic/static/tests/mock_server/mock_models/account_analytic_line.js`
- `addons/analytic/static/tests/mock_server/mock_models/account_analytic_plan.js`
- `addons/analytic/tests/__init__.py`
- `addons/analytic/tests/common.py`
- `addons/analytic/tests/test_analytic_account.py`
- `addons/analytic/tests/test_analytic_dynamic_update.py`
- `addons/analytic/tests/test_analytic_mixin.py`
- `addons/analytic/tests/test_plan_operations.py`
- `addons/analytic/views/analytic_account_views.xml`
- `addons/analytic/views/analytic_distribution_model_views.xml`
- `addons/analytic/views/analytic_line_views.xml`
- `addons/analytic/views/analytic_plan_views.xml`
