# Module: barcodes_gs1_nomenclature

- **Module ID:** MOD-033
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/barcodes_gs1_nomenclature`
- **Manifest:** `addons/barcodes_gs1_nomenclature/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Inventory`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Parse barcodes according to the GS1-128 specifications

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 65 files, including 8 Python, 2 XML, and 6 JavaScript/TypeScript files. The manifest declares dependencies: `barcodes`, `uom`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 2
- Browser asset files: 6
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 13 methods, 2 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/barcodes_gs1_nomenclature/models/barcode_nomenclature.py:13`, `addons/barcodes_gs1_nomenclature/models/barcode_rule.py:7`, `addons/barcodes_gs1_nomenclature/models/ir_http.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 6 JavaScript/TypeScript files; static XML analysis found 33 record/template/menu identifiers.
- **Evidence:** `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:4`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:10`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:20`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:30`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:40`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:50`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:60`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:71`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:81`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:92`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:102`, `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml:112`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/barcodes_gs1_nomenclature/tests/__init__.py`, `addons/barcodes_gs1_nomenclature/tests/test_barcodes_gs1_nomenclature.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `default_gs1_nomenclature`, `barcode_rule_gs1_00`, `barcode_rule_gs1_01`, `barcode_rule_gs1_02`, `barcode_rule_gs1_410`, `barcode_rule_gs1_413`, `barcode_rule_gs1_414`, `barcode_rule_gs1_10`, `barcode_rule_gs1_21`, `barcode_rule_gs1_13`, `barcode_rule_gs1_15`, `barcode_rule_gs1_17`, `barcode_rule_gs1_30`, `barcode_rule_gs1_37`, `barcode_rule_gs1_310y`, `barcode_rule_gs1_311y`, `barcode_rule_gs1_314y`, `barcode_rule_gs1_315y`, `barcode_rule_gs1_316y`, `barcode_rule_gs1_320y`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 6; representative evidence: `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:5`, `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:7`, `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:36`, `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:38`, `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:47`, `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml:49`
- Browser assets: 6; representative files: `addons/barcodes_gs1_nomenclature/static/src/js/epc_utils.js`, `addons/barcodes_gs1_nomenclature/static/src/js/barcode_plugin.js`, `addons/barcodes_gs1_nomenclature/static/src/js/epc_model.js`, `addons/barcodes_gs1_nomenclature/static/src/js/barcode_parser.js`, `addons/barcodes_gs1_nomenclature/static/src/js/tests/barcode_parser.test.js`, `addons/barcodes_gs1_nomenclature/static/src/js/tests/epc_utils.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/barcodes_gs1_nomenclature/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `barcode.nomenclature` (addons/barcodes_gs1_nomenclature/models/barcode_nomenclature.py:13); inherits `barcode.rule` (addons/barcodes_gs1_nomenclature/models/barcode_rule.py:7); inherits `ir.http` (addons/barcodes_gs1_nomenclature/models/ir_http.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `barcodes`, `uom`
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

- `addons/barcodes_gs1_nomenclature/__init__.py`
- `addons/barcodes_gs1_nomenclature/__manifest__.py`
- `addons/barcodes_gs1_nomenclature/data/barcodes_gs1_rules.xml`
- `addons/barcodes_gs1_nomenclature/i18n/ar.po`
- `addons/barcodes_gs1_nomenclature/i18n/az.po`
- `addons/barcodes_gs1_nomenclature/i18n/barcodes_gs1_nomenclature.pot`
- `addons/barcodes_gs1_nomenclature/i18n/bg.po`
- `addons/barcodes_gs1_nomenclature/i18n/bs.po`
- `addons/barcodes_gs1_nomenclature/i18n/ca.po`
- `addons/barcodes_gs1_nomenclature/i18n/cs.po`
- `addons/barcodes_gs1_nomenclature/i18n/da.po`
- `addons/barcodes_gs1_nomenclature/i18n/de.po`
- `addons/barcodes_gs1_nomenclature/i18n/el.po`
- `addons/barcodes_gs1_nomenclature/i18n/es.po`
- `addons/barcodes_gs1_nomenclature/i18n/es_419.po`
- `addons/barcodes_gs1_nomenclature/i18n/et.po`
- `addons/barcodes_gs1_nomenclature/i18n/fa.po`
- `addons/barcodes_gs1_nomenclature/i18n/fi.po`
- `addons/barcodes_gs1_nomenclature/i18n/fr.po`
- `addons/barcodes_gs1_nomenclature/i18n/he.po`
- `addons/barcodes_gs1_nomenclature/i18n/hi.po`
- `addons/barcodes_gs1_nomenclature/i18n/hr.po`
- `addons/barcodes_gs1_nomenclature/i18n/hu.po`
- `addons/barcodes_gs1_nomenclature/i18n/id.po`
- `addons/barcodes_gs1_nomenclature/i18n/it.po`
- `addons/barcodes_gs1_nomenclature/i18n/ja.po`
- `addons/barcodes_gs1_nomenclature/i18n/kab.po`
- `addons/barcodes_gs1_nomenclature/i18n/ko.po`
- `addons/barcodes_gs1_nomenclature/i18n/ku.po`
- `addons/barcodes_gs1_nomenclature/i18n/lo.po`
- `addons/barcodes_gs1_nomenclature/i18n/lt.po`
- `addons/barcodes_gs1_nomenclature/i18n/lv.po`
- `addons/barcodes_gs1_nomenclature/i18n/mn.po`
- `addons/barcodes_gs1_nomenclature/i18n/my.po`
- `addons/barcodes_gs1_nomenclature/i18n/nb.po`
- `addons/barcodes_gs1_nomenclature/i18n/nl.po`
- `addons/barcodes_gs1_nomenclature/i18n/pl.po`
- `addons/barcodes_gs1_nomenclature/i18n/pt.po`
- `addons/barcodes_gs1_nomenclature/i18n/pt_BR.po`
- `addons/barcodes_gs1_nomenclature/i18n/ro.po`
- `addons/barcodes_gs1_nomenclature/i18n/ru.po`
- `addons/barcodes_gs1_nomenclature/i18n/sk.po`
- `addons/barcodes_gs1_nomenclature/i18n/sl.po`
- `addons/barcodes_gs1_nomenclature/i18n/sr@latin.po`
- `addons/barcodes_gs1_nomenclature/i18n/sv.po`
- `addons/barcodes_gs1_nomenclature/i18n/th.po`
- `addons/barcodes_gs1_nomenclature/i18n/tr.po`
- `addons/barcodes_gs1_nomenclature/i18n/uk.po`
- `addons/barcodes_gs1_nomenclature/i18n/uz.po`
- `addons/barcodes_gs1_nomenclature/i18n/vi.po`
- `addons/barcodes_gs1_nomenclature/i18n/zh_CN.po`
- `addons/barcodes_gs1_nomenclature/i18n/zh_TW.po`
- `addons/barcodes_gs1_nomenclature/models/__init__.py`
- `addons/barcodes_gs1_nomenclature/models/barcode_nomenclature.py`
- `addons/barcodes_gs1_nomenclature/models/barcode_rule.py`
- `addons/barcodes_gs1_nomenclature/models/ir_http.py`
- `addons/barcodes_gs1_nomenclature/static/src/js/barcode_parser.js`
- `addons/barcodes_gs1_nomenclature/static/src/js/barcode_plugin.js`
- `addons/barcodes_gs1_nomenclature/static/src/js/epc_model.js`
- `addons/barcodes_gs1_nomenclature/static/src/js/epc_utils.js`
- `addons/barcodes_gs1_nomenclature/static/src/js/tests/barcode_parser.test.js`
- `addons/barcodes_gs1_nomenclature/static/src/js/tests/epc_utils.test.js`
- `addons/barcodes_gs1_nomenclature/tests/__init__.py`
- `addons/barcodes_gs1_nomenclature/tests/test_barcodes_gs1_nomenclature.py`
- `addons/barcodes_gs1_nomenclature/views/barcodes_view.xml`
