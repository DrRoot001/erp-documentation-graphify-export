# Module: purchase_edi_ubl_bis3

- **Module ID:** MOD-497
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/purchase_edi_ubl_bis3`
- **Manifest:** `addons/purchase_edi_ubl_bis3/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Supply Chain/Purchase`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Allows to export and import formats: UBL Bis 3.
When generating the PDF on the order, the PDF will be embedded inside the xml for all UBL formats. This allows the
receiver to retrieve the PDF with only the xml file.

**Scope evidence:** The module contains 61 files, including 9 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `purchase`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 3
- Controller/API files: 0
- XML/data/view/template files: 3
- Browser asset files: 0
- Security files: 0
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 3 model declarations, 46 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/purchase_edi_ubl_bis3/models/purchase_edi_xml_ubl_bis3.py:10`, `addons/purchase_edi_ubl_bis3/models/purchase_order.py:4`, `addons/purchase_edi_ubl_bis3/models/account_move.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/purchase_edi_ubl_bis3/tests/test_account_move_import.py`, `addons/purchase_edi_ubl_bis3/tests/test_purchase_order_edi_gen.py`, `addons/purchase_edi_ubl_bis3/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/purchase_edi_ubl_bis3/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 3
- Representative model evidence: `purchase.edi.xml.ubl_bis3` (addons/purchase_edi_ubl_bis3/models/purchase_edi_xml_ubl_bis3.py:10); inherits `purchase.order` (addons/purchase_edi_ubl_bis3/models/purchase_order.py:4); inherits `account.move` (addons/purchase_edi_ubl_bis3/models/account_move.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `purchase`, `account_edi_ubl_cii`
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

- `addons/purchase_edi_ubl_bis3/__init__.py`
- `addons/purchase_edi_ubl_bis3/__manifest__.py`
- `addons/purchase_edi_ubl_bis3/i18n/ar.po`
- `addons/purchase_edi_ubl_bis3/i18n/az.po`
- `addons/purchase_edi_ubl_bis3/i18n/bg.po`
- `addons/purchase_edi_ubl_bis3/i18n/bs.po`
- `addons/purchase_edi_ubl_bis3/i18n/ca.po`
- `addons/purchase_edi_ubl_bis3/i18n/cs.po`
- `addons/purchase_edi_ubl_bis3/i18n/da.po`
- `addons/purchase_edi_ubl_bis3/i18n/de.po`
- `addons/purchase_edi_ubl_bis3/i18n/el.po`
- `addons/purchase_edi_ubl_bis3/i18n/es.po`
- `addons/purchase_edi_ubl_bis3/i18n/es_419.po`
- `addons/purchase_edi_ubl_bis3/i18n/et.po`
- `addons/purchase_edi_ubl_bis3/i18n/fa.po`
- `addons/purchase_edi_ubl_bis3/i18n/fi.po`
- `addons/purchase_edi_ubl_bis3/i18n/fr.po`
- `addons/purchase_edi_ubl_bis3/i18n/he.po`
- `addons/purchase_edi_ubl_bis3/i18n/hi.po`
- `addons/purchase_edi_ubl_bis3/i18n/hr.po`
- `addons/purchase_edi_ubl_bis3/i18n/hu.po`
- `addons/purchase_edi_ubl_bis3/i18n/id.po`
- `addons/purchase_edi_ubl_bis3/i18n/it.po`
- `addons/purchase_edi_ubl_bis3/i18n/ja.po`
- `addons/purchase_edi_ubl_bis3/i18n/kab.po`
- `addons/purchase_edi_ubl_bis3/i18n/ko.po`
- `addons/purchase_edi_ubl_bis3/i18n/ku.po`
- `addons/purchase_edi_ubl_bis3/i18n/lo.po`
- `addons/purchase_edi_ubl_bis3/i18n/lt.po`
- `addons/purchase_edi_ubl_bis3/i18n/lv.po`
- `addons/purchase_edi_ubl_bis3/i18n/mn.po`
- `addons/purchase_edi_ubl_bis3/i18n/my.po`
- `addons/purchase_edi_ubl_bis3/i18n/nb.po`
- `addons/purchase_edi_ubl_bis3/i18n/nl.po`
- `addons/purchase_edi_ubl_bis3/i18n/pl.po`
- `addons/purchase_edi_ubl_bis3/i18n/pt.po`
- `addons/purchase_edi_ubl_bis3/i18n/pt_BR.po`
- `addons/purchase_edi_ubl_bis3/i18n/purchase_edi_ubl_bis3.pot`
- `addons/purchase_edi_ubl_bis3/i18n/ro.po`
- `addons/purchase_edi_ubl_bis3/i18n/ru.po`
- `addons/purchase_edi_ubl_bis3/i18n/sk.po`
- `addons/purchase_edi_ubl_bis3/i18n/sl.po`
- `addons/purchase_edi_ubl_bis3/i18n/sr@latin.po`
- `addons/purchase_edi_ubl_bis3/i18n/sv.po`
- `addons/purchase_edi_ubl_bis3/i18n/th.po`
- `addons/purchase_edi_ubl_bis3/i18n/tr.po`
- `addons/purchase_edi_ubl_bis3/i18n/uk.po`
- `addons/purchase_edi_ubl_bis3/i18n/uz.po`
- `addons/purchase_edi_ubl_bis3/i18n/vi.po`
- `addons/purchase_edi_ubl_bis3/i18n/zh_CN.po`
- `addons/purchase_edi_ubl_bis3/i18n/zh_TW.po`
- `addons/purchase_edi_ubl_bis3/models/__init__.py`
- `addons/purchase_edi_ubl_bis3/models/account_move.py`
- `addons/purchase_edi_ubl_bis3/models/purchase_edi_xml_ubl_bis3.py`
- `addons/purchase_edi_ubl_bis3/models/purchase_order.py`
- `addons/purchase_edi_ubl_bis3/tests/__init__.py`
- `addons/purchase_edi_ubl_bis3/tests/data/test_po_edi.xml`
- `addons/purchase_edi_ubl_bis3/tests/test_account_move_import.py`
- `addons/purchase_edi_ubl_bis3/tests/test_files/ubl_bis3_PO.xml`
- `addons/purchase_edi_ubl_bis3/tests/test_files/ubl_bis3_PO_description.xml`
- `addons/purchase_edi_ubl_bis3/tests/test_purchase_order_edi_gen.py`
