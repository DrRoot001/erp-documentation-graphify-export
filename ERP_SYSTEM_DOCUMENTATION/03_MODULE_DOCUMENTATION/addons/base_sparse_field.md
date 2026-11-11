# Module: base_sparse_field

- **Module ID:** MOD-043
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_sparse_field`
- **Manifest:** `addons/base_sparse_field/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Implementation of sparse fields.

**Manifest description:**

The purpose of this module is to implement "sparse" fields, i.e., fields
that are mostly null. This implementation circumvents the PostgreSQL
limitation on the number of columns in a table. The values of all sparse
fields are stored in a "serialized" field in the form of a JSON mapping.

**Scope evidence:** The module contains 71 files, including 7 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `base`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_sparse_field/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 8 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/base_sparse_field/models/models.py:9`, `addons/base_sparse_field/models/models.py:16`, `addons/base_sparse_field/models/models.py:92`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/base_sparse_field/views/views.xml:6`, `addons/base_sparse_field/views/views.xml:19`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_sparse_field/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/base_sparse_field/tests/test_sparse_fields.py`, `addons/base_sparse_field/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: `model_form_view`, `field_form_view`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/base_sparse_field/views/views.xml:7`, `addons/base_sparse_field/views/views.xml:9`, `addons/base_sparse_field/views/views.xml:20`, `addons/base_sparse_field/views/views.xml:22`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_sparse_field/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: inherits `base` (addons/base_sparse_field/models/models.py:9); inherits `ir.model.fields` (addons/base_sparse_field/models/models.py:16); `sparse_fields.test` (addons/base_sparse_field/models/models.py:92)
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

- `addons/base_sparse_field/__init__.py`
- `addons/base_sparse_field/__manifest__.py`
- `addons/base_sparse_field/i18n/af.po`
- `addons/base_sparse_field/i18n/am.po`
- `addons/base_sparse_field/i18n/ar.po`
- `addons/base_sparse_field/i18n/az.po`
- `addons/base_sparse_field/i18n/base_sparse_field.pot`
- `addons/base_sparse_field/i18n/bg.po`
- `addons/base_sparse_field/i18n/bs.po`
- `addons/base_sparse_field/i18n/ca.po`
- `addons/base_sparse_field/i18n/cs.po`
- `addons/base_sparse_field/i18n/da.po`
- `addons/base_sparse_field/i18n/de.po`
- `addons/base_sparse_field/i18n/el.po`
- `addons/base_sparse_field/i18n/es.po`
- `addons/base_sparse_field/i18n/es_419.po`
- `addons/base_sparse_field/i18n/es_CL.po`
- `addons/base_sparse_field/i18n/et.po`
- `addons/base_sparse_field/i18n/eu.po`
- `addons/base_sparse_field/i18n/fa.po`
- `addons/base_sparse_field/i18n/fi.po`
- `addons/base_sparse_field/i18n/fo.po`
- `addons/base_sparse_field/i18n/fr.po`
- `addons/base_sparse_field/i18n/fr_CA.po`
- `addons/base_sparse_field/i18n/gl.po`
- `addons/base_sparse_field/i18n/gu.po`
- `addons/base_sparse_field/i18n/he.po`
- `addons/base_sparse_field/i18n/hi.po`
- `addons/base_sparse_field/i18n/hr.po`
- `addons/base_sparse_field/i18n/hu.po`
- `addons/base_sparse_field/i18n/id.po`
- `addons/base_sparse_field/i18n/is.po`
- `addons/base_sparse_field/i18n/it.po`
- `addons/base_sparse_field/i18n/ja.po`
- `addons/base_sparse_field/i18n/ka.po`
- `addons/base_sparse_field/i18n/kab.po`
- `addons/base_sparse_field/i18n/km.po`
- `addons/base_sparse_field/i18n/ko.po`
- `addons/base_sparse_field/i18n/ku.po`
- `addons/base_sparse_field/i18n/lo.po`
- `addons/base_sparse_field/i18n/lt.po`
- `addons/base_sparse_field/i18n/lv.po`
- `addons/base_sparse_field/i18n/mk.po`
- `addons/base_sparse_field/i18n/mn.po`
- `addons/base_sparse_field/i18n/my.po`
- `addons/base_sparse_field/i18n/nb.po`
- `addons/base_sparse_field/i18n/nl.po`
- `addons/base_sparse_field/i18n/pl.po`
- `addons/base_sparse_field/i18n/pt.po`
- `addons/base_sparse_field/i18n/pt_BR.po`
- `addons/base_sparse_field/i18n/ro.po`
- `addons/base_sparse_field/i18n/ru.po`
- `addons/base_sparse_field/i18n/sk.po`
- `addons/base_sparse_field/i18n/sl.po`
- `addons/base_sparse_field/i18n/sq.po`
- `addons/base_sparse_field/i18n/sr@latin.po`
- `addons/base_sparse_field/i18n/sv.po`
- `addons/base_sparse_field/i18n/th.po`
- `addons/base_sparse_field/i18n/tr.po`
- `addons/base_sparse_field/i18n/uk.po`
- `addons/base_sparse_field/i18n/uz.po`
- `addons/base_sparse_field/i18n/vi.po`
- `addons/base_sparse_field/i18n/zh_CN.po`
- `addons/base_sparse_field/i18n/zh_TW.po`
- `addons/base_sparse_field/models/__init__.py`
- `addons/base_sparse_field/models/fields.py`
- `addons/base_sparse_field/models/models.py`
- `addons/base_sparse_field/security/ir.access.csv`
- `addons/base_sparse_field/tests/__init__.py`
- `addons/base_sparse_field/tests/test_sparse_fields.py`
- `addons/base_sparse_field/views/views.xml`
