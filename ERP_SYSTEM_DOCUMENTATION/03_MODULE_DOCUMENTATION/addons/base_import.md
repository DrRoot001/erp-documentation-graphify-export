# Module: base_import

- **Module ID:** MOD-037
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/base_import`
- **Manifest:** `addons/base_import/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

New extensible file import for Odoo
======================================

Re-implement Odoo's file import system:

* Server side, the previous system forces most of the logic into the
  client which duplicates the effort (between clients), makes the
  import system much harder to use without a client (direct RPC or
  other forms of automation) and makes knowledge about the
  import/export system much harder to gather as it is spread over
  3+ different projects.

* In a more extensible manner, so users and partners can build their
  own front-end to import from other file formats (e.g. OpenDocument
  files) which may be simpler to handle in their work flow or from
  their data production sources.

* In a module, so that administrators and users of Odoo who do not
  need or want an online import can avoid it being available to users.

**Scope evidence:** The module contains 103 files, including 7 Python, 8 XML, and 12 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 8
- Browser asset files: 12
- Security files: 1
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/base_import/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 39 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/base_import/models/base_import.py:83`, `addons/base_import/models/base_import.py:97`, `addons/base_import/models/base_import.py:117`, `addons/base_import/models/base_import.py:130`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/base_import/controllers/main.py:12`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 12 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/base_import/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 12; representative files: `addons/base_import/static/src/binary_file_manager.js`, `addons/base_import/static/src/import_model.js`, `addons/base_import/static/src/import_block_ui.js`, `addons/base_import/static/tests/import_records.test.js`, `addons/base_import/static/tests/import_action.test.js`, `addons/base_import/static/src/import_records/import_records.js`, `addons/base_import/static/src/import_data_options/import_data_options.js`, `addons/base_import/static/src/import_data_content/import_data_content.js`, `addons/base_import/static/src/import_data_column_error/import_data_column_error.js`, `addons/base_import/static/src/import_data_sidepanel/import_data_sidepanel.js`, `addons/base_import/static/src/import_action/import_action.js`, `addons/base_import/static/src/import_data_progress/import_data_progress.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/base_import/__manifest__.py`
- **HTTP entry points:** `addons/base_import/controllers/main.py:12`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `base` (addons/base_import/models/base_import.py:83); `base_import.mapping` (addons/base_import/models/base_import.py:97); inherits `res.users` (addons/base_import/models/base_import.py:117); `base_import.import` (addons/base_import/models/base_import.py:130)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/base_import/controllers/main.py:12`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `web`
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

- `addons/base_import/__init__.py`
- `addons/base_import/__manifest__.py`
- `addons/base_import/controllers/__init__.py`
- `addons/base_import/controllers/main.py`
- `addons/base_import/i18n/af.po`
- `addons/base_import/i18n/am.po`
- `addons/base_import/i18n/ar.po`
- `addons/base_import/i18n/az.po`
- `addons/base_import/i18n/base_import.pot`
- `addons/base_import/i18n/bg.po`
- `addons/base_import/i18n/bs.po`
- `addons/base_import/i18n/ca.po`
- `addons/base_import/i18n/cs.po`
- `addons/base_import/i18n/da.po`
- `addons/base_import/i18n/de.po`
- `addons/base_import/i18n/el.po`
- `addons/base_import/i18n/es.po`
- `addons/base_import/i18n/es_419.po`
- `addons/base_import/i18n/es_CL.po`
- `addons/base_import/i18n/et.po`
- `addons/base_import/i18n/eu.po`
- `addons/base_import/i18n/fa.po`
- `addons/base_import/i18n/fi.po`
- `addons/base_import/i18n/fo.po`
- `addons/base_import/i18n/fr.po`
- `addons/base_import/i18n/fr_CA.po`
- `addons/base_import/i18n/gl.po`
- `addons/base_import/i18n/gu.po`
- `addons/base_import/i18n/he.po`
- `addons/base_import/i18n/hi.po`
- `addons/base_import/i18n/hr.po`
- `addons/base_import/i18n/hu.po`
- `addons/base_import/i18n/id.po`
- `addons/base_import/i18n/is.po`
- `addons/base_import/i18n/it.po`
- `addons/base_import/i18n/ja.po`
- `addons/base_import/i18n/ka.po`
- `addons/base_import/i18n/kab.po`
- `addons/base_import/i18n/km.po`
- `addons/base_import/i18n/ko.po`
- `addons/base_import/i18n/ku.po`
- `addons/base_import/i18n/lo.po`
- `addons/base_import/i18n/lt.po`
- `addons/base_import/i18n/lv.po`
- `addons/base_import/i18n/mk.po`
- `addons/base_import/i18n/mn.po`
- `addons/base_import/i18n/my.po`
- `addons/base_import/i18n/nb.po`
- `addons/base_import/i18n/nl.po`
- `addons/base_import/i18n/pl.po`
- `addons/base_import/i18n/pt.po`
- `addons/base_import/i18n/pt_BR.po`
- `addons/base_import/i18n/ro.po`
- `addons/base_import/i18n/ru.po`
- `addons/base_import/i18n/sk.po`
- `addons/base_import/i18n/sl.po`
- `addons/base_import/i18n/sq.po`
- `addons/base_import/i18n/sr@latin.po`
- `addons/base_import/i18n/sv.po`
- `addons/base_import/i18n/th.po`
- `addons/base_import/i18n/tr.po`
- `addons/base_import/i18n/uk.po`
- `addons/base_import/i18n/uz.po`
- `addons/base_import/i18n/vi.po`
- `addons/base_import/i18n/zh_CN.po`
- `addons/base_import/i18n/zh_TW.po`
- `addons/base_import/models/__init__.py`
- `addons/base_import/models/base_import.py`
- `addons/base_import/models/odf_ods_reader.py`
- `addons/base_import/security/ir.access.csv`
- `addons/base_import/static/csv/External_id_3rd_party_application_product_categories.csv`
- `addons/base_import/static/csv/External_id_3rd_party_application_products.csv`
- `addons/base_import/static/csv/Name_products.csv`
- `addons/base_import/static/csv/database_import_test.sql`
- `addons/base_import/static/csv/m2m_customers_tags.csv`
- `addons/base_import/static/csv/o2m_customers_contacts.csv`
- `addons/base_import/static/csv/o2m_purchase_order_lines.csv`
- `addons/base_import/static/csv/purchase.order_functional_error_line_cant_adpat.csv`
- `addons/base_import/static/src/binary_file_manager.js`
- `addons/base_import/static/src/import_action/import_action.js`
- `addons/base_import/static/src/import_action/import_action.scss`
- `addons/base_import/static/src/import_action/import_action.xml`
- `addons/base_import/static/src/import_block_ui.js`
- `addons/base_import/static/src/import_block_ui.xml`
- `addons/base_import/static/src/import_data_column_error/import_data_column_error.js`
- `addons/base_import/static/src/import_data_column_error/import_data_column_error.xml`
- `addons/base_import/static/src/import_data_content/img/studio_icons.png`
- `addons/base_import/static/src/import_data_content/import_data_content.js`
- `addons/base_import/static/src/import_data_content/import_data_content.scss`
- `addons/base_import/static/src/import_data_content/import_data_content.xml`
- `addons/base_import/static/src/import_data_options/import_data_options.js`
- `addons/base_import/static/src/import_data_options/import_data_options.xml`
- `addons/base_import/static/src/import_data_progress/import_data_progress.js`
- `addons/base_import/static/src/import_data_progress/import_data_progress.scss`
- `addons/base_import/static/src/import_data_progress/import_data_progress.xml`
- `addons/base_import/static/src/import_data_sidepanel/import_data_sidepanel.js`
- `addons/base_import/static/src/import_data_sidepanel/import_data_sidepanel.scss`
- `addons/base_import/static/src/import_data_sidepanel/import_data_sidepanel.xml`
- `addons/base_import/static/src/import_model.js`
- `addons/base_import/static/src/import_records/import_records.js`
- `addons/base_import/static/src/import_records/import_records.xml`
- `addons/base_import/static/tests/import_action.test.js`
- `addons/base_import/static/tests/import_records.test.js`
