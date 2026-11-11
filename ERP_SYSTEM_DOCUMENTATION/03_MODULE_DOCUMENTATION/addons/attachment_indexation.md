# Module: attachment_indexation

- **Module ID:** MOD-019
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/attachment_indexation`
- **Manifest:** `addons/attachment_indexation/__manifest__.py`
- **Implementation assessment:** Partially implemented / limited artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden/Tools`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Attachments list and document indexation
========================================
* Show attachment on the top of the forms
* Document Indexation: odt, pdf, xlsx, docx

The `pdfminer.six` Python library has to be installed in order to index PDF files

**Scope evidence:** The module contains 56 files, including 6 Python, 0 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `web`.

## 2. Module structure

- Model/business logic files: 1
- Controller/API files: 0
- XML/data/view/template files: 0
- Browser asset files: 0
- Security files: 0
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 1 model declarations, 10 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/attachment_indexation/models/ir_attachment.py:67`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/attachment_indexation/tests/test_indexation.py`, `addons/attachment_indexation/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 0; representative identifiers: None found
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/attachment_indexation/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 1
- Representative model evidence: inherits `ir.attachment` (addons/attachment_indexation/models/ir_attachment.py:67)
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
- **UI/data evidence:** Not found
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/attachment_indexation/__init__.py`
- `addons/attachment_indexation/__manifest__.py`
- `addons/attachment_indexation/i18n/ar.po`
- `addons/attachment_indexation/i18n/attachment_indexation.pot`
- `addons/attachment_indexation/i18n/az.po`
- `addons/attachment_indexation/i18n/bg.po`
- `addons/attachment_indexation/i18n/bs.po`
- `addons/attachment_indexation/i18n/ca.po`
- `addons/attachment_indexation/i18n/cs.po`
- `addons/attachment_indexation/i18n/da.po`
- `addons/attachment_indexation/i18n/de.po`
- `addons/attachment_indexation/i18n/el.po`
- `addons/attachment_indexation/i18n/es.po`
- `addons/attachment_indexation/i18n/es_419.po`
- `addons/attachment_indexation/i18n/et.po`
- `addons/attachment_indexation/i18n/fa.po`
- `addons/attachment_indexation/i18n/fi.po`
- `addons/attachment_indexation/i18n/fr.po`
- `addons/attachment_indexation/i18n/he.po`
- `addons/attachment_indexation/i18n/hi.po`
- `addons/attachment_indexation/i18n/hr.po`
- `addons/attachment_indexation/i18n/hu.po`
- `addons/attachment_indexation/i18n/id.po`
- `addons/attachment_indexation/i18n/it.po`
- `addons/attachment_indexation/i18n/ja.po`
- `addons/attachment_indexation/i18n/kab.po`
- `addons/attachment_indexation/i18n/ko.po`
- `addons/attachment_indexation/i18n/ku.po`
- `addons/attachment_indexation/i18n/lo.po`
- `addons/attachment_indexation/i18n/lt.po`
- `addons/attachment_indexation/i18n/lv.po`
- `addons/attachment_indexation/i18n/mn.po`
- `addons/attachment_indexation/i18n/my.po`
- `addons/attachment_indexation/i18n/nb.po`
- `addons/attachment_indexation/i18n/nl.po`
- `addons/attachment_indexation/i18n/pl.po`
- `addons/attachment_indexation/i18n/pt.po`
- `addons/attachment_indexation/i18n/pt_BR.po`
- `addons/attachment_indexation/i18n/ro.po`
- `addons/attachment_indexation/i18n/ru.po`
- `addons/attachment_indexation/i18n/sk.po`
- `addons/attachment_indexation/i18n/sl.po`
- `addons/attachment_indexation/i18n/sr@latin.po`
- `addons/attachment_indexation/i18n/sv.po`
- `addons/attachment_indexation/i18n/th.po`
- `addons/attachment_indexation/i18n/tr.po`
- `addons/attachment_indexation/i18n/uk.po`
- `addons/attachment_indexation/i18n/uz.po`
- `addons/attachment_indexation/i18n/vi.po`
- `addons/attachment_indexation/i18n/zh_CN.po`
- `addons/attachment_indexation/i18n/zh_TW.po`
- `addons/attachment_indexation/models/__init__.py`
- `addons/attachment_indexation/models/ir_attachment.py`
- `addons/attachment_indexation/tests/__init__.py`
- `addons/attachment_indexation/tests/files/test_content.pdf`
- `addons/attachment_indexation/tests/test_indexation.py`
