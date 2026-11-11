# Module: mass_mailing_sale

- **Module ID:** MOD-369
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/mass_mailing_sale`
- **Manifest:** `addons/mass_mailing_sale/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Marketing/Email Marketing`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Add sale order UTM info on mass mailing

**Manifest description:**

UTM and mass mailing on sale orders

**Scope evidence:** The module contains 63 files, including 6 Python, 5 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `mass_mailing`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 1
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/mass_mailing_sale/models/sale_order.py:7`, `addons/mass_mailing_sale/models/utm.py:7`, `addons/mass_mailing_sale/models/mailing_mailing.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 1 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/mass_mailing_sale/demo/mailing_mailing.xml:4`, `addons/mass_mailing_sale/views/mailing_mailing_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `mass_mailing.mass_mail_sale_order_0`, `mailing_mailing_view_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/mass_mailing_sale/views/mailing_mailing_views.xml:5`, `addons/mass_mailing_sale/views/mailing_mailing_views.xml:7`
- Browser assets: 1; representative files: `addons/mass_mailing_sale/static/src/builder/options/product_snapshot_snippet_info.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/mass_mailing_sale/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `sale.order` (addons/mass_mailing_sale/models/sale_order.py:7); inherits `utm.campaign` (addons/mass_mailing_sale/models/utm.py:7); inherits `mailing.mailing` (addons/mass_mailing_sale/models/mailing_mailing.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `mass_mailing`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/mass_mailing_sale/__init__.py`
- `addons/mass_mailing_sale/__manifest__.py`
- `addons/mass_mailing_sale/demo/mailing_mailing.xml`
- `addons/mass_mailing_sale/i18n/ar.po`
- `addons/mass_mailing_sale/i18n/az.po`
- `addons/mass_mailing_sale/i18n/bg.po`
- `addons/mass_mailing_sale/i18n/bs.po`
- `addons/mass_mailing_sale/i18n/ca.po`
- `addons/mass_mailing_sale/i18n/cs.po`
- `addons/mass_mailing_sale/i18n/da.po`
- `addons/mass_mailing_sale/i18n/de.po`
- `addons/mass_mailing_sale/i18n/el.po`
- `addons/mass_mailing_sale/i18n/es.po`
- `addons/mass_mailing_sale/i18n/es_419.po`
- `addons/mass_mailing_sale/i18n/et.po`
- `addons/mass_mailing_sale/i18n/fa.po`
- `addons/mass_mailing_sale/i18n/fi.po`
- `addons/mass_mailing_sale/i18n/fr.po`
- `addons/mass_mailing_sale/i18n/gu.po`
- `addons/mass_mailing_sale/i18n/he.po`
- `addons/mass_mailing_sale/i18n/hi.po`
- `addons/mass_mailing_sale/i18n/hr.po`
- `addons/mass_mailing_sale/i18n/hu.po`
- `addons/mass_mailing_sale/i18n/id.po`
- `addons/mass_mailing_sale/i18n/is.po`
- `addons/mass_mailing_sale/i18n/it.po`
- `addons/mass_mailing_sale/i18n/ja.po`
- `addons/mass_mailing_sale/i18n/kab.po`
- `addons/mass_mailing_sale/i18n/ko.po`
- `addons/mass_mailing_sale/i18n/ku.po`
- `addons/mass_mailing_sale/i18n/lo.po`
- `addons/mass_mailing_sale/i18n/lt.po`
- `addons/mass_mailing_sale/i18n/lv.po`
- `addons/mass_mailing_sale/i18n/mass_mailing_sale.pot`
- `addons/mass_mailing_sale/i18n/mn.po`
- `addons/mass_mailing_sale/i18n/my.po`
- `addons/mass_mailing_sale/i18n/nb.po`
- `addons/mass_mailing_sale/i18n/nl.po`
- `addons/mass_mailing_sale/i18n/pl.po`
- `addons/mass_mailing_sale/i18n/pt.po`
- `addons/mass_mailing_sale/i18n/pt_BR.po`
- `addons/mass_mailing_sale/i18n/ro.po`
- `addons/mass_mailing_sale/i18n/ru.po`
- `addons/mass_mailing_sale/i18n/sk.po`
- `addons/mass_mailing_sale/i18n/sl.po`
- `addons/mass_mailing_sale/i18n/sr@latin.po`
- `addons/mass_mailing_sale/i18n/sv.po`
- `addons/mass_mailing_sale/i18n/th.po`
- `addons/mass_mailing_sale/i18n/tr.po`
- `addons/mass_mailing_sale/i18n/uk.po`
- `addons/mass_mailing_sale/i18n/uz.po`
- `addons/mass_mailing_sale/i18n/vi.po`
- `addons/mass_mailing_sale/i18n/zh_CN.po`
- `addons/mass_mailing_sale/i18n/zh_TW.po`
- `addons/mass_mailing_sale/models/__init__.py`
- `addons/mass_mailing_sale/models/mailing_mailing.py`
- `addons/mass_mailing_sale/models/sale_order.py`
- `addons/mass_mailing_sale/models/utm.py`
- `addons/mass_mailing_sale/static/src/builder/options/product_snapshot_fragments.xml`
- `addons/mass_mailing_sale/static/src/builder/options/product_snapshot_snippet_info.js`
- `addons/mass_mailing_sale/static/src/snippets/s_product_snapshot.xml`
- `addons/mass_mailing_sale/static/src/snippets/snippet_categories.xml`
- `addons/mass_mailing_sale/views/mailing_mailing_views.xml`
