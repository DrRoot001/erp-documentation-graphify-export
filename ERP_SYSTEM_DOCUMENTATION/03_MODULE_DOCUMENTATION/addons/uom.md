# Module: uom

- **Module ID:** MOD-590
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/uom`
- **Manifest:** `addons/uom/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

This is the base module for managing Units of measure.
========================================================================

**Scope evidence:** The module contains 69 files, including 8 Python, 5 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 5
- Browser asset files: 2
- Security files: 2
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/uom/security/ir.access.csv`, `addons/uom/security/uom_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 22 methods, 1 constraint handlers, 1 onchange handlers, and 3 dependency declarations.
- **Evidence:** `addons/uom/models/uom_uom.py:17`, `addons/uom/models/res_groups.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 5 XML files and 2 JavaScript/TypeScript files; static XML analysis found 36 record/template/menu identifiers.
- **Evidence:** `addons/uom/security/uom_security.xml:4`, `addons/uom/data/uom_data.xml:5`, `addons/uom/data/uom_data.xml:12`, `addons/uom/data/uom_data.xml:16`, `addons/uom/data/uom_data.xml:21`, `addons/uom/data/uom_data.xml:29`, `addons/uom/data/uom_data.xml:33`, `addons/uom/data/uom_data.xml:38`, `addons/uom/data/uom_data.xml:45`, `addons/uom/data/uom_data.xml:49`, `addons/uom/data/uom_data.xml:55`, `addons/uom/data/uom_data.xml:60`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/uom/security/ir.access.csv`, `addons/uom/security/uom_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/uom/tests/test_uom.py`, `addons/uom/tests/common.py`, `addons/uom/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 5; representative identifiers: `group_uom`, `decimal_product_uom`, `product_uom_unit`, `product_uom_pack_6`, `product_uom_dozen`, `product_uom_hour`, `product_uom_day`, `product_uom_minute`, `product_uom_millimeter`, `product_uom_cm`, `product_uom_meter`, `product_uom_km`, `product_uom_square_meter`, `product_uom_milliliter`, `product_uom_litre`, `product_uom_cubic_meter`, `product_uom_gram`, `product_uom_kgm`, `product_uom_ton`, `product_uom_oz`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 7; representative evidence: `addons/uom/views/uom_uom_views.xml:5`, `addons/uom/views/uom_uom_views.xml:6`, `addons/uom/views/uom_uom_views.xml:18`, `addons/uom/views/uom_uom_views.xml:19`, `addons/uom/views/uom_uom_views.xml:39`, `addons/uom/views/uom_uom_views.xml:40`, `addons/uom/views/uom_uom_views.xml:53`
- Browser assets: 2; representative files: `addons/uom/static/src/components/many2one_uom/many2one_uom_field.js`, `addons/uom/static/src/components/many2x_uom_tags/many2x_uom_tags.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/uom/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: `uom.uom` (addons/uom/models/uom_uom.py:17); inherits `res.groups` (addons/uom/models/res_groups.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `base`
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

- `addons/uom/__init__.py`
- `addons/uom/__manifest__.py`
- `addons/uom/data/uom_data.xml`
- `addons/uom/i18n/ar.po`
- `addons/uom/i18n/az.po`
- `addons/uom/i18n/bg.po`
- `addons/uom/i18n/bs.po`
- `addons/uom/i18n/ca.po`
- `addons/uom/i18n/cs.po`
- `addons/uom/i18n/da.po`
- `addons/uom/i18n/de.po`
- `addons/uom/i18n/el.po`
- `addons/uom/i18n/es.po`
- `addons/uom/i18n/es_419.po`
- `addons/uom/i18n/et.po`
- `addons/uom/i18n/fa.po`
- `addons/uom/i18n/fi.po`
- `addons/uom/i18n/fr.po`
- `addons/uom/i18n/gu.po`
- `addons/uom/i18n/he.po`
- `addons/uom/i18n/hi.po`
- `addons/uom/i18n/hr.po`
- `addons/uom/i18n/hu.po`
- `addons/uom/i18n/id.po`
- `addons/uom/i18n/is.po`
- `addons/uom/i18n/it.po`
- `addons/uom/i18n/ja.po`
- `addons/uom/i18n/kab.po`
- `addons/uom/i18n/km.po`
- `addons/uom/i18n/ko.po`
- `addons/uom/i18n/ku.po`
- `addons/uom/i18n/lo.po`
- `addons/uom/i18n/lt.po`
- `addons/uom/i18n/lv.po`
- `addons/uom/i18n/mn.po`
- `addons/uom/i18n/my.po`
- `addons/uom/i18n/nb.po`
- `addons/uom/i18n/nl.po`
- `addons/uom/i18n/pl.po`
- `addons/uom/i18n/pt.po`
- `addons/uom/i18n/pt_BR.po`
- `addons/uom/i18n/ro.po`
- `addons/uom/i18n/ru.po`
- `addons/uom/i18n/sk.po`
- `addons/uom/i18n/sl.po`
- `addons/uom/i18n/sr@latin.po`
- `addons/uom/i18n/sv.po`
- `addons/uom/i18n/th.po`
- `addons/uom/i18n/tr.po`
- `addons/uom/i18n/uk.po`
- `addons/uom/i18n/uom.pot`
- `addons/uom/i18n/uz.po`
- `addons/uom/i18n/vi.po`
- `addons/uom/i18n/zh_CN.po`
- `addons/uom/i18n/zh_TW.po`
- `addons/uom/models/__init__.py`
- `addons/uom/models/res_groups.py`
- `addons/uom/models/uom_uom.py`
- `addons/uom/security/ir.access.csv`
- `addons/uom/security/uom_security.xml`
- `addons/uom/static/src/components/many2one_uom/many2one_uom_field.js`
- `addons/uom/static/src/components/many2one_uom/many2one_uom_field.scss`
- `addons/uom/static/src/components/many2one_uom/many2one_uom_field.xml`
- `addons/uom/static/src/components/many2x_uom_tags/many2x_uom_tags.js`
- `addons/uom/static/src/components/many2x_uom_tags/many2x_uom_tags.xml`
- `addons/uom/tests/__init__.py`
- `addons/uom/tests/common.py`
- `addons/uom/tests/test_uom.py`
- `addons/uom/views/uom_uom_views.xml`
