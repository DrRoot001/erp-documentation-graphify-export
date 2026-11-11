# Module: payment_custom

- **Module ID:** MOD-398
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment_custom`
- **Manifest:** `addons/payment_custom/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Payment Providers`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** A payment provider for custom flows like wire transfers.

**Manifest description:**



**Scope evidence:** The module contains 87 files, including 12 Python, 4 XML, and 2 JavaScript/TypeScript files. The manifest declares dependencies: `payment`.

## 2. Module structure

- Model/business logic files: 2
- Controller/API files: 2
- XML/data/view/template files: 4
- Browser asset files: 2
- Security files: 0
- Test files: 4
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 2 model declarations, 25 methods, 0 constraint handlers, 0 onchange handlers, and 1 dependency declarations.
- **Evidence:** `addons/payment_custom/models/payment_transaction.py:15`, `addons/payment_custom/models/payment_provider.py:9`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 1 route declarations.
- **Evidence:** `addons/payment_custom/controllers/main.py:15`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 4 XML files and 2 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/payment_custom/data/payment_provider_data.xml:4`, `addons/payment_custom/data/payment_provider_data.xml:15`, `addons/payment_custom/data/payment_method_data.xml:4`, `addons/payment_custom/data/payment_method_data.xml:15`, `addons/payment_custom/views/payment_custom_templates.xml:4`, `addons/payment_custom/views/payment_custom_templates.xml:10`, `addons/payment_custom/views/payment_custom_templates.xml:16`, `addons/payment_custom/views/payment_custom_templates.xml:43`, `addons/payment_custom/views/payment_provider_views.xml:4`, `addons/payment_custom/views/payment_provider_views.xml:67`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 4 test files are present.
- **Evidence:** `addons/payment_custom/tests/test_processing_flows.py`, `addons/payment_custom/tests/common.py`, `addons/payment_custom/tests/test_payment_transaction.py`, `addons/payment_custom/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 4; representative identifiers: `payment.payment_provider_pay_on_invoice`, `payment.payment_provider_transfer`, `payment_method_pay_on_invoice`, `payment_method_wire_transfer`, `payment_custom.token_form`, `payment_custom.payment_method_form`, `custom_state_header`, `custom_payment_transfer_details`, `payment_provider_form`, `payment_provider_kanban`
- Menus: 0; representative evidence: Not found in module
- Templates: 4; representative evidence: `addons/payment_custom/views/payment_custom_templates.xml:4`, `addons/payment_custom/views/payment_custom_templates.xml:10`, `addons/payment_custom/views/payment_custom_templates.xml:16`, `addons/payment_custom/views/payment_custom_templates.xml:43`
- View/action field declarations: 4; representative evidence: `addons/payment_custom/views/payment_provider_views.xml:6`, `addons/payment_custom/views/payment_provider_views.xml:11`, `addons/payment_custom/views/payment_provider_views.xml:69`, `addons/payment_custom/views/payment_provider_views.xml:71`
- Browser assets: 2; representative files: `addons/payment_custom/static/src/interactions/payment_form.js`, `addons/payment_custom/static/src/interactions/payment_status.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment_custom/__manifest__.py`
- **HTTP entry points:** `addons/payment_custom/controllers/main.py:15`
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 2
- Representative model evidence: inherits `payment.transaction` (addons/payment_custom/models/payment_transaction.py:15); inherits `payment.provider` (addons/payment_custom/models/payment_provider.py:9)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 1
- Route evidence: `addons/payment_custom/controllers/main.py:15`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `payment`
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

- `addons/payment_custom/README.md`
- `addons/payment_custom/__init__.py`
- `addons/payment_custom/__manifest__.py`
- `addons/payment_custom/const.py`
- `addons/payment_custom/controllers/__init__.py`
- `addons/payment_custom/controllers/main.py`
- `addons/payment_custom/data/payment_method_data.xml`
- `addons/payment_custom/data/payment_provider_data.xml`
- `addons/payment_custom/i18n/af.po`
- `addons/payment_custom/i18n/ar.po`
- `addons/payment_custom/i18n/az.po`
- `addons/payment_custom/i18n/bg.po`
- `addons/payment_custom/i18n/bs.po`
- `addons/payment_custom/i18n/ca.po`
- `addons/payment_custom/i18n/cs.po`
- `addons/payment_custom/i18n/da.po`
- `addons/payment_custom/i18n/de.po`
- `addons/payment_custom/i18n/el.po`
- `addons/payment_custom/i18n/es.po`
- `addons/payment_custom/i18n/es_419.po`
- `addons/payment_custom/i18n/es_CL.po`
- `addons/payment_custom/i18n/et.po`
- `addons/payment_custom/i18n/fa.po`
- `addons/payment_custom/i18n/fi.po`
- `addons/payment_custom/i18n/fo.po`
- `addons/payment_custom/i18n/fr.po`
- `addons/payment_custom/i18n/fr_BE.po`
- `addons/payment_custom/i18n/gl.po`
- `addons/payment_custom/i18n/gu.po`
- `addons/payment_custom/i18n/he.po`
- `addons/payment_custom/i18n/hi.po`
- `addons/payment_custom/i18n/hr.po`
- `addons/payment_custom/i18n/hu.po`
- `addons/payment_custom/i18n/hy.po`
- `addons/payment_custom/i18n/id.po`
- `addons/payment_custom/i18n/is.po`
- `addons/payment_custom/i18n/it.po`
- `addons/payment_custom/i18n/ja.po`
- `addons/payment_custom/i18n/ka.po`
- `addons/payment_custom/i18n/kab.po`
- `addons/payment_custom/i18n/km.po`
- `addons/payment_custom/i18n/ko.po`
- `addons/payment_custom/i18n/ku.po`
- `addons/payment_custom/i18n/lo.po`
- `addons/payment_custom/i18n/lt.po`
- `addons/payment_custom/i18n/lv.po`
- `addons/payment_custom/i18n/mk.po`
- `addons/payment_custom/i18n/mn.po`
- `addons/payment_custom/i18n/my.po`
- `addons/payment_custom/i18n/nb.po`
- `addons/payment_custom/i18n/nl.po`
- `addons/payment_custom/i18n/payment_custom.pot`
- `addons/payment_custom/i18n/pl.po`
- `addons/payment_custom/i18n/pt.po`
- `addons/payment_custom/i18n/pt_BR.po`
- `addons/payment_custom/i18n/ro.po`
- `addons/payment_custom/i18n/ru.po`
- `addons/payment_custom/i18n/sk.po`
- `addons/payment_custom/i18n/sl.po`
- `addons/payment_custom/i18n/sr@latin.po`
- `addons/payment_custom/i18n/sv.po`
- `addons/payment_custom/i18n/te.po`
- `addons/payment_custom/i18n/th.po`
- `addons/payment_custom/i18n/tr.po`
- `addons/payment_custom/i18n/uk.po`
- `addons/payment_custom/i18n/uz.po`
- `addons/payment_custom/i18n/vi.po`
- `addons/payment_custom/i18n/zh_CN.po`
- `addons/payment_custom/i18n/zh_TW.po`
- `addons/payment_custom/models/__init__.py`
- `addons/payment_custom/models/payment_provider.py`
- `addons/payment_custom/models/payment_transaction.py`
- `addons/payment_custom/static/description/icon.png`
- `addons/payment_custom/static/description/icon.svg`
- `addons/payment_custom/static/description/icon_hi.png`
- `addons/payment_custom/static/description/icon_invoice.png`
- `addons/payment_custom/static/description/icon_invoice.svg`
- `addons/payment_custom/static/img/pay_on_invoice.png`
- `addons/payment_custom/static/img/wire_transfer.png`
- `addons/payment_custom/static/src/interactions/payment_form.js`
- `addons/payment_custom/static/src/interactions/payment_status.js`
- `addons/payment_custom/tests/__init__.py`
- `addons/payment_custom/tests/common.py`
- `addons/payment_custom/tests/test_payment_transaction.py`
- `addons/payment_custom/tests/test_processing_flows.py`
- `addons/payment_custom/views/payment_custom_templates.xml`
- `addons/payment_custom/views/payment_provider_views.xml`
