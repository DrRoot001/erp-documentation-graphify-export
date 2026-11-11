# Module: l10n_pl_edi_jst

- **Module ID:** MOD-300
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_pl_edi_jst`
- **Manifest:** `addons/l10n_pl_edi_jst/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Support for Local Government Unit (LGU) in the FA(3) format

**Manifest description:**

Export FA(3) compliant XML invoices and prepare for integration with KSeF.

**Scope evidence:** The module contains 12 files, including 7 Python, 3 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `l10n_pl`, `l10n_pl_edi`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 0
- XML/data/view/template files: 3
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

- **Description:** 2 model declarations, 3 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_pl_edi_jst/models/res_partner.py:4`, `addons/l10n_pl_edi_jst/models/account_move.py:6`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 3 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/l10n_pl_edi_jst/data/fa3_template.xml:3`, `addons/l10n_pl_edi_jst/views/res_partner_views.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/l10n_pl_edi_jst/tests/test_l10n_pl_edi_jst.py`, `addons/l10n_pl_edi_jst/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 3; representative identifiers: `l10n_pl_edi_jst.fa3_xml_template`, `res_partner_account_pl_form`
- Menus: 0; representative evidence: Not found in module
- Templates: 1; representative evidence: `addons/l10n_pl_edi_jst/data/fa3_template.xml:3`
- View/action field declarations: 2; representative evidence: `addons/l10n_pl_edi_jst/views/res_partner_views.xml:6`, `addons/l10n_pl_edi_jst/views/res_partner_views.xml:8`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_pl_edi_jst/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `res.partner` (addons/l10n_pl_edi_jst/models/res_partner.py:4); inherits `account.move` (addons/l10n_pl_edi_jst/models/account_move.py:6)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `l10n_pl`, `l10n_pl_edi`
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

- `addons/l10n_pl_edi_jst/__init__.py`
- `addons/l10n_pl_edi_jst/__manifest__.py`
- `addons/l10n_pl_edi_jst/data/fa3_template.xml`
- `addons/l10n_pl_edi_jst/i18n/l10n_pl_edi_jst.pot`
- `addons/l10n_pl_edi_jst/i18n/pl.po`
- `addons/l10n_pl_edi_jst/models/__init__.py`
- `addons/l10n_pl_edi_jst/models/account_move.py`
- `addons/l10n_pl_edi_jst/models/res_partner.py`
- `addons/l10n_pl_edi_jst/tests/__init__.py`
- `addons/l10n_pl_edi_jst/tests/export_xmls/standert_fa3_format_with_jst.xml`
- `addons/l10n_pl_edi_jst/tests/test_l10n_pl_edi_jst.py`
- `addons/l10n_pl_edi_jst/views/res_partner_views.xml`
