# Module: partnership

- **Module ID:** MOD-391
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/partnership`
- **Manifest:** `addons/partnership/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/CRM`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This module allows you to manage all operations for managing memberships and partnerships.
==========================================================================================

You can easily assign grade to members/partners, with a specific pricelist.

**Scope evidence:** The module contains 71 files, including 13 Python, 7 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `crm`, `sale`.

## 2. Module structure

- Model/business logic files: 7
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 0
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/partnership/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 7 model declarations, 13 methods, 1 constraint handlers, 1 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/partnership/models/res_partner_grade.py:6`, `addons/partnership/models/res_partner.py:7`, `addons/partnership/models/sale_order.py:7`, `addons/partnership/models/product_template.py:6`, `addons/partnership/models/res_config_settings.py:6`, `addons/partnership/models/product_pricelist.py:6`, `addons/partnership/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 0 JavaScript/TypeScript files; static XML analysis found 17 record/template/menu identifiers.
- **Evidence:** `addons/partnership/data/res_partner_grade_data.xml:3`, `addons/partnership/data/res_partner_grade_data.xml:7`, `addons/partnership/data/res_partner_grade_data.xml:11`, `addons/partnership/views/res_config_settings_views.xml:3`, `addons/partnership/views/res_partner_grade_views.xml:3`, `addons/partnership/views/res_partner_grade_views.xml:14`, `addons/partnership/views/res_partner_grade_views.xml:26`, `addons/partnership/views/res_partner_grade_views.xml:39`, `addons/partnership/views/product_pricelist_views.xml:3`, `addons/partnership/views/partnership_menu.xml:3`, `addons/partnership/views/partnership_menu.xml:8`, `addons/partnership/views/product_template_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/partnership/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/partnership/tests/test_partnership.py`, `addons/partnership/tests/common.py`, `addons/partnership/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `res_partner_grade_data_gold`, `res_partner_grade_data_silver`, `res_partner_grade_data_bronze`, `res_config_settings_view_form`, `view_partner_grade_tree`, `res_partner_grade_view_search`, `res_partner_grade_action`, `view_partner_grade_form`, `view_partner_pricelist_form`, `crm_menu_partners`, `menu_res_partner_grade_action`, `product_template_form_view`, `action_pricelist_partners`, `action_grade_partners`, `view_res_partner_filter_assign`, `view_res_partner_grade_tree`, `view_res_partner_form`
- Menus: 1; representative evidence: `addons/partnership/views/partnership_menu.xml:8`
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 23; representative evidence: `addons/partnership/views/res_config_settings_views.xml:5`, `addons/partnership/views/res_config_settings_views.xml:8`, `addons/partnership/views/res_partner_grade_views.xml:5`, `addons/partnership/views/res_partner_grade_views.xml:6`, `addons/partnership/views/res_partner_grade_views.xml:16`, `addons/partnership/views/res_partner_grade_views.xml:17`, `addons/partnership/views/res_partner_grade_views.xml:28`, `addons/partnership/views/res_partner_grade_views.xml:41`, `addons/partnership/views/res_partner_grade_views.xml:42`, `addons/partnership/views/product_pricelist_views.xml:5`, `addons/partnership/views/product_pricelist_views.xml:7`, `addons/partnership/views/product_template_views.xml:5`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/partnership/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 7
- Representative model evidence: `res.partner.grade` (addons/partnership/models/res_partner_grade.py:6); inherits `res.partner` (addons/partnership/models/res_partner.py:7); inherits `sale.order` (addons/partnership/models/sale_order.py:7); inherits `product.template` (addons/partnership/models/product_template.py:6); inherits `res.config.settings` (addons/partnership/models/res_config_settings.py:6); inherits `product.pricelist` (addons/partnership/models/product_pricelist.py:6); inherits `res.company` (addons/partnership/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `crm`, `sale`
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

- `addons/partnership/__init__.py`
- `addons/partnership/__manifest__.py`
- `addons/partnership/data/res_partner_grade_data.xml`
- `addons/partnership/i18n/ar.po`
- `addons/partnership/i18n/az.po`
- `addons/partnership/i18n/bg.po`
- `addons/partnership/i18n/bs.po`
- `addons/partnership/i18n/ca.po`
- `addons/partnership/i18n/cs.po`
- `addons/partnership/i18n/da.po`
- `addons/partnership/i18n/de.po`
- `addons/partnership/i18n/el.po`
- `addons/partnership/i18n/es.po`
- `addons/partnership/i18n/es_419.po`
- `addons/partnership/i18n/et.po`
- `addons/partnership/i18n/fa.po`
- `addons/partnership/i18n/fi.po`
- `addons/partnership/i18n/fr.po`
- `addons/partnership/i18n/he.po`
- `addons/partnership/i18n/hi.po`
- `addons/partnership/i18n/hr.po`
- `addons/partnership/i18n/hu.po`
- `addons/partnership/i18n/id.po`
- `addons/partnership/i18n/it.po`
- `addons/partnership/i18n/ja.po`
- `addons/partnership/i18n/kab.po`
- `addons/partnership/i18n/ko.po`
- `addons/partnership/i18n/ku.po`
- `addons/partnership/i18n/lo.po`
- `addons/partnership/i18n/lt.po`
- `addons/partnership/i18n/lv.po`
- `addons/partnership/i18n/mn.po`
- `addons/partnership/i18n/my.po`
- `addons/partnership/i18n/nb.po`
- `addons/partnership/i18n/nl.po`
- `addons/partnership/i18n/partnership.pot`
- `addons/partnership/i18n/pl.po`
- `addons/partnership/i18n/pt.po`
- `addons/partnership/i18n/pt_BR.po`
- `addons/partnership/i18n/ro.po`
- `addons/partnership/i18n/ru.po`
- `addons/partnership/i18n/sk.po`
- `addons/partnership/i18n/sl.po`
- `addons/partnership/i18n/sr@latin.po`
- `addons/partnership/i18n/sv.po`
- `addons/partnership/i18n/th.po`
- `addons/partnership/i18n/tr.po`
- `addons/partnership/i18n/uk.po`
- `addons/partnership/i18n/uz.po`
- `addons/partnership/i18n/vi.po`
- `addons/partnership/i18n/zh_CN.po`
- `addons/partnership/i18n/zh_TW.po`
- `addons/partnership/models/__init__.py`
- `addons/partnership/models/product_pricelist.py`
- `addons/partnership/models/product_template.py`
- `addons/partnership/models/res_company.py`
- `addons/partnership/models/res_config_settings.py`
- `addons/partnership/models/res_partner.py`
- `addons/partnership/models/res_partner_grade.py`
- `addons/partnership/models/sale_order.py`
- `addons/partnership/security/ir.access.csv`
- `addons/partnership/static/description/icon.png`
- `addons/partnership/tests/__init__.py`
- `addons/partnership/tests/common.py`
- `addons/partnership/tests/test_partnership.py`
- `addons/partnership/views/partnership_menu.xml`
- `addons/partnership/views/product_pricelist_views.xml`
- `addons/partnership/views/product_template_views.xml`
- `addons/partnership/views/res_config_settings_views.xml`
- `addons/partnership/views/res_partner_grade_views.xml`
- `addons/partnership/views/res_partner_views.xml`
