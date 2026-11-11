# Module: sale_expense

- **Module ID:** MOD-512
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/sale_expense`
- **Manifest:** `addons/sale_expense/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales/Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Quotation, Sales Orders, Delivery & Invoicing Control

**Manifest description:**

Reinvoice Employee Expense
==========================

Create some products for which you can re-invoice the costs.
This module allow to reinvoice employee expense, by setting the SO directly on the expense.

**Scope evidence:** The module contains 75 files, including 15 Python, 6 XML, and 1 JavaScript/TypeScript files. The manifest declares dependencies: `sale_management`, `hr_expense`.

## 2. Module structure

- Model/business logic files: 8
- Controller/API files: 0
- XML/data/view/template files: 6
- Browser asset files: 1
- Security files: 1
- Test files: 3
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/sale_expense/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 8 model declarations, 42 methods, 0 constraint handlers, 1 onchange handlers, and 10 dependency declarations.
- **Evidence:** `addons/sale_expense/models/sale_order.py:8`, `addons/sale_expense/models/product_template.py:7`, `addons/sale_expense/models/hr_expense_split.py:6`, `addons/sale_expense/models/hr_expense.py:6`, `addons/sale_expense/models/account_move.py:6`, `addons/sale_expense/models/account_move_line.py:6`, `addons/sale_expense/models/sale_order_line.py:6`, `addons/sale_expense/wizard/expense_attachment_selection_wizard.py:5`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 6 XML files and 1 JavaScript/TypeScript files; static XML analysis found 10 record/template/menu identifiers.
- **Evidence:** `addons/sale_expense/wizard/expense_attachment_selection_wizard_views.xml:4`, `addons/sale_expense/views/sale_order_views.xml:4`, `addons/sale_expense/views/sale_order_views.xml:31`, `addons/sale_expense/views/product_view.xml:4`, `addons/sale_expense/views/product_view.xml:28`, `addons/sale_expense/views/product_view.xml:40`, `addons/sale_expense/views/hr_expense_views.xml:3`, `addons/sale_expense/views/hr_expense_views.xml:38`, `addons/sale_expense/views/hr_expense_views.xml:50`, `addons/sale_expense/views/hr_expense_views.xml:62`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/sale_expense/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 3 test files are present.
- **Evidence:** `addons/sale_expense/tests/test_reinvoice.py`, `addons/sale_expense/tests/test_sale_expense.py`, `addons/sale_expense/tests/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 6; representative identifiers: `expense_attachment_selection_wizard_view`, `sale_order_form_view_inherit`, `sale_order_reinvoice_tree_view`, `product_product_view_form_inherit_sale_expense`, `product_product_view_list_inherit_sale_expense`, `hr_expense.hr_expense_product`, `hr_expense_form_view_inherit_sale_expense`, `hr_expense_tree_view_inherit_sale_expense`, `hr_expense_split_view_inherit_sale_expense`, `hr_expense_action_from_sale_order`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 18; representative evidence: `addons/sale_expense/wizard/expense_attachment_selection_wizard_views.xml:6`, `addons/sale_expense/wizard/expense_attachment_selection_wizard_views.xml:7`, `addons/sale_expense/views/sale_order_views.xml:6`, `addons/sale_expense/views/sale_order_views.xml:8`, `addons/sale_expense/views/sale_order_views.xml:33`, `addons/sale_expense/views/sale_order_views.xml:37`, `addons/sale_expense/views/product_view.xml:6`, `addons/sale_expense/views/product_view.xml:8`, `addons/sale_expense/views/product_view.xml:30`, `addons/sale_expense/views/product_view.xml:32`, `addons/sale_expense/views/hr_expense_views.xml:5`, `addons/sale_expense/views/hr_expense_views.xml:8`
- Browser assets: 1; representative files: `addons/sale_expense/static/src/views/attachment_selector.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/sale_expense/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 8
- Representative model evidence: inherits `sale.order` (addons/sale_expense/models/sale_order.py:8); inherits `product.template` (addons/sale_expense/models/product_template.py:7); inherits `hr.expense.split` (addons/sale_expense/models/hr_expense_split.py:6); inherits `hr.expense` (addons/sale_expense/models/hr_expense.py:6); inherits `account.move` (addons/sale_expense/models/account_move.py:6); inherits `account.move.line` (addons/sale_expense/models/account_move_line.py:6); inherits `sale.order.line` (addons/sale_expense/models/sale_order_line.py:6); `expense.attachment.selection.wizard` (addons/sale_expense/wizard/expense_attachment_selection_wizard.py:5)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `sale_management`, `hr_expense`
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

- `addons/sale_expense/__init__.py`
- `addons/sale_expense/__manifest__.py`
- `addons/sale_expense/data/sale_expense_data.xml`
- `addons/sale_expense/i18n/ar.po`
- `addons/sale_expense/i18n/az.po`
- `addons/sale_expense/i18n/bg.po`
- `addons/sale_expense/i18n/bs.po`
- `addons/sale_expense/i18n/ca.po`
- `addons/sale_expense/i18n/cs.po`
- `addons/sale_expense/i18n/da.po`
- `addons/sale_expense/i18n/de.po`
- `addons/sale_expense/i18n/el.po`
- `addons/sale_expense/i18n/es.po`
- `addons/sale_expense/i18n/es_419.po`
- `addons/sale_expense/i18n/et.po`
- `addons/sale_expense/i18n/fa.po`
- `addons/sale_expense/i18n/fi.po`
- `addons/sale_expense/i18n/fr.po`
- `addons/sale_expense/i18n/gu.po`
- `addons/sale_expense/i18n/he.po`
- `addons/sale_expense/i18n/hi.po`
- `addons/sale_expense/i18n/hr.po`
- `addons/sale_expense/i18n/hu.po`
- `addons/sale_expense/i18n/id.po`
- `addons/sale_expense/i18n/is.po`
- `addons/sale_expense/i18n/it.po`
- `addons/sale_expense/i18n/ja.po`
- `addons/sale_expense/i18n/kab.po`
- `addons/sale_expense/i18n/km.po`
- `addons/sale_expense/i18n/ko.po`
- `addons/sale_expense/i18n/ku.po`
- `addons/sale_expense/i18n/lo.po`
- `addons/sale_expense/i18n/lt.po`
- `addons/sale_expense/i18n/lv.po`
- `addons/sale_expense/i18n/mn.po`
- `addons/sale_expense/i18n/my.po`
- `addons/sale_expense/i18n/nb.po`
- `addons/sale_expense/i18n/nl.po`
- `addons/sale_expense/i18n/pl.po`
- `addons/sale_expense/i18n/pt.po`
- `addons/sale_expense/i18n/pt_BR.po`
- `addons/sale_expense/i18n/ro.po`
- `addons/sale_expense/i18n/ru.po`
- `addons/sale_expense/i18n/sale_expense.pot`
- `addons/sale_expense/i18n/sk.po`
- `addons/sale_expense/i18n/sl.po`
- `addons/sale_expense/i18n/sr@latin.po`
- `addons/sale_expense/i18n/sv.po`
- `addons/sale_expense/i18n/th.po`
- `addons/sale_expense/i18n/tr.po`
- `addons/sale_expense/i18n/uk.po`
- `addons/sale_expense/i18n/uz.po`
- `addons/sale_expense/i18n/vi.po`
- `addons/sale_expense/i18n/zh_CN.po`
- `addons/sale_expense/i18n/zh_TW.po`
- `addons/sale_expense/models/__init__.py`
- `addons/sale_expense/models/account_move.py`
- `addons/sale_expense/models/account_move_line.py`
- `addons/sale_expense/models/hr_expense.py`
- `addons/sale_expense/models/hr_expense_split.py`
- `addons/sale_expense/models/product_template.py`
- `addons/sale_expense/models/sale_order.py`
- `addons/sale_expense/models/sale_order_line.py`
- `addons/sale_expense/security/ir.access.csv`
- `addons/sale_expense/static/src/views/attachment_selector.js`
- `addons/sale_expense/static/src/views/attachment_selector.xml`
- `addons/sale_expense/tests/__init__.py`
- `addons/sale_expense/tests/test_reinvoice.py`
- `addons/sale_expense/tests/test_sale_expense.py`
- `addons/sale_expense/views/hr_expense_views.xml`
- `addons/sale_expense/views/product_view.xml`
- `addons/sale_expense/views/sale_order_views.xml`
- `addons/sale_expense/wizard/__init__.py`
- `addons/sale_expense/wizard/expense_attachment_selection_wizard.py`
- `addons/sale_expense/wizard/expense_attachment_selection_wizard_views.xml`
