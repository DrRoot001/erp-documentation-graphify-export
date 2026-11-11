# Module: website_partnership

- **Module ID:** MOD-630
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_partnership`
- **Manifest:** `addons/website_partnership/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Publish your partners on your website

**Manifest description:**

This module allows to publish your members/partners on your website.

To publish a member, set a *Level* in their contact form and click the *Publish* button.

**Scope evidence:** The module contains 65 files, including 7 Python, 7 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `partnership`, `website_partner`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 7
- Browser asset files: 1
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_partnership/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_partnership/models/res_partner_grade.py:6`, `addons/website_partnership/models/website.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/website_partnership/controllers/main.py:106`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 1 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/website_partnership/demo/res_partner_grade_demo.xml:4`, `addons/website_partnership/demo/res_partner_grade_demo.xml:7`, `addons/website_partnership/demo/res_partner_grade_demo.xml:10`, `addons/website_partnership/demo/res_partner_demo.xml:3`, `addons/website_partnership/demo/res_partner_demo.xml:6`, `addons/website_partnership/demo/res_partner_demo.xml:9`, `addons/website_partnership/demo/res_partner_demo.xml:12`, `addons/website_partnership/demo/res_partner_demo.xml:15`, `addons/website_partnership/demo/res_partner_demo.xml:18`, `addons/website_partnership/views/res_config_settings_views.xml:3`, `addons/website_partnership/views/res_partner_grade_views.xml:3`, `addons/website_partnership/views/website_partnership_templates.xml:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_partnership/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `partnership.res_partner_grade_data_gold`, `partnership.res_partner_grade_data_silver`, `partnership.res_partner_grade_data_bronze`, `base.res_partner_3`, `base.res_partner_4`, `base.res_partner_12`, `base.res_partner_10`, `base.res_partner_18`, `base.res_partner_1`, `res_config_settings_view_form`, `view_partner_grade_form`, `Partners Page Layout`, `Find Partners`, `Partner Page`, `Partner Details`, `Search`, `Categories`, `Address`, `Contact Details`, `Companies only`
- Menus: 0; representative evidence: Not found in module
- Templates: 13; representative evidence: `addons/website_partnership/views/website_partnership_templates.xml:5`, `addons/website_partnership/views/website_partnership_templates.xml:20`, `addons/website_partnership/views/website_partnership_templates.xml:115`, `addons/website_partnership/views/website_partnership_templates.xml:129`, `addons/website_partnership/views/website_partnership_templates.xml:144`, `addons/website_partnership/views/website_partnership_templates.xml:164`, `addons/website_partnership/views/website_partnership_templates.xml:185`, `addons/website_partnership/views/website_partnership_templates.xml:197`, `addons/website_partnership/views/website_partnership_templates.xml:203`, `addons/website_partnership/views/website_partnership_templates.xml:209`, `addons/website_partnership/views/website_partnership_templates.xml:215`, `addons/website_partnership/views/website_partnership_templates.xml:221`
- View/action field declarations: 4; representative evidence: `addons/website_partnership/views/res_config_settings_views.xml:5`, `addons/website_partnership/views/res_config_settings_views.xml:8`, `addons/website_partnership/views/res_partner_grade_views.xml:5`, `addons/website_partnership/views/res_partner_grade_views.xml:7`
- Browser assets: 1; representative files: `addons/website_partnership/static/tests/tours/publish.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_partnership/__manifest__.py`
- **HTTP entry points:** `addons/website_partnership/controllers/main.py:106`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: `res.partner.grade` (addons/website_partnership/models/res_partner_grade.py:6); inherits `website` (addons/website_partnership/models/website.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/website_partnership/controllers/main.py:106`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `partnership`, `website_partner`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/website_partnership/__init__.py`
- `addons/website_partnership/__manifest__.py`
- `addons/website_partnership/controllers/__init__.py`
- `addons/website_partnership/controllers/main.py`
- `addons/website_partnership/demo/res_partner_demo.xml`
- `addons/website_partnership/demo/res_partner_grade_demo.xml`
- `addons/website_partnership/i18n/ar.po`
- `addons/website_partnership/i18n/az.po`
- `addons/website_partnership/i18n/bg.po`
- `addons/website_partnership/i18n/bs.po`
- `addons/website_partnership/i18n/ca.po`
- `addons/website_partnership/i18n/cs.po`
- `addons/website_partnership/i18n/da.po`
- `addons/website_partnership/i18n/de.po`
- `addons/website_partnership/i18n/el.po`
- `addons/website_partnership/i18n/es.po`
- `addons/website_partnership/i18n/es_419.po`
- `addons/website_partnership/i18n/et.po`
- `addons/website_partnership/i18n/fa.po`
- `addons/website_partnership/i18n/fi.po`
- `addons/website_partnership/i18n/fr.po`
- `addons/website_partnership/i18n/he.po`
- `addons/website_partnership/i18n/hi.po`
- `addons/website_partnership/i18n/hr.po`
- `addons/website_partnership/i18n/hu.po`
- `addons/website_partnership/i18n/id.po`
- `addons/website_partnership/i18n/it.po`
- `addons/website_partnership/i18n/ja.po`
- `addons/website_partnership/i18n/kab.po`
- `addons/website_partnership/i18n/ko.po`
- `addons/website_partnership/i18n/ku.po`
- `addons/website_partnership/i18n/lo.po`
- `addons/website_partnership/i18n/lt.po`
- `addons/website_partnership/i18n/lv.po`
- `addons/website_partnership/i18n/mn.po`
- `addons/website_partnership/i18n/my.po`
- `addons/website_partnership/i18n/nb.po`
- `addons/website_partnership/i18n/nl.po`
- `addons/website_partnership/i18n/pl.po`
- `addons/website_partnership/i18n/pt.po`
- `addons/website_partnership/i18n/pt_BR.po`
- `addons/website_partnership/i18n/ro.po`
- `addons/website_partnership/i18n/ru.po`
- `addons/website_partnership/i18n/sk.po`
- `addons/website_partnership/i18n/sl.po`
- `addons/website_partnership/i18n/sr@latin.po`
- `addons/website_partnership/i18n/sv.po`
- `addons/website_partnership/i18n/th.po`
- `addons/website_partnership/i18n/tr.po`
- `addons/website_partnership/i18n/uk.po`
- `addons/website_partnership/i18n/uz.po`
- `addons/website_partnership/i18n/vi.po`
- `addons/website_partnership/i18n/website_partnership.pot`
- `addons/website_partnership/i18n/zh_CN.po`
- `addons/website_partnership/i18n/zh_TW.po`
- `addons/website_partnership/models/__init__.py`
- `addons/website_partnership/models/res_partner_grade.py`
- `addons/website_partnership/models/website.py`
- `addons/website_partnership/security/ir.access.csv`
- `addons/website_partnership/static/src/website_builder/partner_page_option.xml`
- `addons/website_partnership/static/src/website_builder/website_partnership_option.xml`
- `addons/website_partnership/static/tests/tours/publish.js`
- `addons/website_partnership/views/res_config_settings_views.xml`
- `addons/website_partnership/views/res_partner_grade_views.xml`
- `addons/website_partnership/views/website_partnership_templates.xml`
