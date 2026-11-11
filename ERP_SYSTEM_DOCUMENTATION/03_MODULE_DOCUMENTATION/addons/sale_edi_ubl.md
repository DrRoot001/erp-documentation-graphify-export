# Module: sale_edi_ubl

- **Module ID:** MOD-511
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_edi_ubl`
- **Manifest:** `addons/sale_edi_ubl/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Electronic ordering module
===========================

Allows to import formats: UBL Bis 3.
When uploading or pasting Files in order list view with order related data inside XML file or PDF
File with embedded xml data will allow seller to retrieve Order data from Files.

**Scope evidence:** The module contains 61 files, including 10 Python, 1 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `sale`, `account_edi_ubl_cii`.

## 2. Module structure

- Model/business logic files: 5
- Controller/API files: 0
- XML/data/view/template files: 1
- Browser asset files: 0
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_edi_ubl/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 5 model declarations, 46 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/sale_edi_ubl/models/sale_order.py:6`, `addons/sale_edi_ubl/models/product_product.py:9`, `addons/sale_edi_ubl/models/customer_product_reference.py:6`, `addons/sale_edi_ubl/models/sale_order_line.py:6`, `addons/sale_edi_ubl/models/sale_edi_xml_ubl_bis3.py:10`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 1 XML files and 0 JavaScript/TypeScript files; static XML analysis found 0 record/template/menu identifiers.
- **Evidence:** Not found in module
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_edi_ubl/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/sale_edi_ubl/tests/test_sale_order_edi_gen.py`, `addons/sale_edi_ubl/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 1; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_edi_ubl/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 5
- Representative model evidence: inherits `sale.order` (addons/sale_edi_ubl/models/sale_order.py:6); inherits `product.product` (addons/sale_edi_ubl/models/product_product.py:9); `customer.product.reference` (addons/sale_edi_ubl/models/customer_product_reference.py:6); inherits `sale.order.line` (addons/sale_edi_ubl/models/sale_order_line.py:6); `sale.edi.xml.ubl_bis3` (addons/sale_edi_ubl/models/sale_edi_xml_ubl_bis3.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale`, `account_edi_ubl_cii`
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

- `addons/sale_edi_ubl/__init__.py`
- `addons/sale_edi_ubl/__manifest__.py`
- `addons/sale_edi_ubl/i18n/ar.po`
- `addons/sale_edi_ubl/i18n/az.po`
- `addons/sale_edi_ubl/i18n/bg.po`
- `addons/sale_edi_ubl/i18n/bs.po`
- `addons/sale_edi_ubl/i18n/ca.po`
- `addons/sale_edi_ubl/i18n/cs.po`
- `addons/sale_edi_ubl/i18n/da.po`
- `addons/sale_edi_ubl/i18n/de.po`
- `addons/sale_edi_ubl/i18n/el.po`
- `addons/sale_edi_ubl/i18n/es.po`
- `addons/sale_edi_ubl/i18n/es_419.po`
- `addons/sale_edi_ubl/i18n/et.po`
- `addons/sale_edi_ubl/i18n/fa.po`
- `addons/sale_edi_ubl/i18n/fi.po`
- `addons/sale_edi_ubl/i18n/fr.po`
- `addons/sale_edi_ubl/i18n/he.po`
- `addons/sale_edi_ubl/i18n/hi.po`
- `addons/sale_edi_ubl/i18n/hr.po`
- `addons/sale_edi_ubl/i18n/hu.po`
- `addons/sale_edi_ubl/i18n/id.po`
- `addons/sale_edi_ubl/i18n/it.po`
- `addons/sale_edi_ubl/i18n/ja.po`
- `addons/sale_edi_ubl/i18n/kab.po`
- `addons/sale_edi_ubl/i18n/ko.po`
- `addons/sale_edi_ubl/i18n/ku.po`
- `addons/sale_edi_ubl/i18n/lo.po`
- `addons/sale_edi_ubl/i18n/lt.po`
- `addons/sale_edi_ubl/i18n/lv.po`
- `addons/sale_edi_ubl/i18n/mn.po`
- `addons/sale_edi_ubl/i18n/my.po`
- `addons/sale_edi_ubl/i18n/nb.po`
- `addons/sale_edi_ubl/i18n/nl.po`
- `addons/sale_edi_ubl/i18n/pl.po`
- `addons/sale_edi_ubl/i18n/pt.po`
- `addons/sale_edi_ubl/i18n/pt_BR.po`
- `addons/sale_edi_ubl/i18n/ro.po`
- `addons/sale_edi_ubl/i18n/ru.po`
- `addons/sale_edi_ubl/i18n/sale_edi_ubl.pot`
- `addons/sale_edi_ubl/i18n/sk.po`
- `addons/sale_edi_ubl/i18n/sl.po`
- `addons/sale_edi_ubl/i18n/sr@latin.po`
- `addons/sale_edi_ubl/i18n/sv.po`
- `addons/sale_edi_ubl/i18n/th.po`
- `addons/sale_edi_ubl/i18n/tr.po`
- `addons/sale_edi_ubl/i18n/uk.po`
- `addons/sale_edi_ubl/i18n/uz.po`
- `addons/sale_edi_ubl/i18n/vi.po`
- `addons/sale_edi_ubl/i18n/zh_CN.po`
- `addons/sale_edi_ubl/i18n/zh_TW.po`
- `addons/sale_edi_ubl/models/__init__.py`
- `addons/sale_edi_ubl/models/customer_product_reference.py`
- `addons/sale_edi_ubl/models/product_product.py`
- `addons/sale_edi_ubl/models/sale_edi_xml_ubl_bis3.py`
- `addons/sale_edi_ubl/models/sale_order.py`
- `addons/sale_edi_ubl/models/sale_order_line.py`
- `addons/sale_edi_ubl/security/ir.access.csv`
- `addons/sale_edi_ubl/tests/__init__.py`
- `addons/sale_edi_ubl/tests/data/test_so_edi.xml`
- `addons/sale_edi_ubl/tests/test_sale_order_edi_gen.py`
