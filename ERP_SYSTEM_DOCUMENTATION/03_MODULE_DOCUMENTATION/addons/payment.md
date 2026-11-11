# Module: payment

- **Module ID:** MOD-392
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/payment`
- **Manifest:** `addons/payment/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Hidden`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** The payment engine used by payment provider modules.

**Manifest description:**

No manifest description declared

**Scope evidence:** The module contains 338 files, including 38 Python, 16 XML, and 7 JavaScript/TypeScript files. The manifest declares dependencies: `onboarding`, `portal`.

## 2. Module structure

- Model/business logic files: 14
- Controller/API files: 3
- XML/data/view/template files: 16
- Browser asset files: 7
- Security files: 1
- Test files: 14
- Scheduled/automation evidence files: 10
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** `addons/payment/security/ir.access.csv`

## 4. Functionalities

### Model and business logic

- **Description:** 14 model declarations, 402 methods, 6 constraint handlers, 4 onchange handlers, and 24 dependency declarations.
- **Evidence:** `addons/payment/models/res_partner.py:6`, `addons/payment/models/ir_websocket.py:8`, `addons/payment/models/portal_entry.py:6`, `addons/payment/models/payment_data.py:13`, `addons/payment/models/ir_http.py:6`, `addons/payment/models/payment_token.py:7`, `addons/payment/models/res_country.py:14`, `addons/payment/models/payment_transaction.py:23`, `addons/payment/models/payment_method.py:11`, `addons/payment/models/payment_provider.py:19`, `addons/payment/models/res_company.py:6`, `addons/payment/wizards/res_config_settings.py:7`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### HTTP/API surface

- **Description:** 3 controller files and 7 route declarations.
- **Evidence:** `addons/payment/controllers/portal.py:36`, `addons/payment/controllers/portal.py:156`, `addons/payment/controllers/portal.py:301`, `addons/payment/controllers/portal.py:468`, `addons/payment/controllers/portal.py:493`, `addons/payment/controllers/payment_status.py:24`, `addons/payment/controllers/payment_status.py:71`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 16 XML files and 7 JavaScript/TypeScript files; static XML analysis found 76 record/template/menu identifiers.
- **Evidence:** `addons/payment/wizards/payment_capture_wizard_views.xml:4`, `addons/payment/wizards/payment_link_wizard_views.xml:4`, `addons/payment/data/ir_actions_server_data.xml:4`, `addons/payment/data/ir_actions_server_data.xml:13`, `addons/payment/data/ir_actions_server_data.xml:22`, `addons/payment/data/payment_provider_data.xml:4`, `addons/payment/data/payment_provider_data.xml:10`, `addons/payment/data/payment_provider_data.xml:16`, `addons/payment/data/payment_provider_data.xml:22`, `addons/payment/data/payment_provider_data.xml:30`, `addons/payment/data/payment_provider_data.xml:38`, `addons/payment/data/payment_provider_data.xml:45`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Security

- **Description:** 1 security-directory files are present.
- **Evidence:** `addons/payment/security/ir.access.csv`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Scheduled/automation

- **Description:** 10 files contain cron, automation, or scheduled-action indicators.
- **Evidence:** `addons/payment/__manifest__.py`, `addons/payment/models/payment_data.py`, `addons/payment/models/payment_transaction.py`, `addons/payment/models/payment_provider.py`, `addons/payment/data/ir_actions_server_data.xml`, `addons/payment/data/ir_cron_data.xml`, `addons/payment/tests/common.py`, `addons/payment/tests/test_payment_data.py`, `addons/payment/tests/test_payment_provider.py`, `addons/payment/tests/test_payment_transaction.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### Automated verification

- **Description:** 14 test files are present.
- **Evidence:** `addons/payment/tests/http_common.py`, `addons/payment/tests/test_utils.py`, `addons/payment/tests/common.py`, `addons/payment/tests/test_payment_data.py`, `addons/payment/tests/test_payment_provider.py`, `addons/payment/tests/test_res_company.py`, `addons/payment/tests/test_payment_transaction.py`, `addons/payment/tests/test_flows.py`, `addons/payment/tests/__init__.py`, `addons/payment/tests/test_ir_websocket.py`, `addons/payment/tests/test_payment_token.py`, `addons/payment/tests/test_multicompany_flows.py`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 16; representative identifiers: `payment_capture_wizard_view_form`, `payment_link_wizard_view_form`, `action_start_payment_onboarding`, `action_confirm_payment_transaction`, `action_add_payment_method`, `payment_provider_adyen`, `payment_provider_aps`, `payment_provider_asiapay`, `payment_provider_authorize`, `payment_provider_buckaroo`, `payment_provider_demo`, `payment_provider_dpo`, `payment_provider_ecpay`, `payment_provider_flutterwave`, `payment_provider_iyzico`, `payment_provider_mercado_pago`, `payment_provider_mollie`, `payment_provider_nuvei`, `payment_provider_pay_on_invoice`, `payment_provider_paymob`
- Menus: 0; representative evidence: Not found in module
- Templates: 21; representative evidence: `addons/payment/views/portal_templates.xml:5`, `addons/payment/views/portal_templates.xml:72`, `addons/payment/views/portal_templates.xml:87`, `addons/payment/views/portal_templates.xml:107`, `addons/payment/views/portal_templates.xml:164`, `addons/payment/views/portal_templates.xml:226`, `addons/payment/views/portal_templates.xml:247`, `addons/payment/views/portal_templates.xml:271`, `addons/payment/views/express_checkout_templates.xml:4`, `addons/payment/views/payment_form_templates.xml:4`, `addons/payment/views/payment_form_templates.xml:129`, `addons/payment/views/payment_form_templates.xml:253`
- View/action field declarations: 49; representative evidence: `addons/payment/wizards/payment_capture_wizard_views.xml:6`, `addons/payment/wizards/payment_capture_wizard_views.xml:7`, `addons/payment/wizards/payment_link_wizard_views.xml:6`, `addons/payment/wizards/payment_link_wizard_views.xml:7`, `addons/payment/wizards/payment_link_wizard_views.xml:25`, `addons/payment/views/payment_token_views.xml:6`, `addons/payment/views/payment_token_views.xml:7`, `addons/payment/views/payment_token_views.xml:43`, `addons/payment/views/payment_token_views.xml:44`, `addons/payment/views/payment_token_views.xml:58`, `addons/payment/views/payment_token_views.xml:59`, `addons/payment/views/payment_token_views.xml:84`
- Browser assets: 7; representative files: `addons/payment/static/tests/payment_wizard_copy_clipboard_field.test.js`, `addons/payment/static/src/js/payment_wizard_copy_clipboard_field.js`, `addons/payment/static/src/interactions/express_checkout.js`, `addons/payment/static/src/interactions/payment_form.js`, `addons/payment/static/src/interactions/payment_button.js`, `addons/payment/static/src/interactions/payment_status.js`, `addons/payment/static/src/components/many2many_image_avatar/many2many_image_tags.js`
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/payment/__manifest__.py`
- **HTTP entry points:** `addons/payment/controllers/portal.py:36`, `addons/payment/controllers/portal.py:156`, `addons/payment/controllers/portal.py:301`, `addons/payment/controllers/portal.py:468`, `addons/payment/controllers/portal.py:493`, `addons/payment/controllers/payment_status.py:24`, `addons/payment/controllers/payment_status.py:71`
- **Scheduled entry points:** `addons/payment/__manifest__.py`, `addons/payment/models/payment_data.py`, `addons/payment/models/payment_transaction.py`, `addons/payment/models/payment_provider.py`, `addons/payment/data/ir_actions_server_data.xml`, `addons/payment/data/ir_cron_data.xml`, `addons/payment/tests/common.py`, `addons/payment/tests/test_payment_data.py`, `addons/payment/tests/test_payment_provider.py`, `addons/payment/tests/test_payment_transaction.py`
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 14
- Representative model evidence: inherits `res.partner` (addons/payment/models/res_partner.py:6); inherits `ir.websocket` (addons/payment/models/ir_websocket.py:8); inherits `portal.entry` (addons/payment/models/portal_entry.py:6); `payment.data` (addons/payment/models/payment_data.py:13); inherits `ir.http` (addons/payment/models/ir_http.py:6); `payment.token` (addons/payment/models/payment_token.py:7); inherits `res.country` (addons/payment/models/res_country.py:14); `payment.transaction` (addons/payment/models/payment_transaction.py:23); `payment.method` (addons/payment/models/payment_method.py:11); `payment.provider` (addons/payment/models/payment_provider.py:19); inherits `res.company` (addons/payment/models/res_company.py:6); inherits `res.config.settings` (addons/payment/wizards/res_config_settings.py:7); `payment.capture.wizard` (addons/payment/wizards/payment_capture_wizard.py:8); `payment.link.wizard` (addons/payment/wizards/payment_link_wizard.py:10)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 3
- Route declarations: 7
- Route evidence: `addons/payment/controllers/portal.py:36`, `addons/payment/controllers/portal.py:156`, `addons/payment/controllers/portal.py:301`, `addons/payment/controllers/portal.py:468`, `addons/payment/controllers/portal.py:493`, `addons/payment/controllers/payment_status.py:24`, `addons/payment/controllers/payment_status.py:71`
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `onboarding`, `portal`
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

- `addons/payment/__init__.py`
- `addons/payment/__manifest__.py`
- `addons/payment/const.py`
- `addons/payment/controllers/__init__.py`
- `addons/payment/controllers/payment_status.py`
- `addons/payment/controllers/portal.py`
- `addons/payment/data/ir_actions_server_data.xml`
- `addons/payment/data/ir_cron_data.xml`
- `addons/payment/data/neutralize.sql`
- `addons/payment/data/payment_provider_data.xml`
- `addons/payment/data/portal_entry_data.xml`
- `addons/payment/i18n/af.po`
- `addons/payment/i18n/am.po`
- `addons/payment/i18n/ar.po`
- `addons/payment/i18n/az.po`
- `addons/payment/i18n/bg.po`
- `addons/payment/i18n/bs.po`
- `addons/payment/i18n/ca.po`
- `addons/payment/i18n/cs.po`
- `addons/payment/i18n/da.po`
- `addons/payment/i18n/de.po`
- `addons/payment/i18n/el.po`
- `addons/payment/i18n/es.po`
- `addons/payment/i18n/es_419.po`
- `addons/payment/i18n/es_CL.po`
- `addons/payment/i18n/et.po`
- `addons/payment/i18n/eu.po`
- `addons/payment/i18n/fa.po`
- `addons/payment/i18n/fi.po`
- `addons/payment/i18n/fo.po`
- `addons/payment/i18n/fr.po`
- `addons/payment/i18n/fr_BE.po`
- `addons/payment/i18n/fr_CA.po`
- `addons/payment/i18n/gl.po`
- `addons/payment/i18n/gu.po`
- `addons/payment/i18n/he.po`
- `addons/payment/i18n/hi.po`
- `addons/payment/i18n/hr.po`
- `addons/payment/i18n/hu.po`
- `addons/payment/i18n/hy.po`
- `addons/payment/i18n/id.po`
- `addons/payment/i18n/is.po`
- `addons/payment/i18n/it.po`
- `addons/payment/i18n/ja.po`
- `addons/payment/i18n/ka.po`
- `addons/payment/i18n/kab.po`
- `addons/payment/i18n/kk.po`
- `addons/payment/i18n/km.po`
- `addons/payment/i18n/ko.po`
- `addons/payment/i18n/ku.po`
- `addons/payment/i18n/lb.po`
- `addons/payment/i18n/lo.po`
- `addons/payment/i18n/lt.po`
- `addons/payment/i18n/lv.po`
- `addons/payment/i18n/mk.po`
- `addons/payment/i18n/mn.po`
- `addons/payment/i18n/my.po`
- `addons/payment/i18n/nb.po`
- `addons/payment/i18n/nl.po`
- `addons/payment/i18n/payment.pot`
- `addons/payment/i18n/pl.po`
- `addons/payment/i18n/pt.po`
- `addons/payment/i18n/pt_BR.po`
- `addons/payment/i18n/ro.po`
- `addons/payment/i18n/ru.po`
- `addons/payment/i18n/sk.po`
- `addons/payment/i18n/sl.po`
- `addons/payment/i18n/sq.po`
- `addons/payment/i18n/sr@latin.po`
- `addons/payment/i18n/sv.po`
- `addons/payment/i18n/ta.po`
- `addons/payment/i18n/th.po`
- `addons/payment/i18n/tr.po`
- `addons/payment/i18n/uk.po`
- `addons/payment/i18n/uz.po`
- `addons/payment/i18n/vi.po`
- `addons/payment/i18n/zh_CN.po`
- `addons/payment/i18n/zh_TW.po`
- `addons/payment/logging.py`
- `addons/payment/models/__init__.py`
- `addons/payment/models/ir_http.py`
- `addons/payment/models/ir_websocket.py`
- `addons/payment/models/payment_data.py`
- `addons/payment/models/payment_method.py`
- `addons/payment/models/payment_provider.py`
- `addons/payment/models/payment_token.py`
- `addons/payment/models/payment_transaction.py`
- `addons/payment/models/portal_entry.py`
- `addons/payment/models/res_company.py`
- `addons/payment/models/res_country.py`
- `addons/payment/models/res_partner.py`
- `addons/payment/security/ir.access.csv`
- `addons/payment/static/description/icon.png`
- `addons/payment/static/description/icon.svg`
- `addons/payment/static/description/icon_hi.png`
- `addons/payment/static/img/7eleven.png`
- `addons/payment/static/img/abitab.png`
- `addons/payment/static/img/ach_direct_debit.png`
- `addons/payment/static/img/affirm.png`
- `addons/payment/static/img/afterpay.png`
- `addons/payment/static/img/afterpay_riverty.png`
- `addons/payment/static/img/akulaku.png`
- `addons/payment/static/img/alipay.png`
- `addons/payment/static/img/alipay_hk.png`
- `addons/payment/static/img/alipay_plus.png`
- `addons/payment/static/img/alma.png`
- `addons/payment/static/img/aman.png`
- `addons/payment/static/img/amazon_pay.png`
- `addons/payment/static/img/amex.png`
- `addons/payment/static/img/apple_pay.png`
- `addons/payment/static/img/appota.png`
- `addons/payment/static/img/argencard.png`
- `addons/payment/static/img/atome.png`
- `addons/payment/static/img/bacs_direct_debit.png`
- `addons/payment/static/img/bancnet.png`
- `addons/payment/static/img/banco_de_bogota.png`
- `addons/payment/static/img/banco_guayaquil.png`
- `addons/payment/static/img/banco_pichincha.png`
- `addons/payment/static/img/bancolombia.png`
- `addons/payment/static/img/bancontact.png`
- `addons/payment/static/img/bank.png`
- `addons/payment/static/img/bank_bca.png`
- `addons/payment/static/img/bank_permata.png`
- `addons/payment/static/img/becs_direct_debit.png`
- `addons/payment/static/img/belfius.png`
- `addons/payment/static/img/benefit.png`
- `addons/payment/static/img/bharatqr.png`
- `addons/payment/static/img/billease.png`
- `addons/payment/static/img/billink.png`
- `addons/payment/static/img/bizum.png`
- `addons/payment/static/img/blik.png`
- `addons/payment/static/img/bni.png`
- `addons/payment/static/img/boleto.png`
- `addons/payment/static/img/boost.png`
- `addons/payment/static/img/bri.png`
- `addons/payment/static/img/bsi.png`
- `addons/payment/static/img/cabal.png`
- `addons/payment/static/img/caixa.png`
- `addons/payment/static/img/card.png`
- `addons/payment/static/img/cash_app_pay.png`
- `addons/payment/static/img/cashalo.png`
- `addons/payment/static/img/cebuana.png`
- `addons/payment/static/img/cencosud.png`
- `addons/payment/static/img/cetelem.png`
- `addons/payment/static/img/cimb_niaga.png`
- `addons/payment/static/img/cirrus.png`
- `addons/payment/static/img/clearpay.png`
- `addons/payment/static/img/codensa.png`
- `addons/payment/static/img/cofidis.png`
- `addons/payment/static/img/contact.png`
- `addons/payment/static/img/cordial.png`
- `addons/payment/static/img/cordobesa.png`
- `addons/payment/static/img/cvs.png`
- `addons/payment/static/img/dana.png`
- `addons/payment/static/img/dankort.png`
- `addons/payment/static/img/davivienda.png`
- `addons/payment/static/img/diners.png`
- `addons/payment/static/img/discover.png`
- `addons/payment/static/img/duitnow.png`
- `addons/payment/static/img/elo.png`
- `addons/payment/static/img/enets.png`
- `addons/payment/static/img/eps.png`
- `addons/payment/static/img/facilito.png`
- `addons/payment/static/img/family_mart.png`
- `addons/payment/static/img/floa_bank.png`
- `addons/payment/static/img/flutterwave.png`
- `addons/payment/static/img/forsa.png`
- `addons/payment/static/img/fpx.png`
- `addons/payment/static/img/gcash.png`
- `addons/payment/static/img/google_pay.png`
- `addons/payment/static/img/gopay.png`
- `addons/payment/static/img/grabpay.png`
- `addons/payment/static/img/halan.png`
- `addons/payment/static/img/hi_life.png`
- `addons/payment/static/img/hipercard.png`
- `addons/payment/static/img/hoolah.png`
- `addons/payment/static/img/humm.png`
- `addons/payment/static/img/ideal.png`
- `addons/payment/static/img/ideal_wero.png`
- `addons/payment/static/img/in3.png`
- `addons/payment/static/img/ipass_money.png`
- `addons/payment/static/img/jcb.png`
- `addons/payment/static/img/jeniuspay.png`
- `addons/payment/static/img/jkopay.png`
- `addons/payment/static/img/kakaopay.png`
- `addons/payment/static/img/kbc.png`
- `addons/payment/static/img/kfh.png`
- `addons/payment/static/img/kiosk.png`
- `addons/payment/static/img/klarna.png`
- `addons/payment/static/img/knet.png`
- `addons/payment/static/img/kredivo.png`
- `addons/payment/static/img/lider.png`
- `addons/payment/static/img/linepay.png`
- `addons/payment/static/img/link.png`
- `addons/payment/static/img/linkaja.png`
- `addons/payment/static/img/mada.png`
- `addons/payment/static/img/maestro.png`
- `addons/payment/static/img/magna.png`
- `addons/payment/static/img/mandiri.png`
- `addons/payment/static/img/mastercard.png`
- `addons/payment/static/img/maya.png`
- `addons/payment/static/img/maybank.png`
- `addons/payment/static/img/mbway.png`
- `addons/payment/static/img/meeza.png`
- `addons/payment/static/img/mercado_livre.png`
- `addons/payment/static/img/mobile.png`
- `addons/payment/static/img/mobile_pay.png`
- `addons/payment/static/img/momo.png`
- `addons/payment/static/img/mpesa.png`
- `addons/payment/static/img/mtn-mobile-money.png`
- `addons/payment/static/img/multibanco.png`
- `addons/payment/static/img/mybank.png`
- `addons/payment/static/img/napas_card.png`
- `addons/payment/static/img/naps.png`
- `addons/payment/static/img/naranja.png`
- `addons/payment/static/img/nativa.png`
- `addons/payment/static/img/octopus.png`
- `addons/payment/static/img/ok_mart.png`
- `addons/payment/static/img/omannet.png`
- `addons/payment/static/img/ovo.png`
- `addons/payment/static/img/oxxopay.png`
- `addons/payment/static/img/p24.png`
- `addons/payment/static/img/pace.png`
- `addons/payment/static/img/pay_id.png`
- `addons/payment/static/img/pay_later.png`
- `addons/payment/static/img/paybright.png`
- `addons/payment/static/img/payconiq.png`
- `addons/payment/static/img/payme.png`
- `addons/payment/static/img/payment-methods.svg`
- `addons/payment/static/img/paynow.png`
- `addons/payment/static/img/paypal.png`
- `addons/payment/static/img/paypal_paylater.png`
- `addons/payment/static/img/paysafecard.png`
- `addons/payment/static/img/paytm.png`
- `addons/payment/static/img/paytrail.png`
- `addons/payment/static/img/pf_pay.png`
- `addons/payment/static/img/pix.png`
- `addons/payment/static/img/poli.png`
- `addons/payment/static/img/poste_pay.png`
- `addons/payment/static/img/premiumcard.png`
- `addons/payment/static/img/presto.png`
- `addons/payment/static/img/promptpay.png`
- `addons/payment/static/img/qris.png`
- `addons/payment/static/img/rabbit_line_pay.png`
- `addons/payment/static/img/ratepay.png`
- `addons/payment/static/img/redpagos.png`
- `addons/payment/static/img/revolut_pay.png`
- `addons/payment/static/img/rupay.png`
- `addons/payment/static/img/samsung_pay.png`
- `addons/payment/static/img/satispay.png`
- Additional source files not expanded in this page: 88; see `../../01_CODEBASE_ANALYSIS/Repository_Inventory.csv`.
