# Module: hr_expense

- **Module ID:** MOD-086
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/hr_expense`
- **Manifest:** `addons/hr_expense/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `True`
- **Category:** `Human Resources/Expenses`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Submit, validate and reinvoice employee expenses

**Manifest description:**

Manage expenses by Employees
============================

This application allows you to manage your employees' daily expenses. It gives you access to your employees’ fee notes and give you the right to complete and validate or refuse the notes. After validation it creates an invoice for the employee.
Employee can encode their own expenses and the validation flow puts it automatically in the accounting after validation by managers.


The whole flow is implemented as:
---------------------------------
* Draft expense
* Submitted by the employee to his manager
* Approved by his manager
* Validation by the accountant and accounting entries creation

This module also uses analytic accounting and is compatible with the invoice on timesheet module so that you are able to automatically re-invoice your customers' expenses if your work by project.

**Scope evidence:** The module contains 161 files, including 38 Python, 27 XML, and 14 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `web_tour`, `hr`.

## 2. Module structure

- Model/business logic files: 24
- Controller/API files: 2
- XML/data/view/template files: 27
- Browser asset files: 14
- Security files: 2
- Test files: 9
- Scheduled/automation evidence files: 0
- Reporting evidence files: 2

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/hr_expense/security/ir.access.csv`, `addons/hr_expense/security/hr_expense_security.xml`

## 4. Functionalities

### Model and business logic

- **Description:** 24 model declarations, 264 methods, 6 constraint handlers, 5 onchange handlers, and 49 dependency declarations.
- **Evidence:** `addons/hr_expense/models/product_product.py:4`, `addons/hr_expense/models/hr_expense_product_job_position_limit.py:5`, `addons/hr_expense/models/product_template.py:6`, `addons/hr_expense/models/res_config_settings.py:4`, `addons/hr_expense/models/hr_employee_public.py:5`, `addons/hr_expense/models/hr_department.py:6`, `addons/hr_expense/models/account_payment.py:7`, `addons/hr_expense/models/analytic.py:9`, `addons/hr_expense/models/analytic.py:27`, `addons/hr_expense/models/ir_actions_report.py:9`, `addons/hr_expense/models/account_journal.py:6`, `addons/hr_expense/models/account_tax.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 0 route declarations.
- **Evidence:** `addons/hr_expense/controllers/webmanifest.py`, `addons/hr_expense/controllers/__init__.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 27 XML files and 14 JavaScript/TypeScript files; static XML analysis found 118 record/template/menu identifiers.
- **Evidence:** `addons/hr_expense/security/hr_expense_security.xml:3`, `addons/hr_expense/security/hr_expense_security.xml:10`, `addons/hr_expense/security/hr_expense_security.xml:17`, `addons/hr_expense/security/hr_expense_security.xml:24`, `addons/hr_expense/report/hr_expense_report.xml:106`, `addons/hr_expense/report/hr_expense_report.xml:116`, `addons/hr_expense/report/hr_expense_report.xml:3`, `addons/hr_expense/report/hr_expense_report.xml:92`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:3`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:28`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:3`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:20`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 2 security-directory files are present.
- **Evidence:** `addons/hr_expense/security/ir.access.csv`, `addons/hr_expense/security/hr_expense_security.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 2 files contain report-action/template indicators.
- **Evidence:** `addons/hr_expense/models/ir_actions_report.py`, `addons/hr_expense/report/hr_expense_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 9 test files are present.
- **Evidence:** `addons/hr_expense/tests/test_expenses_mail_import.py`, `addons/hr_expense/tests/test_expenses_access_rights.py`, `addons/hr_expense/tests/test_expense_job_position_limits.py`, `addons/hr_expense/tests/common.py`, `addons/hr_expense/tests/test_ui.py`, `addons/hr_expense/tests/test_expenses_tour.py`, `addons/hr_expense/tests/test_expenses_states.py`, `addons/hr_expense/tests/__init__.py`, `addons/hr_expense/tests/test_expenses.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 27; representative identifiers: `res_groups_privilege_expenses`, `group_hr_expense_team_approver`, `group_hr_expense_user`, `group_hr_expense_manager`, `action_report_hr_expense`, `action_report_expense_img`, `report_expense`, `report_expense_img`, `hr_expense_approve_duplicate_view_form`, `hr_expense_approve_duplicate_action`, `hr_expense_refuse_wizard_view_form`, `hr_expense_refuse_wizard_action`, `hr_expense_split`, `digest_tip_hr_expense_0`, `mail_act_expense_approval`, `mt_expense_approved`, `mt_expense_refused`, `mt_expense_paid`, `mt_expense_reset`, `mt_expense_entry_delete`
- Menus: 10; representative evidence: `addons/hr_expense/views/res_config_settings_views.xml:85`, `addons/hr_expense/views/hr_expense_views.xml:710`, `addons/hr_expense/views/hr_expense_views.xml:712`, `addons/hr_expense/views/hr_expense_views.xml:713`, `addons/hr_expense/views/hr_expense_views.xml:715`, `addons/hr_expense/views/hr_expense_views.xml:718`, `addons/hr_expense/views/hr_expense_views.xml:720`, `addons/hr_expense/views/hr_expense_views.xml:723`, `addons/hr_expense/views/hr_expense_views.xml:725`, `addons/hr_expense/views/mail_activity_views.xml:11`
- Templates: 6; representative evidence: `addons/hr_expense/report/hr_expense_report.xml:3`, `addons/hr_expense/report/hr_expense_report.xml:92`, `addons/hr_expense/data/mail_templates.xml:4`, `addons/hr_expense/data/mail_templates.xml:11`, `addons/hr_expense/data/mail_templates.xml:35`, `addons/hr_expense/data/mail_templates.xml:88`
- View/action field declarations: 110; representative evidence: `addons/hr_expense/report/hr_expense_report.xml:108`, `addons/hr_expense/report/hr_expense_report.xml:118`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:4`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:5`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:30`, `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml:31`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:5`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:6`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:22`, `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml:23`, `addons/hr_expense/wizard/hr_expense_split_wizard_views.xml:6`, `addons/hr_expense/wizard/hr_expense_split_wizard_views.xml:7`
- Browser assets: 14; representative files: `addons/hr_expense/static/src/mixins/document_upload.js`, `addons/hr_expense/static/src/components/expense_dashboard.js`, `addons/hr_expense/static/src/components/nb_attachment.js`, `addons/hr_expense/static/src/components/attachment_view.js`, `addons/hr_expense/static/src/components/hr_expense_product_form_view.js`, `addons/hr_expense/static/src/views/kanban.js`, `addons/hr_expense/static/src/views/list.js`, `addons/hr_expense/static/src/views/expense_form_view.js`, `addons/hr_expense/static/src/js/web/activity_menu_patch.js`, `addons/hr_expense/static/src/js/tours/hr_expense.js`, `addons/hr_expense/static/src/webclient/share_target/expense_share_target_item.js`, `addons/hr_expense/static/tests/tours/expense_product_tours.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/hr_expense/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/hr_expense/models/ir_actions_report.py`, `addons/hr_expense/report/hr_expense_report.xml`

## 7. Database interactions

- Model declarations: 24
- Representative model evidence: inherits `product.product` (addons/hr_expense/models/product_product.py:4); `hr.expense.product.job.position.limit` (addons/hr_expense/models/hr_expense_product_job_position_limit.py:5); inherits `product.template` (addons/hr_expense/models/product_template.py:6); inherits `res.config.settings` (addons/hr_expense/models/res_config_settings.py:4); inherits `hr.employee.public` (addons/hr_expense/models/hr_employee_public.py:5); inherits `hr.department` (addons/hr_expense/models/hr_department.py:6); inherits `account.payment` (addons/hr_expense/models/account_payment.py:7); inherits `account.analytic.applicability` (addons/hr_expense/models/analytic.py:9); inherits `account.analytic.account` (addons/hr_expense/models/analytic.py:27); inherits `ir.actions.report` (addons/hr_expense/models/ir_actions_report.py:9); inherits `account.journal` (addons/hr_expense/models/account_journal.py:6); inherits `account.tax` (addons/hr_expense/models/account_tax.py:4); `hr.expense` (addons/hr_expense/models/hr_expense.py:26); inherits `account.move` (addons/hr_expense/models/account_move.py:7); inherits `account.move.line` (addons/hr_expense/models/account_move_line.py:7); inherits `hr.employee` (addons/hr_expense/models/hr_employee.py:7); inherits `hr.employee.public` (addons/hr_expense/models/hr_employee.py:77); inherits `ir.attachment` (addons/hr_expense/models/ir_attachment.py:7); inherits `res.company` (addons/hr_expense/models/res_company.py:7); `hr.expense.refuse.wizard` (addons/hr_expense/wizard/hr_expense_refuse_reason.py:6); `hr.expense.split.wizard` (addons/hr_expense/wizard/hr_expense_split_wizard.py:6); `hr.expense.split` (addons/hr_expense/wizard/hr_expense_split.py:10); `hr.expense.approve.duplicate` (addons/hr_expense/wizard/hr_expense_approve_duplicate.py:6); inherits `account.payment.register` (addons/hr_expense/wizard/account_payment_register.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `web_tour`, `hr`
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

- `addons/hr_expense/__init__.py`
- `addons/hr_expense/__manifest__.py`
- `addons/hr_expense/controllers/__init__.py`
- `addons/hr_expense/controllers/webmanifest.py`
- `addons/hr_expense/data/digest_data.xml`
- `addons/hr_expense/data/hr_expense_data.xml`
- `addons/hr_expense/data/hr_expense_demo.xml`
- `addons/hr_expense/data/hr_expense_tour.xml`
- `addons/hr_expense/data/mail_activity_type_data.xml`
- `addons/hr_expense/data/mail_alias_data.xml`
- `addons/hr_expense/data/mail_message_subtype_data.xml`
- `addons/hr_expense/data/mail_templates.xml`
- `addons/hr_expense/i18n/af.po`
- `addons/hr_expense/i18n/am.po`
- `addons/hr_expense/i18n/ar.po`
- `addons/hr_expense/i18n/az.po`
- `addons/hr_expense/i18n/bg.po`
- `addons/hr_expense/i18n/bs.po`
- `addons/hr_expense/i18n/ca.po`
- `addons/hr_expense/i18n/cs.po`
- `addons/hr_expense/i18n/da.po`
- `addons/hr_expense/i18n/de.po`
- `addons/hr_expense/i18n/el.po`
- `addons/hr_expense/i18n/en_AU.po`
- `addons/hr_expense/i18n/es.po`
- `addons/hr_expense/i18n/es_419.po`
- `addons/hr_expense/i18n/es_CL.po`
- `addons/hr_expense/i18n/et.po`
- `addons/hr_expense/i18n/eu.po`
- `addons/hr_expense/i18n/fa.po`
- `addons/hr_expense/i18n/fi.po`
- `addons/hr_expense/i18n/fo.po`
- `addons/hr_expense/i18n/fr.po`
- `addons/hr_expense/i18n/fr_BE.po`
- `addons/hr_expense/i18n/fr_CA.po`
- `addons/hr_expense/i18n/gl.po`
- `addons/hr_expense/i18n/gu.po`
- `addons/hr_expense/i18n/he.po`
- `addons/hr_expense/i18n/hi.po`
- `addons/hr_expense/i18n/hr.po`
- `addons/hr_expense/i18n/hr_expense.pot`
- `addons/hr_expense/i18n/hu.po`
- `addons/hr_expense/i18n/id.po`
- `addons/hr_expense/i18n/is.po`
- `addons/hr_expense/i18n/it.po`
- `addons/hr_expense/i18n/ja.po`
- `addons/hr_expense/i18n/ka.po`
- `addons/hr_expense/i18n/kab.po`
- `addons/hr_expense/i18n/km.po`
- `addons/hr_expense/i18n/ko.po`
- `addons/hr_expense/i18n/ku.po`
- `addons/hr_expense/i18n/lb.po`
- `addons/hr_expense/i18n/lo.po`
- `addons/hr_expense/i18n/lt.po`
- `addons/hr_expense/i18n/lv.po`
- `addons/hr_expense/i18n/mk.po`
- `addons/hr_expense/i18n/mn.po`
- `addons/hr_expense/i18n/my.po`
- `addons/hr_expense/i18n/nb.po`
- `addons/hr_expense/i18n/nl.po`
- `addons/hr_expense/i18n/pl.po`
- `addons/hr_expense/i18n/pt.po`
- `addons/hr_expense/i18n/pt_BR.po`
- `addons/hr_expense/i18n/ro.po`
- `addons/hr_expense/i18n/ru.po`
- `addons/hr_expense/i18n/sk.po`
- `addons/hr_expense/i18n/sl.po`
- `addons/hr_expense/i18n/sq.po`
- `addons/hr_expense/i18n/sr@latin.po`
- `addons/hr_expense/i18n/sv.po`
- `addons/hr_expense/i18n/ta.po`
- `addons/hr_expense/i18n/te.po`
- `addons/hr_expense/i18n/th.po`
- `addons/hr_expense/i18n/tr.po`
- `addons/hr_expense/i18n/uk.po`
- `addons/hr_expense/i18n/uz.po`
- `addons/hr_expense/i18n/vi.po`
- `addons/hr_expense/i18n/zh_CN.po`
- `addons/hr_expense/i18n/zh_TW.po`
- `addons/hr_expense/migrations/2.1/pre-migrate.py`
- `addons/hr_expense/models/__init__.py`
- `addons/hr_expense/models/account_journal.py`
- `addons/hr_expense/models/account_move.py`
- `addons/hr_expense/models/account_move_line.py`
- `addons/hr_expense/models/account_payment.py`
- `addons/hr_expense/models/account_tax.py`
- `addons/hr_expense/models/analytic.py`
- `addons/hr_expense/models/hr_department.py`
- `addons/hr_expense/models/hr_employee.py`
- `addons/hr_expense/models/hr_employee_public.py`
- `addons/hr_expense/models/hr_expense.py`
- `addons/hr_expense/models/hr_expense_product_job_position_limit.py`
- `addons/hr_expense/models/ir_actions_report.py`
- `addons/hr_expense/models/ir_attachment.py`
- `addons/hr_expense/models/product_product.py`
- `addons/hr_expense/models/product_template.py`
- `addons/hr_expense/models/res_company.py`
- `addons/hr_expense/models/res_config_settings.py`
- `addons/hr_expense/report/hr_expense_report.xml`
- `addons/hr_expense/security/hr_expense_security.xml`
- `addons/hr_expense/security/ir.access.csv`
- `addons/hr_expense/static/description/icon.png`
- `addons/hr_expense/static/description/icon.svg`
- `addons/hr_expense/static/description/icon_hi.png`
- `addons/hr_expense/static/img/app_store.png`
- `addons/hr_expense/static/img/communication.svg`
- `addons/hr_expense/static/img/food.svg`
- `addons/hr_expense/static/img/gift.svg`
- `addons/hr_expense/static/img/mileage.svg`
- `addons/hr_expense/static/img/nocontent.png`
- `addons/hr_expense/static/img/other.svg`
- `addons/hr_expense/static/img/play_store.png`
- `addons/hr_expense/static/img/transport.svg`
- `addons/hr_expense/static/src/components/attachment_view.js`
- `addons/hr_expense/static/src/components/expense_dashboard.js`
- `addons/hr_expense/static/src/components/expense_dashboard.xml`
- `addons/hr_expense/static/src/components/hr_expense_product_form_view.js`
- `addons/hr_expense/static/src/components/nb_attachment.js`
- `addons/hr_expense/static/src/components/nb_attachment.xml`
- `addons/hr_expense/static/src/img/milk-expense.png`
- `addons/hr_expense/static/src/js/tours/hr_expense.js`
- `addons/hr_expense/static/src/js/web/activity_menu_patch.js`
- `addons/hr_expense/static/src/mixins/document_upload.js`
- `addons/hr_expense/static/src/scss/hr_expense.scss`
- `addons/hr_expense/static/src/views/expense_form_view.js`
- `addons/hr_expense/static/src/views/kanban.js`
- `addons/hr_expense/static/src/views/kanban.xml`
- `addons/hr_expense/static/src/views/list.js`
- `addons/hr_expense/static/src/views/list.xml`
- `addons/hr_expense/static/src/webclient/share_target/expense_share_target_item.js`
- `addons/hr_expense/static/tests/tours/expense_form_tours.js`
- `addons/hr_expense/static/tests/tours/expense_product_tours.js`
- `addons/hr_expense/static/tests/tours/expense_upload_tours.js`
- `addons/hr_expense/tests/__init__.py`
- `addons/hr_expense/tests/common.py`
- `addons/hr_expense/tests/test_expense_job_position_limits.py`
- `addons/hr_expense/tests/test_expenses.py`
- `addons/hr_expense/tests/test_expenses_access_rights.py`
- `addons/hr_expense/tests/test_expenses_mail_import.py`
- `addons/hr_expense/tests/test_expenses_states.py`
- `addons/hr_expense/tests/test_expenses_tour.py`
- `addons/hr_expense/tests/test_ui.py`
- `addons/hr_expense/views/account_journal_dashboard_view.xml`
- `addons/hr_expense/views/account_move_views.xml`
- `addons/hr_expense/views/account_payment_views.xml`
- `addons/hr_expense/views/hr_department_views.xml`
- `addons/hr_expense/views/hr_employee_views.xml`
- `addons/hr_expense/views/hr_expense_split_views.xml`
- `addons/hr_expense/views/hr_expense_views.xml`
- `addons/hr_expense/views/mail_activity_views.xml`
- `addons/hr_expense/views/product_product_views.xml`
- `addons/hr_expense/views/res_config_settings_views.xml`
- `addons/hr_expense/wizard/__init__.py`
- `addons/hr_expense/wizard/account_payment_register.py`
- `addons/hr_expense/wizard/hr_expense_approve_duplicate.py`
- `addons/hr_expense/wizard/hr_expense_approve_duplicate_views.xml`
- `addons/hr_expense/wizard/hr_expense_refuse_reason.py`
- `addons/hr_expense/wizard/hr_expense_refuse_reason_views.xml`
- `addons/hr_expense/wizard/hr_expense_split.py`
- `addons/hr_expense/wizard/hr_expense_split_wizard.py`
- `addons/hr_expense/wizard/hr_expense_split_wizard_views.xml`
