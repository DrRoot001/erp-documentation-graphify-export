# Module: website_customer

- **Module ID:** MOD-605
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/website_customer`
- **Manifest:** `addons/website_customer/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Website/Website`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Publish your customer references

**Manifest description:**

Publish your customers as business references on your website to attract new potential prospects.

**Scope evidence:** The module contains 84 files, including 9 Python, 4 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `website_crm_partner_assign`, `website_partner`, `website_google_map`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 1
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/website_customer/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 9 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/website_customer/models/res_partner.py:7`, `addons/website_customer/models/res_partner.py:23`, `addons/website_customer/models/website.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 2 route declarations.
- **Evidence:** `addons/website_customer/controllers/main.py:54`, `addons/website_customer/controllers/main.py:165`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 1 JavaScript/TypeScript files; static XML analysis found 21 record/template/menu identifiers.
- **Evidence:** `addons/website_customer/data/res_partner_demo.xml:5`, `addons/website_customer/data/res_partner_demo.xml:35`, `addons/website_customer/data/res_partner_demo.xml:63`, `addons/website_customer/data/res_partner_demo.xml:93`, `addons/website_customer/views/website_customer_templates.xml:4`, `addons/website_customer/views/website_customer_templates.xml:165`, `addons/website_customer/views/website_customer_templates.xml:194`, `addons/website_customer/views/website_customer_templates.xml:214`, `addons/website_customer/views/website_customer_templates.xml:237`, `addons/website_customer/views/website_customer_templates.xml:251`, `addons/website_customer/views/website_customer_templates.xml:273`, `addons/website_customer/views/website_customer_templates.xml:284`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/website_customer/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/website_customer/tests/test_website_customers_technical_page.py`, `addons/website_customer/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `base.res_partner_2`, `base.res_partner_3`, `base.res_partner_4`, `base.res_partner_3`, `Our References`, `Show Map`, `Filter on Industry`, `Filter on Countries`, `Filter on Tags`, `Customer Detail`, `Partner Detail Columns`, `Partner Details`, `Partner Implemented By Block`, `Partner References Block`, `Partner References Block`, `view_partners_form_website`, `view_partner_tag_form`, `view_partner_tag_list`, `res_partner_tag_view_search`, `action_partner_tag_form`
- Menus: 1; representative evidence: `addons/website_customer/views/res_partner_views.xml:71`
- Templates: 11; representative evidence: `addons/website_customer/views/website_customer_templates.xml:4`, `addons/website_customer/views/website_customer_templates.xml:165`, `addons/website_customer/views/website_customer_templates.xml:194`, `addons/website_customer/views/website_customer_templates.xml:214`, `addons/website_customer/views/website_customer_templates.xml:237`, `addons/website_customer/views/website_customer_templates.xml:251`, `addons/website_customer/views/website_customer_templates.xml:273`, `addons/website_customer/views/website_customer_templates.xml:284`, `addons/website_customer/views/website_customer_templates.xml:292`, `addons/website_customer/views/website_customer_templates.xml:315`, `addons/website_customer/views/website_customer_templates.xml:341`
- View/action field declarations: 9; representative evidence: `addons/website_customer/views/res_partner_views.xml:5`, `addons/website_customer/views/res_partner_views.xml:7`, `addons/website_customer/views/res_partner_views.xml:18`, `addons/website_customer/views/res_partner_views.xml:19`, `addons/website_customer/views/res_partner_views.xml:35`, `addons/website_customer/views/res_partner_views.xml:37`, `addons/website_customer/views/res_partner_views.xml:48`, `addons/website_customer/views/res_partner_views.xml:49`, `addons/website_customer/views/res_partner_views.xml:60`
- Browser assets: 1; representative files: `addons/website_customer/static/src/website_builder/customer_filter_option.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/website_customer/__manifest__.py`
- **HTTP entry points:** `addons/website_customer/controllers/main.py:54`, `addons/website_customer/controllers/main.py:165`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `res.partner` (addons/website_customer/models/res_partner.py:7); `res.partner.tag` (addons/website_customer/models/res_partner.py:23); inherits `website` (addons/website_customer/models/website.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 2
- Route evidence: `addons/website_customer/controllers/main.py:54`, `addons/website_customer/controllers/main.py:165`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `website_crm_partner_assign`, `website_partner`, `website_google_map`
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

- `addons/website_customer/__init__.py`
- `addons/website_customer/__manifest__.py`
- `addons/website_customer/controllers/__init__.py`
- `addons/website_customer/controllers/main.py`
- `addons/website_customer/data/res_partner_demo.xml`
- `addons/website_customer/i18n/af.po`
- `addons/website_customer/i18n/am.po`
- `addons/website_customer/i18n/ar.po`
- `addons/website_customer/i18n/az.po`
- `addons/website_customer/i18n/bg.po`
- `addons/website_customer/i18n/bs.po`
- `addons/website_customer/i18n/ca.po`
- `addons/website_customer/i18n/cs.po`
- `addons/website_customer/i18n/da.po`
- `addons/website_customer/i18n/de.po`
- `addons/website_customer/i18n/el.po`
- `addons/website_customer/i18n/es.po`
- `addons/website_customer/i18n/es_419.po`
- `addons/website_customer/i18n/es_CL.po`
- `addons/website_customer/i18n/et.po`
- `addons/website_customer/i18n/eu.po`
- `addons/website_customer/i18n/fa.po`
- `addons/website_customer/i18n/fi.po`
- `addons/website_customer/i18n/fo.po`
- `addons/website_customer/i18n/fr.po`
- `addons/website_customer/i18n/fr_BE.po`
- `addons/website_customer/i18n/fr_CA.po`
- `addons/website_customer/i18n/gl.po`
- `addons/website_customer/i18n/gu.po`
- `addons/website_customer/i18n/he.po`
- `addons/website_customer/i18n/hi.po`
- `addons/website_customer/i18n/hr.po`
- `addons/website_customer/i18n/hu.po`
- `addons/website_customer/i18n/id.po`
- `addons/website_customer/i18n/is.po`
- `addons/website_customer/i18n/it.po`
- `addons/website_customer/i18n/ja.po`
- `addons/website_customer/i18n/ka.po`
- `addons/website_customer/i18n/kab.po`
- `addons/website_customer/i18n/kk.po`
- `addons/website_customer/i18n/km.po`
- `addons/website_customer/i18n/ko.po`
- `addons/website_customer/i18n/ku.po`
- `addons/website_customer/i18n/lo.po`
- `addons/website_customer/i18n/lt.po`
- `addons/website_customer/i18n/lv.po`
- `addons/website_customer/i18n/mk.po`
- `addons/website_customer/i18n/ml_IN.po`
- `addons/website_customer/i18n/mn.po`
- `addons/website_customer/i18n/my.po`
- `addons/website_customer/i18n/nb.po`
- `addons/website_customer/i18n/nl.po`
- `addons/website_customer/i18n/pl.po`
- `addons/website_customer/i18n/pt.po`
- `addons/website_customer/i18n/pt_BR.po`
- `addons/website_customer/i18n/ro.po`
- `addons/website_customer/i18n/ru.po`
- `addons/website_customer/i18n/sk.po`
- `addons/website_customer/i18n/sl.po`
- `addons/website_customer/i18n/sq.po`
- `addons/website_customer/i18n/sr@latin.po`
- `addons/website_customer/i18n/sv.po`
- `addons/website_customer/i18n/ta.po`
- `addons/website_customer/i18n/th.po`
- `addons/website_customer/i18n/tr.po`
- `addons/website_customer/i18n/uk.po`
- `addons/website_customer/i18n/uz.po`
- `addons/website_customer/i18n/vi.po`
- `addons/website_customer/i18n/website_customer.pot`
- `addons/website_customer/i18n/zh_CN.po`
- `addons/website_customer/i18n/zh_TW.po`
- `addons/website_customer/models/__init__.py`
- `addons/website_customer/models/res_partner.py`
- `addons/website_customer/models/website.py`
- `addons/website_customer/security/ir.access.csv`
- `addons/website_customer/static/description/icon.png`
- `addons/website_customer/static/description/icon.svg`
- `addons/website_customer/static/description/icon_hi.png`
- `addons/website_customer/static/src/website_builder/customer_filter_option.js`
- `addons/website_customer/static/src/website_builder/customer_filter_option.xml`
- `addons/website_customer/tests/__init__.py`
- `addons/website_customer/tests/test_website_customers_technical_page.py`
- `addons/website_customer/views/res_partner_views.xml`
- `addons/website_customer/views/website_customer_templates.xml`
