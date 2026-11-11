# Module: account_payment_custom

- **Module ID:** MOD-009
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_payment_custom`
- **Manifest:** `addons/account_payment_custom/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Custom`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Bridge between payment_custom and account_payment.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 66 files, including 15 Python, 2 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account_payment`, `payment_custom`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 2
- XML/data/view/template files: 2
- Browser asset files: 0
- Security files: 0
- Test files: 5
- Scheduled/automation evidence files: 6
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 23 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/account_payment_custom/models/account_payment_method.py:6`, `addons/account_payment_custom/models/account_bank_statement_line.py:8`, `addons/account_payment_custom/models/payment_transaction.py:6`, `addons/account_payment_custom/models/payment_provider.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/account_payment_custom/controllers/portal.py`, `addons/account_payment_custom/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 2 XML files and 0 JavaScript/TypeScript files; static XML analysis found 2 record/template/menu identifiers.
- **Evidence:** `addons/account_payment_custom/data/ir_cron.xml:4`, `addons/account_payment_custom/data/account_payment_method.xml:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 6 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/account_payment_custom/__manifest__.py`, `addons/account_payment_custom/models/account_bank_statement_line.py`, `addons/account_payment_custom/models/payment_provider.py`, `addons/account_payment_custom/data/ir_cron.xml`, `addons/account_payment_custom/tests/test_payment_provider.py`, `addons/account_payment_custom/tests/test_account_bank_statement_line.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/account_payment_custom/tests/common.py`, `addons/account_payment_custom/tests/test_portal.py`, `addons/account_payment_custom/tests/test_payment_provider.py`, `addons/account_payment_custom/tests/__init__.py`, `addons/account_payment_custom/tests/test_account_bank_statement_line.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 2; representative identifiers: `cron_auto_confirm_paid_wire_transfer_txs`, `account_payment_method_wire_transfer`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 0; representative evidence: Not found in module
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_payment_custom/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** `addons/account_payment_custom/__manifest__.py`, `addons/account_payment_custom/models/account_bank_statement_line.py`, `addons/account_payment_custom/models/payment_provider.py`, `addons/account_payment_custom/data/ir_cron.xml`, `addons/account_payment_custom/tests/test_payment_provider.py`, `addons/account_payment_custom/tests/test_account_bank_statement_line.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `account.payment.method` (addons/account_payment_custom/models/account_payment_method.py:6); inherits `account.bank.statement.line` (addons/account_payment_custom/models/account_bank_statement_line.py:8); inherits `payment.transaction` (addons/account_payment_custom/models/payment_transaction.py:6); inherits `payment.provider` (addons/account_payment_custom/models/payment_provider.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account_payment`, `payment_custom`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Not found
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/account_payment_custom/__init__.py`
- `addons/account_payment_custom/__manifest__.py`
- `addons/account_payment_custom/const.py`
- `addons/account_payment_custom/controllers/__init__.py`
- `addons/account_payment_custom/controllers/portal.py`
- `addons/account_payment_custom/data/account_payment_method.xml`
- `addons/account_payment_custom/data/ir_cron.xml`
- `addons/account_payment_custom/i18n/account_payment_custom.pot`
- `addons/account_payment_custom/i18n/ar.po`
- `addons/account_payment_custom/i18n/az.po`
- `addons/account_payment_custom/i18n/bg.po`
- `addons/account_payment_custom/i18n/bs.po`
- `addons/account_payment_custom/i18n/ca.po`
- `addons/account_payment_custom/i18n/cs.po`
- `addons/account_payment_custom/i18n/da.po`
- `addons/account_payment_custom/i18n/de.po`
- `addons/account_payment_custom/i18n/el.po`
- `addons/account_payment_custom/i18n/es.po`
- `addons/account_payment_custom/i18n/es_419.po`
- `addons/account_payment_custom/i18n/et.po`
- `addons/account_payment_custom/i18n/fa.po`
- `addons/account_payment_custom/i18n/fi.po`
- `addons/account_payment_custom/i18n/fr.po`
- `addons/account_payment_custom/i18n/he.po`
- `addons/account_payment_custom/i18n/hi.po`
- `addons/account_payment_custom/i18n/hr.po`
- `addons/account_payment_custom/i18n/hu.po`
- `addons/account_payment_custom/i18n/id.po`
- `addons/account_payment_custom/i18n/it.po`
- `addons/account_payment_custom/i18n/ja.po`
- `addons/account_payment_custom/i18n/kab.po`
- `addons/account_payment_custom/i18n/ko.po`
- `addons/account_payment_custom/i18n/ku.po`
- `addons/account_payment_custom/i18n/lo.po`
- `addons/account_payment_custom/i18n/lt.po`
- `addons/account_payment_custom/i18n/lv.po`
- `addons/account_payment_custom/i18n/mn.po`
- `addons/account_payment_custom/i18n/my.po`
- `addons/account_payment_custom/i18n/nb.po`
- `addons/account_payment_custom/i18n/nl.po`
- `addons/account_payment_custom/i18n/pl.po`
- `addons/account_payment_custom/i18n/pt.po`
- `addons/account_payment_custom/i18n/pt_BR.po`
- `addons/account_payment_custom/i18n/ro.po`
- `addons/account_payment_custom/i18n/ru.po`
- `addons/account_payment_custom/i18n/sk.po`
- `addons/account_payment_custom/i18n/sl.po`
- `addons/account_payment_custom/i18n/sr@latin.po`
- `addons/account_payment_custom/i18n/sv.po`
- `addons/account_payment_custom/i18n/th.po`
- `addons/account_payment_custom/i18n/tr.po`
- `addons/account_payment_custom/i18n/uk.po`
- `addons/account_payment_custom/i18n/uz.po`
- `addons/account_payment_custom/i18n/vi.po`
- `addons/account_payment_custom/i18n/zh_CN.po`
- `addons/account_payment_custom/i18n/zh_TW.po`
- `addons/account_payment_custom/models/__init__.py`
- `addons/account_payment_custom/models/account_bank_statement_line.py`
- `addons/account_payment_custom/models/account_payment_method.py`
- `addons/account_payment_custom/models/payment_provider.py`
- `addons/account_payment_custom/models/payment_transaction.py`
- `addons/account_payment_custom/tests/__init__.py`
- `addons/account_payment_custom/tests/common.py`
- `addons/account_payment_custom/tests/test_account_bank_statement_line.py`
- `addons/account_payment_custom/tests/test_payment_provider.py`
- `addons/account_payment_custom/tests/test_portal.py`
