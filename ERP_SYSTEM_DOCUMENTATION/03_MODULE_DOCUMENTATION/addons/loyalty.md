# Module: loyalty

- **Module ID:** MOD-349
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/loyalty`
- **Manifest:** `addons/loyalty/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Sales`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** Use discounts, gift cards, eWallets and loyalty programs in your sales channels

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 109 files, including 21 Python, 17 XML, and 5 JavaScript/TypeScript files. The manifest declares dependencies: `product`, `portal`, `account`.

## 2. Module structure

- Model/business logic files: 13
- Controller/API files: 2
- XML/data/view/template files: 17
- Browser asset files: 5
- Security files: 1
- Test files: 2
- Scheduled/automation evidence files: 0
- Reporting evidence files: 1

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/loyalty/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 13 model declarations, 131 methods, 9 constraint handlers, 0 onchange handlers, and 26 dependency declarations.
- **Evidence:** `addons/loyalty/models/res_partner.py:6`, `addons/loyalty/models/product_product.py:7`, `addons/loyalty/models/loyalty_reward.py:11`, `addons/loyalty/models/product_template.py:8`, `addons/loyalty/models/loyalty_program.py:14`, `addons/loyalty/models/loyalty_history.py:12`, `addons/loyalty/models/product_pricelist.py:7`, `addons/loyalty/models/loyalty_rule.py:10`, `addons/loyalty/models/loyalty_card.py:11`, `addons/loyalty/models/loyalty_mail.py:9`, `addons/loyalty/wizard/loyalty_generate_wizard.py:8`, `addons/loyalty/wizard/base_partner_merge.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 2 controller files and 3 route declarations.
- **Evidence:** `addons/loyalty/controllers/portal.py:11`, `addons/loyalty/controllers/portal.py:43`, `addons/loyalty/controllers/portal.py:93`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 17 XML files and 5 JavaScript/TypeScript files; static XML analysis found 51 record/template/menu identifiers.
- **Evidence:** `addons/loyalty/report/loyalty_report.xml:4`, `addons/loyalty/report/loyalty_report.xml:13`, `addons/loyalty/report/loyalty_report_templates.xml:3`, `addons/loyalty/report/loyalty_report_templates.xml:73`, `addons/loyalty/report/loyalty_report_templates.xml:82`, `addons/loyalty/report/loyalty_report_templates.xml:123`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:3`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:60`, `addons/loyalty/wizard/loyalty_card_update_balance_views.xml:4`, `addons/loyalty/data/loyalty_demo.xml:4`, `addons/loyalty/data/loyalty_demo.xml:12`, `addons/loyalty/data/loyalty_demo.xml:18`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/loyalty/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Reporting

- **Description:** 1 files contain report-action/template indicators.
- **Evidence:** `addons/loyalty/report/loyalty_report.xml`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 2 test files are present.
- **Evidence:** `addons/loyalty/tests/__init__.py`, `addons/loyalty/tests/test_loyalty.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 17; representative identifiers: `report_loyalty_card`, `report_gift_card`, `loyalty_report`, `loyalty_report_i18n`, `gift_card_report`, `gift_card_report_i18n`, `loyalty_generate_wizard_view_form`, `loyalty_generate_wizard_action`, `loyalty_card_update_balance_form`, `10_percent_with_code`, `10_percent_with_code_rule`, `10_percent_with_code_reward`, `3_cabinets_plus_1_free`, `3_cabinets_plus_1_free_rule`, `3_cabinets_plus_1_free_reward`, `10_percent_coupon`, `10_percent_coupon_rule`, `10_percent_coupon_reward`, `10_percent_coupon_communication`, `mail_template_gift_card`
- Menus: 0; representative evidence: Not found in module
- Templates: 7; representative evidence: `addons/loyalty/report/loyalty_report_templates.xml:3`, `addons/loyalty/report/loyalty_report_templates.xml:73`, `addons/loyalty/report/loyalty_report_templates.xml:82`, `addons/loyalty/report/loyalty_report_templates.xml:123`, `addons/loyalty/views/portal_templates.xml:2`, `addons/loyalty/views/portal_templates.xml:49`, `addons/loyalty/views/portal_templates.xml:94`
- View/action field declarations: 46; representative evidence: `addons/loyalty/report/loyalty_report.xml:6`, `addons/loyalty/report/loyalty_report.xml:15`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:5`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:6`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:62`, `addons/loyalty/wizard/loyalty_generate_wizard_views.xml:63`, `addons/loyalty/wizard/loyalty_card_update_balance_views.xml:6`, `addons/loyalty/wizard/loyalty_card_update_balance_views.xml:7`, `addons/loyalty/views/loyalty_reward_views.xml:5`, `addons/loyalty/views/loyalty_reward_views.xml:6`, `addons/loyalty/views/loyalty_reward_views.xml:74`, `addons/loyalty/views/loyalty_reward_views.xml:75`
- Browser assets: 5; representative files: `addons/loyalty/static/src/js/loyalty_list_view.js`, `addons/loyalty/static/src/js/loyalty_card_list_view.js`, `addons/loyalty/static/src/js/loyalty_control_panel_widget.js`, `addons/loyalty/static/src/interactions/loyalty_card.js`, `addons/loyalty/static/src/js/portal/loyalty_card_dialog/loyalty_card_dialog.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/loyalty/__manifest__.py`
- **HTTP entry points:** `addons/loyalty/controllers/portal.py:11`, `addons/loyalty/controllers/portal.py:43`, `addons/loyalty/controllers/portal.py:93`
- **Scheduled entry points:** Not found in module
- **Report entry points:** `addons/loyalty/report/loyalty_report.xml`

## 7. Database interactions

- Model declarations: 13
- Representative model evidence: inherits `res.partner` (addons/loyalty/models/res_partner.py:6); inherits `product.product` (addons/loyalty/models/product_product.py:7); `loyalty.reward` (addons/loyalty/models/loyalty_reward.py:11); inherits `product.template` (addons/loyalty/models/product_template.py:8); `loyalty.program` (addons/loyalty/models/loyalty_program.py:14); `loyalty.history` (addons/loyalty/models/loyalty_history.py:12); inherits `product.pricelist` (addons/loyalty/models/product_pricelist.py:7); `loyalty.rule` (addons/loyalty/models/loyalty_rule.py:10); `loyalty.card` (addons/loyalty/models/loyalty_card.py:11); `loyalty.mail` (addons/loyalty/models/loyalty_mail.py:9); `loyalty.generate.wizard` (addons/loyalty/wizard/loyalty_generate_wizard.py:8); inherits `base.partner.merge.automatic.wizard` (addons/loyalty/wizard/base_partner_merge.py:4); `loyalty.card.update.balance` (addons/loyalty/wizard/loyalty_card_update_balance.py:7)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 2
- Route declarations: 3
- Route evidence: `addons/loyalty/controllers/portal.py:11`, `addons/loyalty/controllers/portal.py:43`, `addons/loyalty/controllers/portal.py:93`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `product`, `portal`, `account`
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

- `addons/loyalty/__init__.py`
- `addons/loyalty/__manifest__.py`
- `addons/loyalty/controllers/__init__.py`
- `addons/loyalty/controllers/portal.py`
- `addons/loyalty/data/loyalty_data.xml`
- `addons/loyalty/data/loyalty_demo.xml`
- `addons/loyalty/data/mail_template_data.xml`
- `addons/loyalty/i18n/ar.po`
- `addons/loyalty/i18n/az.po`
- `addons/loyalty/i18n/bg.po`
- `addons/loyalty/i18n/bs.po`
- `addons/loyalty/i18n/ca.po`
- `addons/loyalty/i18n/cs.po`
- `addons/loyalty/i18n/da.po`
- `addons/loyalty/i18n/de.po`
- `addons/loyalty/i18n/el.po`
- `addons/loyalty/i18n/es.po`
- `addons/loyalty/i18n/es_419.po`
- `addons/loyalty/i18n/et.po`
- `addons/loyalty/i18n/fa.po`
- `addons/loyalty/i18n/fi.po`
- `addons/loyalty/i18n/fr.po`
- `addons/loyalty/i18n/he.po`
- `addons/loyalty/i18n/hi.po`
- `addons/loyalty/i18n/hr.po`
- `addons/loyalty/i18n/hu.po`
- `addons/loyalty/i18n/id.po`
- `addons/loyalty/i18n/it.po`
- `addons/loyalty/i18n/ja.po`
- `addons/loyalty/i18n/kab.po`
- `addons/loyalty/i18n/ko.po`
- `addons/loyalty/i18n/ku.po`
- `addons/loyalty/i18n/lo.po`
- `addons/loyalty/i18n/loyalty.pot`
- `addons/loyalty/i18n/lt.po`
- `addons/loyalty/i18n/lv.po`
- `addons/loyalty/i18n/mn.po`
- `addons/loyalty/i18n/my.po`
- `addons/loyalty/i18n/nb.po`
- `addons/loyalty/i18n/nl.po`
- `addons/loyalty/i18n/pl.po`
- `addons/loyalty/i18n/pt.po`
- `addons/loyalty/i18n/pt_BR.po`
- `addons/loyalty/i18n/ro.po`
- `addons/loyalty/i18n/ru.po`
- `addons/loyalty/i18n/sk.po`
- `addons/loyalty/i18n/sl.po`
- `addons/loyalty/i18n/sr@latin.po`
- `addons/loyalty/i18n/sv.po`
- `addons/loyalty/i18n/th.po`
- `addons/loyalty/i18n/tr.po`
- `addons/loyalty/i18n/uk.po`
- `addons/loyalty/i18n/uz.po`
- `addons/loyalty/i18n/vi.po`
- `addons/loyalty/i18n/zh_CN.po`
- `addons/loyalty/i18n/zh_TW.po`
- `addons/loyalty/models/__init__.py`
- `addons/loyalty/models/loyalty_card.py`
- `addons/loyalty/models/loyalty_history.py`
- `addons/loyalty/models/loyalty_mail.py`
- `addons/loyalty/models/loyalty_program.py`
- `addons/loyalty/models/loyalty_reward.py`
- `addons/loyalty/models/loyalty_rule.py`
- `addons/loyalty/models/product_pricelist.py`
- `addons/loyalty/models/product_product.py`
- `addons/loyalty/models/product_template.py`
- `addons/loyalty/models/res_partner.py`
- `addons/loyalty/report/loyalty_report.xml`
- `addons/loyalty/report/loyalty_report_templates.xml`
- `addons/loyalty/security/ir.access.csv`
- `addons/loyalty/static/img/2_plus_1.svg`
- `addons/loyalty/static/img/coupons.svg`
- `addons/loyalty/static/img/discount_placeholder_thumbnail.png`
- `addons/loyalty/static/img/ewallet.svg`
- `addons/loyalty/static/img/fidelity_cards.svg`
- `addons/loyalty/static/img/gift_card.png`
- `addons/loyalty/static/img/gift_card.svg`
- `addons/loyalty/static/img/loyalty_cards.svg`
- `addons/loyalty/static/img/loyalty_cards_2.svg`
- `addons/loyalty/static/img/portal-loyalty.svg`
- `addons/loyalty/static/img/promo_code.svg`
- `addons/loyalty/static/img/promotional_program.svg`
- `addons/loyalty/static/src/img/ewallet.svg`
- `addons/loyalty/static/src/img/loyalty.svg`
- `addons/loyalty/static/src/interactions/loyalty_card.js`
- `addons/loyalty/static/src/js/loyalty_card_list_view.js`
- `addons/loyalty/static/src/js/loyalty_control_panel_widget.js`
- `addons/loyalty/static/src/js/loyalty_list_view.js`
- `addons/loyalty/static/src/js/portal/loyalty_card_dialog/loyalty_card_dialog.js`
- `addons/loyalty/static/src/js/portal/loyalty_card_dialog/loyalty_card_dialog.xml`
- `addons/loyalty/static/src/scss/loyalty.dark.scss`
- `addons/loyalty/static/src/scss/loyalty.scss`
- `addons/loyalty/static/src/xml/loyalty_templates.xml`
- `addons/loyalty/tests/__init__.py`
- `addons/loyalty/tests/test_loyalty.py`
- `addons/loyalty/views/loyalty_card_views.xml`
- `addons/loyalty/views/loyalty_history_views.xml`
- `addons/loyalty/views/loyalty_mail_views.xml`
- `addons/loyalty/views/loyalty_program_views.xml`
- `addons/loyalty/views/loyalty_reward_views.xml`
- `addons/loyalty/views/loyalty_rule_views.xml`
- `addons/loyalty/views/portal_templates.xml`
- `addons/loyalty/views/res_partner_views.xml`
- `addons/loyalty/wizard/__init__.py`
- `addons/loyalty/wizard/base_partner_merge.py`
- `addons/loyalty/wizard/loyalty_card_update_balance.py`
- `addons/loyalty/wizard/loyalty_card_update_balance_views.xml`
- `addons/loyalty/wizard/loyalty_generate_wizard.py`
- `addons/loyalty/wizard/loyalty_generate_wizard_views.xml`
