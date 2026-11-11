# Module: barcodes

- **Module ID:** MOD-032
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/barcodes`
- **Manifest:** `addons/barcodes/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Scan and Parse Barcodes

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 98 files, including 9 Python, 7 XML, and 11 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 7
- Browser asset files: 11
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/barcodes/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 20 methods, 1 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/barcodes/models/barcode_nomenclature.py:16`, `addons/barcodes/models/barcode_rule.py:7`, `addons/barcodes/models/ir_http.py:7`, `addons/barcodes/models/res_company.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 7 XML files and 11 JavaScript/TypeScript files; static XML analysis found 7 record/template/menu identifiers.
- **Evidence:** `addons/barcodes/data/barcodes_data.xml:3`, `addons/barcodes/data/barcodes_data.xml:7`, `addons/barcodes/views/res_partner_views.xml:3`, `addons/barcodes/views/barcodes_view.xml:4`, `addons/barcodes/views/barcodes_view.xml:43`, `addons/barcodes/views/barcodes_view.xml:53`, `addons/barcodes/views/barcodes_view.xml:66`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/barcodes/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/barcodes/tests/test_barcode_nomenclature.py`, `addons/barcodes/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 7; representative identifiers: `default_barcode_nomenclature`, `barcode_rule_product`, `view_partner_barcodes_form`, `view_barcode_nomenclature_form`, `view_barcode_nomenclature_tree`, `action_barcode_nomenclature_form`, `view_barcode_rule_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 10; representative evidence: `addons/barcodes/views/res_partner_views.xml:5`, `addons/barcodes/views/res_partner_views.xml:10`, `addons/barcodes/views/barcodes_view.xml:6`, `addons/barcodes/views/barcodes_view.xml:7`, `addons/barcodes/views/barcodes_view.xml:45`, `addons/barcodes/views/barcodes_view.xml:46`, `addons/barcodes/views/barcodes_view.xml:55`, `addons/barcodes/views/barcodes_view.xml:56`, `addons/barcodes/views/barcodes_view.xml:68`, `addons/barcodes/views/barcodes_view.xml:69`
- Browser assets: 11; representative files: `addons/barcodes/static/src/barcode_handlers.js`, `addons/barcodes/static/src/barcode_plugin.js`, `addons/barcodes/static/tests/barcode_scan.test.js`, `addons/barcodes/static/tests/barcode_parser.test.js`, `addons/barcodes/static/tests/barcode_mobile.test.js`, `addons/barcodes/static/tests/barcode.test.js`, `addons/barcodes/static/src/js/barcode_parser.js`, `addons/barcodes/static/src/components/barcode_input.js`, `addons/barcodes/static/src/components/barcode_view.js`, `addons/barcodes/static/src/components/barcode_scanner.js`, `addons/barcodes/static/src/components/manual_barcode.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/barcodes/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: `barcode.nomenclature` (addons/barcodes/models/barcode_nomenclature.py:16); `barcode.rule` (addons/barcodes/models/barcode_rule.py:7); inherits `ir.http` (addons/barcodes/models/ir_http.py:7); inherits `res.company` (addons/barcodes/models/res_company.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/barcodes/__init__.py`
- `addons/barcodes/__manifest__.py`
- `addons/barcodes/data/barcodes_data.xml`
- `addons/barcodes/i18n/af.po`
- `addons/barcodes/i18n/am.po`
- `addons/barcodes/i18n/ar.po`
- `addons/barcodes/i18n/az.po`
- `addons/barcodes/i18n/barcodes.pot`
- `addons/barcodes/i18n/bg.po`
- `addons/barcodes/i18n/bs.po`
- `addons/barcodes/i18n/ca.po`
- `addons/barcodes/i18n/cs.po`
- `addons/barcodes/i18n/da.po`
- `addons/barcodes/i18n/de.po`
- `addons/barcodes/i18n/el.po`
- `addons/barcodes/i18n/es.po`
- `addons/barcodes/i18n/es_419.po`
- `addons/barcodes/i18n/es_CL.po`
- `addons/barcodes/i18n/et.po`
- `addons/barcodes/i18n/eu.po`
- `addons/barcodes/i18n/fa.po`
- `addons/barcodes/i18n/fi.po`
- `addons/barcodes/i18n/fo.po`
- `addons/barcodes/i18n/fr.po`
- `addons/barcodes/i18n/fr_BE.po`
- `addons/barcodes/i18n/fr_CA.po`
- `addons/barcodes/i18n/gl.po`
- `addons/barcodes/i18n/gu.po`
- `addons/barcodes/i18n/he.po`
- `addons/barcodes/i18n/hi.po`
- `addons/barcodes/i18n/hr.po`
- `addons/barcodes/i18n/hu.po`
- `addons/barcodes/i18n/id.po`
- `addons/barcodes/i18n/is.po`
- `addons/barcodes/i18n/it.po`
- `addons/barcodes/i18n/ja.po`
- `addons/barcodes/i18n/ka.po`
- `addons/barcodes/i18n/kab.po`
- `addons/barcodes/i18n/km.po`
- `addons/barcodes/i18n/ko.po`
- `addons/barcodes/i18n/ku.po`
- `addons/barcodes/i18n/lo.po`
- `addons/barcodes/i18n/lt.po`
- `addons/barcodes/i18n/lv.po`
- `addons/barcodes/i18n/mk.po`
- `addons/barcodes/i18n/mn.po`
- `addons/barcodes/i18n/my.po`
- `addons/barcodes/i18n/nb.po`
- `addons/barcodes/i18n/nl.po`
- `addons/barcodes/i18n/pl.po`
- `addons/barcodes/i18n/pt.po`
- `addons/barcodes/i18n/pt_BR.po`
- `addons/barcodes/i18n/ro.po`
- `addons/barcodes/i18n/ru.po`
- `addons/barcodes/i18n/sk.po`
- `addons/barcodes/i18n/sl.po`
- `addons/barcodes/i18n/sq.po`
- `addons/barcodes/i18n/sr@latin.po`
- `addons/barcodes/i18n/sv.po`
- `addons/barcodes/i18n/ta.po`
- `addons/barcodes/i18n/th.po`
- `addons/barcodes/i18n/tr.po`
- `addons/barcodes/i18n/uk.po`
- `addons/barcodes/i18n/uz.po`
- `addons/barcodes/i18n/vi.po`
- `addons/barcodes/i18n/zh_CN.po`
- `addons/barcodes/i18n/zh_TW.po`
- `addons/barcodes/models/__init__.py`
- `addons/barcodes/models/barcode_nomenclature.py`
- `addons/barcodes/models/barcode_rule.py`
- `addons/barcodes/models/ir_http.py`
- `addons/barcodes/models/res_company.py`
- `addons/barcodes/security/ir.access.csv`
- `addons/barcodes/static/img/barcode.png`
- `addons/barcodes/static/src/audio/error.mp3`
- `addons/barcodes/static/src/audio/error.ogg`
- `addons/barcodes/static/src/barcode_handlers.js`
- `addons/barcodes/static/src/barcode_plugin.js`
- `addons/barcodes/static/src/components/barcode_input.js`
- `addons/barcodes/static/src/components/barcode_input.scss`
- `addons/barcodes/static/src/components/barcode_input.xml`
- `addons/barcodes/static/src/components/barcode_scanner.js`
- `addons/barcodes/static/src/components/barcode_scanner.scss`
- `addons/barcodes/static/src/components/barcode_scanner.xml`
- `addons/barcodes/static/src/components/barcode_view.js`
- `addons/barcodes/static/src/components/barcode_view.scss`
- `addons/barcodes/static/src/components/barcode_view.xml`
- `addons/barcodes/static/src/components/manual_barcode.js`
- `addons/barcodes/static/src/components/manual_barcode.xml`
- `addons/barcodes/static/src/js/barcode_parser.js`
- `addons/barcodes/static/tests/barcode.test.js`
- `addons/barcodes/static/tests/barcode_mobile.test.js`
- `addons/barcodes/static/tests/barcode_parser.test.js`
- `addons/barcodes/static/tests/barcode_scan.test.js`
- `addons/barcodes/tests/__init__.py`
- `addons/barcodes/tests/test_barcode_nomenclature.py`
- `addons/barcodes/views/barcodes_view.xml`
- `addons/barcodes/views/res_partner_views.xml`
