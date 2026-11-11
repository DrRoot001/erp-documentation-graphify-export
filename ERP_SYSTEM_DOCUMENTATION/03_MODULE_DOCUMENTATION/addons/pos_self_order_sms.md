# Module: pos_self_order_sms

- **Module ID:** MOD-462
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/pos_self_order_sms`
- **Manifest:** `addons/pos_self_order_sms/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Point Of Sale`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Integrates POS Self Order with SMS to send customers order confirmation via SMS.

**Scope evidence:** The module contains 59 files, including 7 Python, 2 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `pos_self_order`, `pos_sms`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 1
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/pos_self_order_sms/models/pos_order.py:11`, `addons/pos_self_order_sms/models/pos_preset.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 1 JavaScript/TypeScript files; static XML analysis found 3 record/template/menu identifiers.
- **Evidence:** `addons/pos_self_order_sms/data/preset_data.xml:3`, `addons/pos_self_order_sms/data/preset_data.xml:6`, `addons/pos_self_order_sms/views/pos_preset_views.xml:3`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/pos_self_order_sms/tests/test_self_order_sms_receipt.py`, `addons/pos_self_order_sms/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `pos_restaurant.pos_takeout_preset`, `pos_restaurant.pos_delivery_preset`, `view_pos_preset_form_inherit_pos_self_order_sms`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 2; representative evidence: `addons/pos_self_order_sms/views/pos_preset_views.xml:5`, `addons/pos_self_order_sms/views/pos_preset_views.xml:7`
- Browser assets: 1; representative files: `addons/pos_self_order_sms/static/src/app/models/pos_preset.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/pos_self_order_sms/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `pos.order` (addons/pos_self_order_sms/models/pos_order.py:11); inherits `pos.preset` (addons/pos_self_order_sms/models/pos_preset.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `pos_self_order`, `pos_sms`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/pos_self_order_sms/__init__.py`
- `addons/pos_self_order_sms/__manifest__.py`
- `addons/pos_self_order_sms/data/preset_data.xml`
- `addons/pos_self_order_sms/i18n/ar.po`
- `addons/pos_self_order_sms/i18n/az.po`
- `addons/pos_self_order_sms/i18n/bg.po`
- `addons/pos_self_order_sms/i18n/bs.po`
- `addons/pos_self_order_sms/i18n/ca.po`
- `addons/pos_self_order_sms/i18n/cs.po`
- `addons/pos_self_order_sms/i18n/da.po`
- `addons/pos_self_order_sms/i18n/de.po`
- `addons/pos_self_order_sms/i18n/el.po`
- `addons/pos_self_order_sms/i18n/es.po`
- `addons/pos_self_order_sms/i18n/es_419.po`
- `addons/pos_self_order_sms/i18n/et.po`
- `addons/pos_self_order_sms/i18n/fa.po`
- `addons/pos_self_order_sms/i18n/fi.po`
- `addons/pos_self_order_sms/i18n/fr.po`
- `addons/pos_self_order_sms/i18n/he.po`
- `addons/pos_self_order_sms/i18n/hi.po`
- `addons/pos_self_order_sms/i18n/hr.po`
- `addons/pos_self_order_sms/i18n/hu.po`
- `addons/pos_self_order_sms/i18n/id.po`
- `addons/pos_self_order_sms/i18n/it.po`
- `addons/pos_self_order_sms/i18n/ja.po`
- `addons/pos_self_order_sms/i18n/kab.po`
- `addons/pos_self_order_sms/i18n/ko.po`
- `addons/pos_self_order_sms/i18n/ku.po`
- `addons/pos_self_order_sms/i18n/lo.po`
- `addons/pos_self_order_sms/i18n/lt.po`
- `addons/pos_self_order_sms/i18n/lv.po`
- `addons/pos_self_order_sms/i18n/mn.po`
- `addons/pos_self_order_sms/i18n/my.po`
- `addons/pos_self_order_sms/i18n/nb.po`
- `addons/pos_self_order_sms/i18n/nl.po`
- `addons/pos_self_order_sms/i18n/pl.po`
- `addons/pos_self_order_sms/i18n/pos_self_order_sms.pot`
- `addons/pos_self_order_sms/i18n/pt.po`
- `addons/pos_self_order_sms/i18n/pt_BR.po`
- `addons/pos_self_order_sms/i18n/ro.po`
- `addons/pos_self_order_sms/i18n/ru.po`
- `addons/pos_self_order_sms/i18n/sk.po`
- `addons/pos_self_order_sms/i18n/sl.po`
- `addons/pos_self_order_sms/i18n/sr@latin.po`
- `addons/pos_self_order_sms/i18n/sv.po`
- `addons/pos_self_order_sms/i18n/th.po`
- `addons/pos_self_order_sms/i18n/tr.po`
- `addons/pos_self_order_sms/i18n/uk.po`
- `addons/pos_self_order_sms/i18n/uz.po`
- `addons/pos_self_order_sms/i18n/vi.po`
- `addons/pos_self_order_sms/i18n/zh_CN.po`
- `addons/pos_self_order_sms/i18n/zh_TW.po`
- `addons/pos_self_order_sms/models/__init__.py`
- `addons/pos_self_order_sms/models/pos_order.py`
- `addons/pos_self_order_sms/models/pos_preset.py`
- `addons/pos_self_order_sms/static/src/app/models/pos_preset.js`
- `addons/pos_self_order_sms/tests/__init__.py`
- `addons/pos_self_order_sms/tests/test_self_order_sms_receipt.py`
- `addons/pos_self_order_sms/views/pos_preset_views.xml`
