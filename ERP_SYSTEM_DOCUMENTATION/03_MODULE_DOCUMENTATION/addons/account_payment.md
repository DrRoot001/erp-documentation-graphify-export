# Module: account_payment

- **Module ID:** MOD-008
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/account_payment`
- **Manifest:** `addons/account_payment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Accounting`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Enable customers to pay invoices on the portal and post payments when transactions are processed.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 95 files, including 23 Python, 14 XML, and 4 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `payment`.

## 2. Module structure

- Model/business logic files: 11
- Controller/API files: 3
- XML/data/view/template files: 14
- Browser asset files: 4
- Security files: 1
- Test files: 5
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/account_payment/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 11 model declarations, 111 methods, 1 constraint handlers, 1 onchange handlers, and 20 dependency declarations.
- **Evidence:** `addons/account_payment/models/account_payment_method.py:7`, `addons/account_payment/models/account_payment.py:7`, `addons/account_payment/models/account_payment_method_line.py:7`, `addons/account_payment/models/account_journal.py:7`, `addons/account_payment/models/account_move.py:11`, `addons/account_payment/models/payment_transaction.py:6`, `addons/account_payment/models/payment_provider.py:16`, `addons/account_payment/wizards/res_config_settings.py:6`, `addons/account_payment/wizards/payment_refund_wizard.py:7`, `addons/account_payment/wizards/payment_link_wizard.py:9`, `addons/account_payment/wizards/account_payment_register.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 5 route declarations.
- **Evidence:** `addons/account_payment/controllers/portal.py:53`, `addons/account_payment/controllers/portal.py:155`, `addons/account_payment/controllers/payment.py:14`, `addons/account_payment/controllers/payment.py:38`, `addons/account_payment/controllers/payment.py:76`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 14 XML files and 4 JavaScript/TypeScript files; static XML analysis found 24 record/template/menu identifiers.
- **Evidence:** `addons/account_payment/wizards/res_config_settings_views.xml:4`, `addons/account_payment/wizards/account_payment_register_views.xml:4`, `addons/account_payment/wizards/payment_link_wizard_views.xml:4`, `addons/account_payment/wizards/payment_link_wizard_views.xml:14`, `addons/account_payment/wizards/payment_refund_wizard_views.xml:4`, `addons/account_payment/data/ir_config_parameter.xml:4`, `addons/account_payment/data/portal_entry_data.xml:3`, `addons/account_payment/views/account_payment_menus.xml:4`, `addons/account_payment/views/account_move_views.xml:4`, `addons/account_payment/views/account_payment_views.xml:4`, `addons/account_payment/views/payment_transaction_views.xml:4`, `addons/account_payment/views/account_portal_templates.xml:2`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/account_payment/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/account_payment/models/account_move.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 5 test files are present.
- **Evidence:** `addons/account_payment/tests/test_account_payment.py`, `addons/account_payment/tests/common.py`, `addons/account_payment/tests/test_payment_flows.py`, `addons/account_payment/tests/test_payment_provider.py`, `addons/account_payment/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 14; representative identifiers: `res_config_settings_view_form`, `view_account_payment_register_form_inherit_payment`, `action_invoice_order_generate_link`, `payment_link_wizard__form_inherit_account_payment`, `payment_refund_wizard_view_form`, `enable_portal_payment`, `portal_entry_overdue_invoices`, `payment_provider_menu`, `account_invoice_view_form_inherit_payment`, `view_account_payment_form_inherit_payment`, `payment_transaction_form`, `Portal layout: overdue invoices`, `account_payment.portal_docs_entry`, `Overdue payments`, `Payment on My Invoices`, `Invoice Payment`, `Invoice Paid`, `Payment on My Invoices`, `Invoice error display: payment errors`, `Invoice success display: payment success`
- Menus: 1; representative evidence: `addons/account_payment/views/account_payment_menus.xml:4`
- Templates: 11; representative evidence: `addons/account_payment/views/account_portal_templates.xml:2`, `addons/account_payment/views/account_portal_templates.xml:23`, `addons/account_payment/views/account_portal_templates.xml:34`, `addons/account_payment/views/account_portal_templates.xml:58`, `addons/account_payment/views/account_portal_templates.xml:113`, `addons/account_payment/views/account_portal_templates.xml:236`, `addons/account_payment/views/account_portal_templates.xml:252`, `addons/account_payment/views/account_portal_templates.xml:292`, `addons/account_payment/views/account_portal_templates.xml:314`, `addons/account_payment/views/account_portal_templates.xml:330`, `addons/account_payment/views/payment_form_templates.xml:4`
- View/action field declarations: 20; representative evidence: `addons/account_payment/wizards/res_config_settings_views.xml:6`, `addons/account_payment/wizards/res_config_settings_views.xml:8`, `addons/account_payment/wizards/account_payment_register_views.xml:6`, `addons/account_payment/wizards/account_payment_register_views.xml:8`, `addons/account_payment/wizards/payment_link_wizard_views.xml:6`, `addons/account_payment/wizards/payment_link_wizard_views.xml:7`, `addons/account_payment/wizards/payment_link_wizard_views.xml:16`, `addons/account_payment/wizards/payment_link_wizard_views.xml:18`, `addons/account_payment/wizards/payment_refund_wizard_views.xml:6`, `addons/account_payment/wizards/payment_refund_wizard_views.xml:7`, `addons/account_payment/views/account_move_views.xml:6`, `addons/account_payment/views/account_move_views.xml:8`
- Browser assets: 4; representative files: `addons/account_payment/static/src/interactions/portal_invoice_page_payment.js`, `addons/account_payment/static/src/interactions/portal_my_invoices_payment_list.js`, `addons/account_payment/static/src/interactions/payment_form.js`, `addons/account_payment/static/tests/interactions/portal_invoice_page_payment.test.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/account_payment/__manifest__.py`
- **HTTP entry points:** `addons/account_payment/controllers/portal.py:53`, `addons/account_payment/controllers/portal.py:155`, `addons/account_payment/controllers/payment.py:14`, `addons/account_payment/controllers/payment.py:38`, `addons/account_payment/controllers/payment.py:76`
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/account_payment/models/account_move.py`

## 7. Database interactions

- Model declarations: 11
- Representative model evidence: inherits `account.payment.method` (addons/account_payment/models/account_payment_method.py:7); inherits `account.payment` (addons/account_payment/models/account_payment.py:7); inherits `account.payment.method.line` (addons/account_payment/models/account_payment_method_line.py:7); inherits `account.journal` (addons/account_payment/models/account_journal.py:7); inherits `account.move` (addons/account_payment/models/account_move.py:11); inherits `payment.transaction` (addons/account_payment/models/payment_transaction.py:6); inherits `payment.provider` (addons/account_payment/models/payment_provider.py:16); inherits `res.config.settings` (addons/account_payment/wizards/res_config_settings.py:6); `payment.refund.wizard` (addons/account_payment/wizards/payment_refund_wizard.py:7); inherits `payment.link.wizard` (addons/account_payment/wizards/payment_link_wizard.py:9); inherits `account.payment.register` (addons/account_payment/wizards/account_payment_register.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 5
- Route evidence: `addons/account_payment/controllers/portal.py:53`, `addons/account_payment/controllers/portal.py:155`, `addons/account_payment/controllers/payment.py:14`, `addons/account_payment/controllers/payment.py:38`, `addons/account_payment/controllers/payment.py:76`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `payment`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Present
- **Security evidence:** Present
- **Test evidence:** Present
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/account_payment/__init__.py`
- `addons/account_payment/__manifest__.py`
- `addons/account_payment/controllers/__init__.py`
- `addons/account_payment/controllers/payment.py`
- `addons/account_payment/controllers/portal.py`
- `addons/account_payment/data/ir_config_parameter.xml`
- `addons/account_payment/data/portal_entry_data.xml`
- `addons/account_payment/i18n/account_payment.pot`
- `addons/account_payment/i18n/af.po`
- `addons/account_payment/i18n/ar.po`
- `addons/account_payment/i18n/az.po`
- `addons/account_payment/i18n/bg.po`
- `addons/account_payment/i18n/bs.po`
- `addons/account_payment/i18n/ca.po`
- `addons/account_payment/i18n/cs.po`
- `addons/account_payment/i18n/da.po`
- `addons/account_payment/i18n/de.po`
- `addons/account_payment/i18n/el.po`
- `addons/account_payment/i18n/es.po`
- `addons/account_payment/i18n/es_419.po`
- `addons/account_payment/i18n/et.po`
- `addons/account_payment/i18n/fa.po`
- `addons/account_payment/i18n/fi.po`
- `addons/account_payment/i18n/fr.po`
- `addons/account_payment/i18n/gu.po`
- `addons/account_payment/i18n/he.po`
- `addons/account_payment/i18n/hi.po`
- `addons/account_payment/i18n/hr.po`
- `addons/account_payment/i18n/hu.po`
- `addons/account_payment/i18n/id.po`
- `addons/account_payment/i18n/is.po`
- `addons/account_payment/i18n/it.po`
- `addons/account_payment/i18n/ja.po`
- `addons/account_payment/i18n/kab.po`
- `addons/account_payment/i18n/ko.po`
- `addons/account_payment/i18n/ku.po`
- `addons/account_payment/i18n/lo.po`
- `addons/account_payment/i18n/lt.po`
- `addons/account_payment/i18n/lv.po`
- `addons/account_payment/i18n/mn.po`
- `addons/account_payment/i18n/my.po`
- `addons/account_payment/i18n/nb.po`
- `addons/account_payment/i18n/nl.po`
- `addons/account_payment/i18n/pl.po`
- `addons/account_payment/i18n/pt.po`
- `addons/account_payment/i18n/pt_BR.po`
- `addons/account_payment/i18n/ro.po`
- `addons/account_payment/i18n/ru.po`
- `addons/account_payment/i18n/sk.po`
- `addons/account_payment/i18n/sl.po`
- `addons/account_payment/i18n/sq.po`
- `addons/account_payment/i18n/sr@latin.po`
- `addons/account_payment/i18n/sv.po`
- `addons/account_payment/i18n/th.po`
- `addons/account_payment/i18n/tr.po`
- `addons/account_payment/i18n/uk.po`
- `addons/account_payment/i18n/uz.po`
- `addons/account_payment/i18n/vi.po`
- `addons/account_payment/i18n/zh_CN.po`
- `addons/account_payment/i18n/zh_TW.po`
- `addons/account_payment/models/__init__.py`
- `addons/account_payment/models/account_journal.py`
- `addons/account_payment/models/account_move.py`
- `addons/account_payment/models/account_payment.py`
- `addons/account_payment/models/account_payment_method.py`
- `addons/account_payment/models/account_payment_method_line.py`
- `addons/account_payment/models/payment_provider.py`
- `addons/account_payment/models/payment_transaction.py`
- `addons/account_payment/security/ir.access.csv`
- `addons/account_payment/static/src/interactions/payment_form.js`
- `addons/account_payment/static/src/interactions/portal_invoice_page_payment.js`
- `addons/account_payment/static/src/interactions/portal_my_invoices_payment_list.js`
- `addons/account_payment/static/tests/interactions/portal_invoice_page_payment.test.js`
- `addons/account_payment/tests/__init__.py`
- `addons/account_payment/tests/common.py`
- `addons/account_payment/tests/test_account_payment.py`
- `addons/account_payment/tests/test_payment_flows.py`
- `addons/account_payment/tests/test_payment_provider.py`
- `addons/account_payment/views/account_journal_views.xml`
- `addons/account_payment/views/account_move_views.xml`
- `addons/account_payment/views/account_payment_menus.xml`
- `addons/account_payment/views/account_payment_views.xml`
- `addons/account_payment/views/account_portal_templates.xml`
- `addons/account_payment/views/payment_form_templates.xml`
- `addons/account_payment/views/payment_provider_views.xml`
- `addons/account_payment/views/payment_transaction_views.xml`
- `addons/account_payment/wizards/__init__.py`
- `addons/account_payment/wizards/account_payment_register.py`
- `addons/account_payment/wizards/account_payment_register_views.xml`
- `addons/account_payment/wizards/payment_link_wizard.py`
- `addons/account_payment/wizards/payment_link_wizard_views.xml`
- `addons/account_payment/wizards/payment_refund_wizard.py`
- `addons/account_payment/wizards/payment_refund_wizard_views.xml`
- `addons/account_payment/wizards/res_config_settings.py`
- `addons/account_payment/wizards/res_config_settings_views.xml`
