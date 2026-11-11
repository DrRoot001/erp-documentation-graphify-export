# ERP SYSTEM Module Hierarchy — Phase 2
## Classification method
Modules are grouped using the manifest `category` field first, then conservative name-prefix rules for uncategorized technical/localization modules. This is a documentation taxonomy, not an assertion that all modules are installed or enabled together. Every module remains linked to its manifest and evidence page.
**Total modules:** 666  
**Business/application flags:** 34  
**Core modules:** 19  
**External addon modules:** 647
## Accounting & Finance (45 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`account`](addons/account.md) | Accounting/Accounting | Invoices & Payments | 6 | 173 Python, 138 XML, 115 JS/TS, 80 tests, 2 security, 10 routes |
| [`account_check_printing`](addons/account_check_printing.md) | Accounting/Accounting | Check printing basic features | 1 | 12 Python, 5 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`account_debit_note`](addons/account_debit_note.md) | Accounting/Accounting | Debit Notes | 1 | 9 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`account_edi`](addons/account_edi.md) | Accounting/Accounting | Not declared | 1 | 16 Python, 4 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`account_edi_proxy_client`](addons/account_edi_proxy_client.md) | Accounting/Accounting | Not declared | 2 | 9 Python, 1 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`account_edi_ubl_cii`](addons/account_edi_ubl_cii.md) | Accounting/Accounting | Not declared | 1 | 73 Python, 198 XML, 0 JS/TS, 36 tests, 0 security, 0 routes |
| [`account_fleet`](addons/account_fleet.md) | Accounting/Accounting | Manage accounting with fleets | 2 | 14 Python, 6 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`account_payment`](addons/account_payment.md) | Accounting/Accounting | Enable customers to pay invoices on the portal and post payments when transactions are processed. | 2 | 23 Python, 14 XML, 4 JS/TS, 5 tests, 1 security, 5 routes |
| [`account_payment_custom`](addons/account_payment_custom.md) | Accounting/Payment Custom | Bridge between payment_custom and account_payment. | 2 | 15 Python, 2 XML, 0 JS/TS, 5 tests, 0 security, 0 routes |
| [`account_payment_interco`](addons/account_payment_interco.md) | Accounting/Accounting | Enable Intercompany payments to reconcile with their invoices on post. | 1 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`account_peppol`](addons/account_peppol.md) | Accounting/Accounting | This module is used to send/receive documents with Peppol | 2 | 37 Python, 15 XML, 7 JS/TS, 9 tests, 1 security, 5 routes |
| [`account_qr_code_emv`](addons/account_qr_code_emv.md) | Accounting/Payment | Not declared | 1 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`account_qr_code_sepa`](addons/account_qr_code_sepa.md) | Accounting/Payment | Not declared | 1 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`account_tax_python`](addons/account_tax_python.md) | Accounting/Accounting | Use python code to define taxes | 1 | 8 Python, 1 XML, 1 JS/TS, 3 tests, 0 security, 0 routes |
| [`account_test`](addons/account_test.md) | Accounting/Accounting | Not declared | 1 | 6 Python, 4 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`account_update_tax_tags`](addons/account_update_tax_tags.md) | Accounting/Accounting | Allow updating tax grids on existing entries | 1 | 6 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`analytic`](addons/analytic.md) | Accounting/Accounting | Not declared | 3 | 18 Python, 8 XML, 18 JS/TS, 6 tests, 2 security, 0 routes |
| [`payment_adyen`](addons/payment_adyen.md) | Accounting/Payment Providers | A Dutch payment provider covering Europe and the US. | 1 | 16 Python, 6 XML, 1 JS/TS, 4 tests, 0 security, 5 routes |
| [`payment_aps`](addons/payment_aps.md) | Accounting/Payment Providers | An Amazon payment provider covering the MENA region. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_asiapay`](addons/payment_asiapay.md) | Accounting/Payment Providers | An payment provider based in Hong Kong covering most Asian countries. | 1 | 13 Python, 3 XML, 0 JS/TS, 5 tests, 0 security, 2 routes |
| [`payment_authorize`](addons/payment_authorize.md) | Accounting/Payment Providers | An payment provider covering the US, Australia, and Canada. | 1 | 16 Python, 5 XML, 1 JS/TS, 6 tests, 0 security, 2 routes |
| [`payment_buckaroo`](addons/payment_buckaroo.md) | Accounting/Payment Providers | A Dutch payment provider covering several countries in Europe. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_custom`](addons/payment_custom.md) | Accounting/Payment Providers | A payment provider for custom flows like wire transfers. | 1 | 12 Python, 4 XML, 2 JS/TS, 4 tests, 0 security, 1 routes |
| [`payment_demo`](addons/payment_demo.md) | Accounting/Accounting | A payment provider for running fake payment flows for demo purposes. | 1 | 14 Python, 6 XML, 3 JS/TS, 4 tests, 0 security, 1 routes |
| [`payment_dpo`](addons/payment_dpo.md) | Accounting/Payment Providers | A Kenyan payment provider covering several African countries. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 1 routes |
| [`payment_ecpay`](addons/payment_ecpay.md) | Accounting/Payment Providers | A payment provider covering the Taiwanese market. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_flutterwave`](addons/payment_flutterwave.md) | Accounting/Payment Providers | A Nigerian payment provider covering several African countries. | 1 | 14 Python, 3 XML, 1 JS/TS, 5 tests, 0 security, 3 routes |
| [`payment_iyzico`](addons/payment_iyzico.md) | Accounting/Payment Providers | A payment provider covering Turkey. | 1 | 13 Python, 3 XML, 0 JS/TS, 5 tests, 0 security, 2 routes |
| [`payment_mercado_pago`](addons/payment_mercado_pago.md) | Accounting/Payment Providers | A payment provider covering several countries in Latin America. | 1 | 15 Python, 5 XML, 1 JS/TS, 5 tests, 0 security, 4 routes |
| [`payment_mollie`](addons/payment_mollie.md) | Accounting/Payment Providers | A Dutch payment provider covering several European countries. | 1 | 12 Python, 3 XML, 0 JS/TS, 3 tests, 0 security, 2 routes |
| [`payment_nuvei`](addons/payment_nuvei.md) | Accounting/Payment Providers | A payment provider covering Latin America. | 1 | 13 Python, 3 XML, 0 JS/TS, 5 tests, 0 security, 2 routes |
| [`payment_paymob`](addons/payment_paymob.md) | Accounting/Payment Providers | An Egyptian payment provider for the Middle East. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_paypal`](addons/payment_paypal.md) | Accounting/Payment Providers | An American payment provider for online payments all over the world. | 1 | 14 Python, 6 XML, 3 JS/TS, 3 tests, 0 security, 6 routes |
| [`payment_payu`](addons/payment_payu.md) | Accounting/Payment Providers | A payment provider covering India. | 1 | 14 Python, 4 XML, 0 JS/TS, 5 tests, 0 security, 3 routes |
| [`payment_razorpay`](addons/payment_razorpay.md) | Accounting/Payment Providers | A payment provider covering India. | 1 | 15 Python, 4 XML, 1 JS/TS, 5 tests, 0 security, 3 routes |
| [`payment_redsys`](addons/payment_redsys.md) | Accounting/Payment Providers | A payment provider covering the Spanish market. | 1 | 12 Python, 3 XML, 0 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_stripe`](addons/payment_stripe.md) | Accounting/Payment Providers | An Irish-American payment provider covering the US and many others. | 1 | 16 Python, 5 XML, 3 JS/TS, 5 tests, 0 security, 6 routes |
| [`payment_toss_payments`](addons/payment_toss_payments.md) | Accounting/Payment Providers | A payment provider covering the South Korea market | 1 | 12 Python, 4 XML, 1 JS/TS, 4 tests, 0 security, 3 routes |
| [`payment_worldline`](addons/payment_worldline.md) | Accounting/Payment Providers | A French payment provider covering several European countries. | 1 | 12 Python, 3 XML, 1 JS/TS, 4 tests, 0 security, 2 routes |
| [`payment_xendit`](addons/payment_xendit.md) | Accounting/Payment Providers | A payment provider for Indonesian and the Philippines. | 1 | 13 Python, 4 XML, 1 JS/TS, 5 tests, 0 security, 3 routes |
| [`pos_account_tax_python`](addons/pos_account_tax_python.md) | Accounting/Accounting | Not declared | 2 | 6 Python, 0 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`product_email_template`](addons/product_email_template.md) | Accounting/Accounting | Not declared | 1 | 7 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`project_account`](addons/project_account.md) | Accounting/Accounting | project profitability items computation | 2 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`snailmail_account`](addons/snailmail_account.md) | Hidden/Tools | Not declared | 2 | 13 Python, 1 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`spreadsheet_account`](addons/spreadsheet_account.md) | Accounting | Spreadsheet Accounting formulas | 2 | 12 Python, 0 XML, 17 JS/TS, 7 tests, 0 security, 0 routes |

## Accounting & Localization (234 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`l10n_account_edi_ubl_cii_tests`](addons/l10n_account_edi_ubl_cii_tests.md) | Accounting/Accounting | Not declared | 6 | 13 Python, 42 XML, 0 JS/TS, 11 tests, 0 security, 0 routes |
| [`l10n_account_withholding_tax`](addons/l10n_account_withholding_tax.md) | Accounting/Localizations | Not declared | 1 | 19 Python, 8 XML, 2 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_account_withholding_tax_pos`](addons/l10n_account_withholding_tax_pos.md) | Accounting/Localizations | Not declared | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ae`](addons/l10n_ae.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ae_pos`](addons/l10n_ae_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 4 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_anz_ubl_pint`](addons/l10n_anz_ubl_pint.md) | Accounting/Localizations/EDI | Not declared | 1 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_ar`](addons/l10n_ar.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 35 Python, 32 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`l10n_ar_pos`](addons/l10n_ar_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 10 Python, 2 XML, 6 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_ar_stock`](addons/l10n_ar_stock.md) | Accounting/Localizations | Not declared | 2 | 10 Python, 7 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_ar_website_sale`](addons/l10n_ar_website_sale.md) | Accounting/Localizations/Website | Not declared | 2 | 8 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_ar_withholding`](addons/l10n_ar_withholding.md) | Accounting/Localizations | Not declared | 3 | 19 Python, 5 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_at`](addons/l10n_at.md) | Accounting/Localizations/Account Charts | Austrian Standardized Charts & Tax | 3 | 6 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_au`](addons/l10n_au.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 7 Python, 16 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bd`](addons/l10n_bd.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 6 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_be`](addons/l10n_be.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 12 Python, 4 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_be_pos`](addons/l10n_be_pos.md) | Sales/Point of Sale | Link module between point_of_sale and l10n_be | 3 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_be_pos_restaurant`](addons/l10n_be_pos_restaurant.md) | Sales/Point of Sale | Not declared | 2 | 5 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_be_pos_sale`](addons/l10n_be_pos_sale.md) | Sales/Point of Sale | Link module between pos_sale and l10n_be | 2 | 6 Python, 0 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_bf`](addons/l10n_bf.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bg`](addons/l10n_bg.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bg_ledger`](addons/l10n_bg_ledger.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bh`](addons/l10n_bh.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 7 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_bh_pos`](addons/l10n_bh_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 6 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bj`](addons/l10n_bj.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_bo`](addons/l10n_bo.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_br`](addons/l10n_br.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 24 Python, 14 XML, 1 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_br_sales`](addons/l10n_br_sales.md) | Sales/Sales | Not declared | 2 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_br_website_sale`](addons/l10n_br_website_sale.md) | Sales/Sales | Not declared | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ca`](addons/l10n_ca.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 10 Python, 7 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_cd`](addons/l10n_cd.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cf`](addons/l10n_cf.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cg`](addons/l10n_cg.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ch`](addons/l10n_ch.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 25 Python, 11 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`l10n_ch_pos`](addons/l10n_ch_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 7 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_ci`](addons/l10n_ci.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cl`](addons/l10n_cl.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 20 Python, 17 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_cm`](addons/l10n_cm.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cn`](addons/l10n_cn.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 15 Python, 11 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_co`](addons/l10n_co.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 8 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_co_pos`](addons/l10n_co_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 8 Python, 1 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_cr`](addons/l10n_cr.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cy`](addons/l10n_cy.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_cz`](addons/l10n_cz.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 12 Python, 8 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_de`](addons/l10n_de.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 18 Python, 5 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_din5008`](addons/l10n_din5008.md) | Accounting/Localizations | Not declared | 1 | 7 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_din5008_expense`](addons/l10n_din5008_expense.md) | Accounting/Localizations | Not declared | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_din5008_purchase`](addons/l10n_din5008_purchase.md) | Accounting/Localizations | Not declared | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_din5008_repair`](addons/l10n_din5008_repair.md) | Accounting/Localizations | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_din5008_sale`](addons/l10n_din5008_sale.md) | Accounting/Localizations | Not declared | 2 | 2 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_din5008_stock`](addons/l10n_din5008_stock.md) | Accounting/Localizations | Not declared | 2 | 2 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_dk`](addons/l10n_dk.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 32 Python, 20 XML, 2 JS/TS, 5 tests, 1 security, 3 routes |
| [`l10n_dk_fik`](addons/l10n_dk_fik.md) | Accounting/Localizations | Use FIK Number as Payment reference | 1 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_do`](addons/l10n_do.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 9 Python, 8 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_dz`](addons/l10n_dz.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ec`](addons/l10n_ec.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 18 Python, 9 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_ec_sale`](addons/l10n_ec_sale.md) | Accounting/Localizations/Sale | Not declared | 2 | 9 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_ee`](addons/l10n_ee.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 9 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_eg`](addons/l10n_eg.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 4 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_eg_edi_eta`](addons/l10n_eg_edi_eta.md) | account | Egypt Tax Authority Invoice Integration | 1 | 24 Python, 11 XML, 1 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_eg_edi_pos`](addons/l10n_eg_edi_pos.md) | Accounting/Localizations/EDI | Submit POS receipts to the Egyptian Tax Authority | 2 | 17 Python, 5 XML, 6 JS/TS, 8 tests, 0 security, 0 routes |
| [`l10n_es`](addons/l10n_es.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 19 Python, 20 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_es_edi_facturae`](addons/l10n_es_edi_facturae.md) | Accounting/Localizations/EDI | Not declared | 2 | 17 Python, 24 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_es_edi_sii`](addons/l10n_es_edi_sii.md) | Accounting/Localizations/EDI | Not declared | 2 | 17 Python, 6 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`l10n_es_edi_tbai`](addons/l10n_es_edi_tbai.md) | Accounting/Localizations/EDI | Not declared | 2 | 24 Python, 29 XML, 0 JS/TS, 10 tests, 1 security, 0 routes |
| [`l10n_es_edi_tbai_pos`](addons/l10n_es_edi_tbai_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 13 Python, 3 XML, 5 JS/TS, 5 tests, 0 security, 0 routes |
| [`l10n_es_edi_verifactu`](addons/l10n_es_edi_verifactu.md) | Accounting/Localizations/EDI | Module for sending Spanish Veri*Factu XML to the AEAT | 2 | 22 Python, 10 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`l10n_es_edi_verifactu_pos`](addons/l10n_es_edi_verifactu_pos.md) | Accounting/Localizations/Point of Sale | Add Veri*Factu support to Point of Sale | 2 | 13 Python, 3 XML, 5 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_es_pos`](addons/l10n_es_pos.md) | Accounting/Localizations/Point of Sale | Spanish localization for Point of Sale | 2 | 14 Python, 3 XML, 6 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_es_website_sale`](addons/l10n_es_website_sale.md) | Accounting/Localizations/Website | Not declared | 2 | 12 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 1 routes |
| [`l10n_es_website_sale_id_type`](addons/l10n_es_website_sale_id_type.md) | Accounting/Localizations/Website | Let customers pick the type of their identification document at checkout | 1 | 8 Python, 1 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_et`](addons/l10n_et.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_eu_account_vies`](addons/l10n_eu_account_vies.md) | Accounting/Accounting | Not declared | 1 | 10 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 1 routes |
| [`l10n_eu_oss`](addons/l10n_eu_oss.md) | Accounting/Localizations | Not declared | 1 | 11 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_fi`](addons/l10n_fi.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 10 Python, 3 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_fi_sale`](addons/l10n_fi_sale.md) | Sales/Sales | Not declared | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_fr`](addons/l10n_fr.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 7 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_fr_account`](addons/l10n_fr_account.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 23 Python, 6 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`l10n_fr_facturx_chorus_pro`](addons/l10n_fr_facturx_chorus_pro.md) | Accounting/Localizations/EDI | Not declared | 3 | 9 Python, 5 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_fr_hr_holidays`](addons/l10n_fr_hr_holidays.md) | Human Resources/Time Off | Management of leaves for part-time workers in France | 1 | 10 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_fr_payment`](addons/l10n_fr_payment.md) | Not declared | Applies CAWL/Worldline branding rules for French companies. | 2 | 5 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_fr_pdp`](addons/l10n_fr_pdp.md) | Accounting/Localizations/EDI | Not declared | 3 | 43 Python, 48 XML, 2 JS/TS, 9 tests, 1 security, 2 routes |
| [`l10n_fr_pdp_penalty_rate`](addons/l10n_fr_pdp_penalty_rate.md) | Accounting/Localizations/EDI | Not declared | 1 | 11 Python, 2 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_fr_pdp_pos`](addons/l10n_fr_pdp_pos.md) | Accounting/Localizations/Reporting | Flux 10 e-reporting for POS | 2 | 7 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_fr_pos_cert`](addons/l10n_fr_pos_cert.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 16 Python, 8 XML, 11 JS/TS, 5 tests, 1 security, 0 routes |
| [`l10n_ga`](addons/l10n_ga.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gcc_invoice`](addons/l10n_gcc_invoice.md) | Accounting/Localizations | Not declared | 1 | 9 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_gcc_invoice_stock_account`](addons/l10n_gcc_invoice_stock_account.md) | Accounting/Localizations | Not declared | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gcc_pos`](addons/l10n_gcc_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 10 Python, 2 XML, 3 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_ge`](addons/l10n_ge.md) | Accounting/Localizations/Account Charts | Georgian accounting localization package | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gf`](addons/l10n_gf.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gn`](addons/l10n_gn.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gp`](addons/l10n_gp.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gq`](addons/l10n_gq.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gr`](addons/l10n_gr.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gr_edi`](addons/l10n_gr_edi.md) | Accounting/Localizations | Connect to myDATA API implementation for Greece | 2 | 21 Python, 16 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_gr_edi_delivery_note`](addons/l10n_gr_edi_delivery_note.md) | Accounting/Localizations | Transmit Greece myDATA EDI for Delivery Notes | 4 | 9 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_gr_edi_e_invoo`](addons/l10n_gr_edi_e_invoo.md) | Accounting/Localizations/EDI | Not declared | 2 | 10 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_gr_edi_e_invoo_bridge`](addons/l10n_gr_edi_e_invoo_bridge.md) | Accounting/Localizations/EDI | Not declared | 2 | 10 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_gt`](addons/l10n_gt.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 7 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_gw`](addons/l10n_gw.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_hk`](addons/l10n_hk.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 7 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_hn`](addons/l10n_hn.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_hr`](addons/l10n_hr.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_hr_edi`](addons/l10n_hr_edi.md) | Accounting/Localizations/Reporting | Not declared | 2 | 26 Python, 20 XML, 0 JS/TS, 6 tests, 1 security, 0 routes |
| [`l10n_hr_kuna`](addons/l10n_hr_kuna.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_hu`](addons/l10n_hu.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 7 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_hu_edi`](addons/l10n_hu_edi.md) | Accounting/Localizations/EDI | Not declared | 2 | 29 Python, 57 XML, 1 JS/TS, 10 tests, 1 security, 0 routes |
| [`l10n_id`](addons/l10n_id.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 15 Python, 5 XML, 0 JS/TS, 3 tests, 1 security, 1 routes |
| [`l10n_id_efaktur_coretax`](addons/l10n_id_efaktur_coretax.md) | Accounting/Localizations/EDI | Not declared | 1 | 17 Python, 10 XML, 0 JS/TS, 4 tests, 1 security, 1 routes |
| [`l10n_id_pos`](addons/l10n_id_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 8 Python, 0 XML, 4 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_id_pos_self_order_qris`](addons/l10n_id_pos_self_order_qris.md) | Sales/Point of Sale | Accept QRIS QR code payments in a kiosk. | 2 | 4 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ie`](addons/l10n_ie.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 7 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_il`](addons/l10n_il.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_in`](addons/l10n_in.md) | Accounting/Localizations/Account Charts | Not declared | 5 | 38 Python, 31 XML, 3 JS/TS, 9 tests, 2 security, 0 routes |
| [`l10n_in_boe`](addons/l10n_in_boe.md) | Accounting/Localizations | Not declared | 2 | 8 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_in_edi`](addons/l10n_in_edi.md) | Accounting/Localizations/EDI | Not declared | 1 | 15 Python, 6 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_in_ewaybill`](addons/l10n_in_ewaybill.md) | Accounting/Localizations | Not declared | 1 | 18 Python, 8 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_in_ewaybill_irn`](addons/l10n_in_ewaybill_irn.md) | Accounting/Localizations | Not declared | 2 | 6 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_in_ewaybill_stock`](addons/l10n_in_ewaybill_stock.md) | Accounting/Localizations/EDI | Not declared | 2 | 8 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_in_hr_holidays`](addons/l10n_in_hr_holidays.md) | Human Resources/Time Off | Leave Management of Indian Localization | 1 | 10 Python, 4 XML, 1 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_in_pos`](addons/l10n_in_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 27 Python, 13 XML, 14 JS/TS, 9 tests, 0 security, 0 routes |
| [`l10n_in_purchase_stock`](addons/l10n_in_purchase_stock.md) | Accounting/Localizations/Purchase | Get warehouse address if the bill is created from Purchase Order | 2 | 8 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_in_sale`](addons/l10n_in_sale.md) | Accounting/Localizations/Sale | Not declared | 2 | 10 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_in_sale_stock`](addons/l10n_in_sale_stock.md) | Accounting/Localizations/Sale | Get warehouse address if the invoice is created from Sale Order | 3 | 6 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_in_stock`](addons/l10n_in_stock.md) | Accounting/Localizations | Not declared | 3 | 5 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_iq`](addons/l10n_iq.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_it`](addons/l10n_it.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 15 Python, 12 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_it_edi`](addons/l10n_it_edi.md) | Accounting/Localizations/EDI | Not declared | 3 | 38 Python, 68 XML, 2 JS/TS, 14 tests, 1 security, 0 routes |
| [`l10n_it_edi_doi`](addons/l10n_it_edi_doi.md) | Accounting/Localizations | Not declared | 2 | 14 Python, 7 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_it_edi_sale`](addons/l10n_it_edi_sale.md) | Accounting/Localizations/EDI | Not declared | 2 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_it_stock_ddt`](addons/l10n_it_stock_ddt.md) | Accounting/Localizations/EDI | Not declared | 3 | 8 Python, 6 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_jo`](addons/l10n_jo.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_jo_edi`](addons/l10n_jo_edi.md) | Accounting/Localizations/EDI | Electronic Invoicing for Jordan UBL 2.1 | 2 | 15 Python, 14 XML, 1 JS/TS, 5 tests, 0 security, 0 routes |
| [`l10n_jo_edi_pos`](addons/l10n_jo_edi_pos.md) | Accounting/Localizations/EDI | Not declared | 2 | 16 Python, 6 XML, 6 JS/TS, 5 tests, 0 security, 0 routes |
| [`l10n_jp`](addons/l10n_jp.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 12 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_jp_ubl_pint`](addons/l10n_jp_ubl_pint.md) | Accounting/Localizations/EDI | Not declared | 1 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_ke`](addons/l10n_ke.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 8 Python, 6 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`l10n_ke_edi_tremol`](addons/l10n_ke_edi_tremol.md) | Accounting/Localizations/EDI | Kenya Tremol Device EDI Integration | 1 | 13 Python, 5 XML, 3 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_kh`](addons/l10n_kh.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_km`](addons/l10n_km.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_kr`](addons/l10n_kr.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 8 Python, 6 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_kr_sale`](addons/l10n_kr_sale.md) | Accounting/Localizations/Sale | Not declared | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_kw`](addons/l10n_kw.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_kz`](addons/l10n_kz.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_la`](addons/l10n_la.md) | Accounting/Localizations/Account Charts | Chart of accounts, VAT taxes and monthly VAT return for Laos | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_latam_check`](addons/l10n_latam_check.md) | Accounting/Localizations | Checks Management | 1 | 18 Python, 6 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`l10n_latam_invoice_document`](addons/l10n_latam_invoice_document.md) | Accounting/Localizations | LATAM Document Types | 2 | 15 Python, 7 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`l10n_lb_account`](addons/l10n_lb_account.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_lk`](addons/l10n_lk.md) | Accounting/Localizations/Account Charts | Provides accounting localizations for Sri Lanka. | 2 | 10 Python, 6 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_lt`](addons/l10n_lt.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 6 Python, 4 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_lu`](addons/l10n_lu.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 6 Python, 6 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_lv`](addons/l10n_lv.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ma`](addons/l10n_ma.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 8 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mc`](addons/l10n_mc.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mk`](addons/l10n_mk.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ml`](addons/l10n_ml.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mm`](addons/l10n_mm.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 7 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_mn`](addons/l10n_mn.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mq`](addons/l10n_mq.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mr`](addons/l10n_mr.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mt`](addons/l10n_mt.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mt_pos`](addons/l10n_mt_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`l10n_mu_account`](addons/l10n_mu_account.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 6 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_mx`](addons/l10n_mx.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 16 Python, 6 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_my`](addons/l10n_my.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 9 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_my_edi`](addons/l10n_my_edi.md) | Accounting/Localizations/EDI | E-invoicing using MyInvois | 3 | 27 Python, 27 XML, 0 JS/TS, 6 tests, 1 security, 0 routes |
| [`l10n_my_edi_pos`](addons/l10n_my_edi_pos.md) | Accounting/Localizations/EDI | Consolidated E-invoicing using MyInvois | 2 | 13 Python, 10 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_my_ubl_pint`](addons/l10n_my_ubl_pint.md) | Accounting/Localizations/EDI | Not declared | 1 | 9 Python, 5 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_mz`](addons/l10n_mz.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ne`](addons/l10n_ne.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ng`](addons/l10n_ng.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_nl`](addons/l10n_nl.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 12 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_no`](addons/l10n_no.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 10 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_nz`](addons/l10n_nz.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 7 Python, 4 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_om`](addons/l10n_om.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_pa`](addons/l10n_pa.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 12 Python, 7 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`l10n_pe`](addons/l10n_pe.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 20 Python, 7 XML, 1 JS/TS, 2 tests, 1 security, 1 routes |
| [`l10n_pe_pos`](addons/l10n_pe_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 12 Python, 3 XML, 5 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_ph`](addons/l10n_ph.md) | Accounting/Localizations/Account Charts | This is the module to manage the accounting chart for The Philippines. | 2 | 16 Python, 12 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_ph_invoice`](addons/l10n_ph_invoice.md) | Accounting/Localizations | Apply Philippine SC/PWD discount privileges on customer invoices and credit notes. | 1 | 12 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_ph_sale`](addons/l10n_ph_sale.md) | Accounting/Localizations | Apply Philippine SC/PWD discount privileges on quotations and sale orders. | 2 | 10 Python, 1 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_pk`](addons/l10n_pk.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 13 Python, 6 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_pk_edi`](addons/l10n_pk_edi.md) | Accounting/Localizations/EDI | Electronic Invoicing for Pakistan FBR(v1.12) | 4 | 21 Python, 11 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_pk_edi_pos`](addons/l10n_pk_edi_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 4 | 13 Python, 10 XML, 8 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_pl`](addons/l10n_pl.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 20 Python, 8 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`l10n_pl_edi`](addons/l10n_pl_edi.md) | Accounting/Localizations | Support for FA(3) electronic invoices in Poland via KSeF | 2 | 15 Python, 19 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_pl_edi_jst`](addons/l10n_pl_edi_jst.md) | Accounting/Localizations | Support for Local Government Unit (LGU) in the FA(3) format | 2 | 7 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_pt`](addons/l10n_pt.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 8 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_qa`](addons/l10n_qa.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_re`](addons/l10n_re.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ro`](addons/l10n_ro.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 6 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ro_edi`](addons/l10n_ro_edi.md) | Accounting/Localizations/EDI | E-Invoice implementation for Romania | 2 | 22 Python, 15 XML, 1 JS/TS, 4 tests, 1 security, 2 routes |
| [`l10n_ro_edi_stock`](addons/l10n_ro_edi_stock.md) | Accounting/Localizations/EDI | Not declared | 2 | 13 Python, 13 XML, 1 JS/TS, 5 tests, 0 security, 0 routes |
| [`l10n_rs`](addons/l10n_rs.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_rs_edi`](addons/l10n_rs_edi.md) | Accounting/Localizations/EDI | E-Invoice implementation for Serbia | 2 | 13 Python, 5 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_rw`](addons/l10n_rw.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_sa`](addons/l10n_sa.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 22 Python, 11 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_sa_edi`](addons/l10n_sa_edi.md) | Accounting/Localizations/EDI | E-Invoicing, Universal Business Language | 3 | 32 Python, 23 XML, 1 JS/TS, 6 tests, 1 security, 0 routes |
| [`l10n_sa_edi_pos`](addons/l10n_sa_edi_pos.md) | Accounting/Localizations/EDI | ZATCA E-Invoicing, support for PoS | 2 | 13 Python, 2 XML, 7 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_sa_pos`](addons/l10n_sa_pos.md) | Accounting/Localizations/Point of Sale | Not declared | 2 | 10 Python, 2 XML, 7 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_se`](addons/l10n_se.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 11 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_sg`](addons/l10n_sg.md) | Accounting/Localizations/Account Charts | Not declared | 4 | 19 Python, 8 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`l10n_sg_ubl_pint`](addons/l10n_sg_ubl_pint.md) | Accounting/Localizations/EDI | Not declared | 1 | 9 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_si`](addons/l10n_si.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 8 Python, 6 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_sk`](addons/l10n_sk.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 11 Python, 5 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_sn`](addons/l10n_sn.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_syscohada`](addons/l10n_syscohada.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_td`](addons/l10n_td.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_test_pos_qr_payment`](addons/l10n_test_pos_qr_payment.md) | Sales/Point of Sale | Not declared | 6 | 5 Python, 0 XML, 4 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_tg`](addons/l10n_tg.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_th`](addons/l10n_th.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 25 Python, 14 XML, 0 JS/TS, 7 tests, 1 security, 1 routes |
| [`l10n_tn`](addons/l10n_tn.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_tr`](addons/l10n_tr.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 16 Python, 6 XML, 1 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_tw`](addons/l10n_tw.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 6 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_tw_edi_ecpay`](addons/l10n_tw_edi_ecpay.md) | Accounting/Localizations/EDI | E-invoicing using ECpay | 1 | 19 Python, 6 XML, 0 JS/TS, 2 tests, 1 security, 1 routes |
| [`l10n_tw_edi_ecpay_pos`](addons/l10n_tw_edi_ecpay_pos.md) | Point of sale/Localizations/EDI | ECpay E-invoice bridge module for POS | 2 | 13 Python, 6 XML, 10 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_tw_edi_ecpay_sale`](addons/l10n_tw_edi_ecpay_sale.md) | Website Sale/Localizations/EDI | ECPay E-invoice bridge module for Sales | 2 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`l10n_tw_edi_ecpay_website_sale`](addons/l10n_tw_edi_ecpay_website_sale.md) | Website Sale/Localizations/EDI | ECpay E-invoice bridge module for Ecommerce | 2 | 10 Python, 2 XML, 4 JS/TS, 2 tests, 0 security, 4 routes |
| [`l10n_tz_account`](addons/l10n_tz_account.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ua`](addons/l10n_ua.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ug`](addons/l10n_ug.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_uk`](addons/l10n_uk.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 6 Python, 5 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_us`](addons/l10n_us.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 6 Python, 4 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`l10n_us_account`](addons/l10n_us_account.md) | Accounting/Localizations/Account Charts | Not declared | 3 | 9 Python, 7 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_uy`](addons/l10n_uy.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 16 Python, 9 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_uz`](addons/l10n_uz.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_ve`](addons/l10n_ve.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_vn`](addons/l10n_vn.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 12 Python, 5 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`l10n_vn_edi_viettel`](addons/l10n_vn_edi_viettel.md) | Accounting/Localizations/EDI | E-invoicing using SInvoice by Viettel | 1 | 16 Python, 5 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_vn_edi_viettel_pos`](addons/l10n_vn_edi_viettel_pos.md) | Accounting/Localizations/EDI | POS E-invoicing using SInvoice by Viettel | 2 | 13 Python, 4 XML, 7 JS/TS, 3 tests, 1 security, 0 routes |
| [`l10n_vn_edi_viettel_stock`](addons/l10n_vn_edi_viettel_stock.md) | Accounting/Localizations/EDI | Delivery E-invoicing using SInvoice by Viettel | 2 | 13 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`l10n_yt`](addons/l10n_yt.md) | Accounting/Localizations/Account Charts | Not declared | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_za`](addons/l10n_za.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`l10n_zm_account`](addons/l10n_zm_account.md) | Accounting/Localizations/Account Charts | Not declared | 1 | 5 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |

## Authentication & Integrations (28 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`auth_ldap`](addons/auth_ldap.md) | Hidden/Tools | Not declared | 2 | 9 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`auth_oauth`](addons/auth_oauth.md) | Hidden/Tools | Not declared | 4 | 9 Python, 4 XML, 0 JS/TS, 0 tests, 1 security, 3 routes |
| [`auth_passkey`](addons/auth_passkey.md) | Hidden/Tools | Log in with a Passkey | 2 | 61 Python, 5 XML, 9 JS/TS, 2 tests, 1 security, 2 routes |
| [`auth_passkey_portal`](addons/auth_passkey_portal.md) | Hidden/Tools | Passkeys for portal users | 2 | 4 Python, 2 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`auth_password_policy`](addons/auth_password_policy.md) | Hidden/Tools | Implement basic password policy configuration & check | 2 | 5 Python, 4 XML, 3 JS/TS, 0 tests, 0 security, 0 routes |
| [`auth_password_policy_portal`](addons/auth_password_policy_portal.md) | Tools | Not declared | 2 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`auth_password_policy_signup`](addons/auth_password_policy_signup.md) | Hidden/Tools | Not declared | 2 | 5 Python, 2 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`auth_signup`](addons/auth_signup.md) | Hidden/Tools | Not declared | 3 | 13 Python, 9 XML, 2 JS/TS, 4 tests, 0 security, 5 routes |
| [`auth_timeout`](addons/auth_timeout.md) | Hidden/Tools | Ask for authentication after user inactivity | 4 | 10 Python, 1 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`auth_totp`](addons/auth_totp.md) | Extra Tools | Not declared | 1 | 15 Python, 5 XML, 3 JS/TS, 3 tests, 1 security, 1 routes |
| [`auth_totp_mail`](addons/auth_totp_mail.md) | Extra Tools | Not declared | 2 | 14 Python, 7 XML, 2 JS/TS, 4 tests, 0 security, 2 routes |
| [`auth_totp_portal`](addons/auth_totp_portal.md) | Hidden | Not declared | 2 | 6 Python, 1 XML, 6 JS/TS, 2 tests, 1 security, 0 routes |
| [`certificate`](addons/certificate.md) | Hidden/Tools | Manage certificate | 1 | 9 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`cloud_storage`](addons/cloud_storage.md) | Technical Settings | Store chatter attachments in the cloud | 2 | 14 Python, 3 XML, 7 JS/TS, 5 tests, 0 security, 1 routes |
| [`cloud_storage_azure`](addons/cloud_storage_azure.md) | Technical Settings | Store chatter attachments in the Azure cloud | 1 | 11 Python, 1 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`cloud_storage_google`](addons/cloud_storage_google.md) | Technical Settings | Store chatter attachments in the Google cloud | 1 | 12 Python, 1 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`cloud_storage_migration`](addons/cloud_storage_migration.md) | Technical Settings | Migrate local attachments to cloud storage | 1 | 8 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`google_account`](addons/google_account.md) | Hidden/Tools | Not declared | 1 | 6 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 1 routes |
| [`google_address_autocomplete`](addons/google_address_autocomplete.md) | Hidden/Tools | Assist with automatic completion & suggestions when filling address | 1 | 10 Python, 4 XML, 4 JS/TS, 3 tests, 0 security, 2 routes |
| [`google_gmail`](addons/google_gmail.md) | Hidden | Not declared | 1 | 13 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 2 routes |
| [`google_recaptcha`](addons/google_recaptcha.md) | Hidden | Not declared | 1 | 5 Python, 2 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`iot_drivers`](addons/iot_drivers.md) | Hidden | Connect the Web Client to Hardware Peripherals | 0 | 51 Python, 0 XML, 19 JS/TS, 0 tests, 0 security, 0 routes |
| [`iot_webserial`](addons/iot_webserial.md) | Administration/IoT | Interface with serial devices directly via the browser using Web Serial. | 1 | 2 Python, 1 XML, 6 JS/TS, 0 tests, 0 security, 0 routes |
| [`microsoft_account`](addons/microsoft_account.md) | Hidden/Tools | Not declared | 1 | 7 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 1 routes |
| [`microsoft_outlook`](addons/microsoft_outlook.md) | Hidden | Not declared | 1 | 12 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 2 routes |
| [`payment`](addons/payment.md) | Hidden | The payment engine used by payment provider modules. | 2 | 38 Python, 16 XML, 7 JS/TS, 14 tests, 1 security, 7 routes |
| [`phone_validation`](addons/phone_validation.md) | Hidden | Validate and format phone numbers | 2 | 32 Python, 4 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`sms_twilio`](addons/sms_twilio.md) | Hidden/Tools | Send SMS messages using Twilio | 1 | 22 Python, 3 XML, 1 JS/TS, 5 tests, 1 security, 1 routes |

## Human Resources & Workforce (31 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`fleet`](addons/fleet.md) | Human Resources/Fleet | Manage your fleet and track car costs | 2 | 30 Python, 15 XML, 2 JS/TS, 8 tests, 2 security, 0 routes |
| [`fleet_maintenance`](addons/fleet_maintenance.md) | Human Resources | Integrates Fleet and Maintenance | 2 | 5 Python, 3 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`gamification`](addons/gamification.md) | Human Resources | Not declared | 1 | 19 Python, 19 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`hr`](addons/hr.md) | Human Resources/Employees | Centralize employee information | 6 | 70 Python, 55 XML, 79 JS/TS, 28 tests, 2 security, 3 routes |
| [`hr_address_extended`](addons/hr_address_extended.md) | Human Resources/Employees | Centralize employee information | 2 | 7 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`hr_attendance`](addons/hr_attendance.md) | Human Resources/Attendances | Track employee attendance | 4 | 29 Python, 29 XML, 27 JS/TS, 13 tests, 2 security, 15 routes |
| [`hr_calendar`](addons/hr_calendar.md) | Human Resources/Employees | Not declared | 2 | 14 Python, 6 XML, 6 JS/TS, 6 tests, 1 security, 0 routes |
| [`hr_calendar_google`](addons/hr_calendar_google.md) | Human Resources/Remote Work | Not declared | 2 | 7 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`hr_expense`](addons/hr_expense.md) | Human Resources/Expenses | Submit, validate and reinvoice employee expenses | 3 | 38 Python, 27 XML, 14 JS/TS, 9 tests, 2 security, 0 routes |
| [`hr_fleet`](addons/hr_fleet.md) | Human Resources | Get history of driven cars by employees | 2 | 13 Python, 5 XML, 2 JS/TS, 2 tests, 1 security, 0 routes |
| [`hr_gamification`](addons/hr_gamification.md) | Human Resources | Not declared | 2 | 11 Python, 4 XML, 6 JS/TS, 2 tests, 2 security, 0 routes |
| [`hr_holidays`](addons/hr_holidays.md) | Human Resources/Time Off | Allocate time off and follow leave requests | 3 | 88 Python, 53 XML, 74 JS/TS, 44 tests, 2 security, 5 routes |
| [`hr_holidays_attendance`](addons/hr_holidays_attendance.md) | Human Resources | Attendance Holidays | 2 | 26 Python, 7 XML, 0 JS/TS, 9 tests, 1 security, 0 routes |
| [`hr_livechat`](addons/hr_livechat.md) | Human Resources | Not declared | 2 | 2 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`hr_maintenance`](addons/hr_maintenance.md) | Human Resources | Equipment, Assets, Internal Hardware, Allocation Tracking | 2 | 9 Python, 3 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`hr_presence`](addons/hr_presence.md) | Human Resources | Not declared | 3 | 9 Python, 6 XML, 3 JS/TS, 0 tests, 1 security, 0 routes |
| [`hr_recruitment`](addons/hr_recruitment.md) | Human Resources/Recruitment | Track your recruitment pipeline | 6 | 40 Python, 34 XML, 18 JS/TS, 8 tests, 2 security, 0 routes |
| [`hr_recruitment_skills`](addons/hr_recruitment_skills.md) | Human Resources/Recruitment | Manage skills of your employees | 2 | 9 Python, 6 XML, 2 JS/TS, 3 tests, 1 security, 0 routes |
| [`hr_recruitment_sms`](addons/hr_recruitment_sms.md) | Human Resources/Recruitment | Mass mailing sms to job applicants | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`hr_recruitment_survey`](addons/hr_recruitment_survey.md) | Human Resources | Surveys | 2 | 16 Python, 9 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`hr_skills`](addons/hr_skills.md) | Human Resources/Employees | Manage skills, knowledge and resume of your employees | 1 | 29 Python, 27 XML, 21 JS/TS, 6 tests, 1 security, 1 routes |
| [`hr_skills_event`](addons/hr_skills_event.md) | Hidden | Link training events to resume of your employees | 2 | 7 Python, 3 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`hr_skills_slides`](addons/hr_skills_slides.md) | Human Resources/Employees | Add completed courses to resume of your employees | 2 | 9 Python, 7 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`hr_skills_survey`](addons/hr_skills_survey.md) | Human Resources/Employees | Add certification to resume of your employees | 2 | 8 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`hr_timesheet`](addons/hr_timesheet.md) | Services/Timesheets | Track employee time on tasks | 4 | 38 Python, 22 XML, 21 JS/TS, 12 tests, 2 security, 1 routes |
| [`hr_timesheet_attendance`](addons/hr_timesheet_attendance.md) | Human Resources/Attendances | Not declared | 2 | 9 Python, 1 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`hr_work_entry`](addons/hr_work_entry.md) | Human Resources/Employees | Manage work entries | 1 | 23 Python, 15 XML, 5 JS/TS, 5 tests, 1 security, 1 routes |
| [`lunch`](addons/lunch.md) | Human Resources/Lunch | Handle lunch orders of your employees | 1 | 25 Python, 18 XML, 10 JS/TS, 6 tests, 2 security, 6 routes |
| [`project_timesheet_holidays`](addons/project_timesheet_holidays.md) | Human Resources | Schedule timesheet when on time off | 2 | 16 Python, 3 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`resource`](addons/resource.md) | Hidden | Not declared | 2 | 19 Python, 15 XML, 27 JS/TS, 8 tests, 1 security, 0 routes |
| [`resource_mail`](addons/resource_mail.md) | Hidden | Not declared | 2 | 6 Python, 3 XML, 10 JS/TS, 0 tests, 0 security, 0 routes |

## Marketing & Engagement (29 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`digest`](addons/digest.md) | Marketing | Not declared | 3 | 14 Python, 8 XML, 0 JS/TS, 3 tests, 1 security, 3 routes |
| [`event`](addons/event.md) | Marketing/Events | Trainings, Conferences, Meetings, Exhibitions, Registrations | 7 | 32 Python, 40 XML, 16 JS/TS, 6 tests, 2 security, 4 routes |
| [`event_booth`](addons/event_booth.md) | Marketing/Events | Manage event booths | 1 | 12 Python, 11 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`event_booth_sale`](addons/event_booth_sale.md) | Marketing/Events | Manage event booths sale | 2 | 18 Python, 8 XML, 2 JS/TS, 4 tests, 1 security, 0 routes |
| [`event_crm`](addons/event_crm.md) | Marketing/Events | Not declared | 2 | 14 Python, 9 XML, 1 JS/TS, 5 tests, 1 security, 0 routes |
| [`event_crm_sale`](addons/event_crm_sale.md) | Marketing/Events | Not declared | 2 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`event_product`](addons/event_product.md) | Marketing/Events | Not declared | 3 | 12 Python, 5 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`event_sale`](addons/event_sale.md) | Marketing/Events | Not declared | 2 | 22 Python, 13 XML, 3 JS/TS, 6 tests, 2 security, 0 routes |
| [`event_sms`](addons/event_sms.md) | Marketing/Events | Not declared | 2 | 9 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`link_tracker`](addons/link_tracker.md) | Marketing | Not declared | 2 | 15 Python, 2 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`marketing_card`](addons/marketing_card.md) | Marketing/Marketing Card | Generate dynamic shareable cards | 4 | 19 Python, 12 XML, 1 JS/TS, 3 tests, 2 security, 6 routes |
| [`marketing_card_event`](addons/marketing_card_event.md) | Marketing/Marketing Card | Generate dynamic shareable cards for entities linked to events. | 2 | 8 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mass_mailing`](addons/mass_mailing.md) | Marketing/Email Marketing | Design, send and track emails | 8 | 55 Python, 103 XML, 97 JS/TS, 16 tests, 2 security, 17 routes |
| [`mass_mailing_crm`](addons/mass_mailing_crm.md) | Marketing/Email Marketing | Add lead / opportunities UTM info on mass mailing | 2 | 6 Python, 1 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_crm_sms`](addons/mass_mailing_crm_sms.md) | Marketing/Email Marketing | Add lead / opportunities info on mass mailing sms | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_event`](addons/mass_mailing_event.md) | Marketing/Email Marketing | Not declared | 2 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_event_sms`](addons/mass_mailing_event_sms.md) | Marketing/Email Marketing | Not declared | 5 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mass_mailing_event_track`](addons/mass_mailing_event_track.md) | Marketing/Email Marketing | Not declared | 2 | 5 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_event_track_sms`](addons/mass_mailing_event_track_sms.md) | Marketing/Email Marketing | Not declared | 4 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_sale`](addons/mass_mailing_sale.md) | Marketing/Email Marketing | Add sale order UTM info on mass mailing | 2 | 6 Python, 5 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_sale_sms`](addons/mass_mailing_sale_sms.md) | Marketing/Email Marketing | Add sale order info on mass mailing sms | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_slides`](addons/mass_mailing_slides.md) | Marketing/Email Marketing | Not declared | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mass_mailing_sms`](addons/mass_mailing_sms.md) | Marketing/Email Marketing | Design, send and track SMS | 3 | 29 Python, 16 XML, 2 JS/TS, 9 tests, 1 security, 3 routes |
| [`mass_mailing_themes`](addons/mass_mailing_themes.md) | Marketing/Email Marketing | Design gorgeous mails | 1 | 2 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`social_media`](addons/social_media.md) | Marketing/Social Marketing | Social media connectors for company settings. | 1 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`survey`](addons/survey.md) | Marketing/Surveys | Send your surveys or share them live. | 6 | 37 Python, 39 XML, 46 JS/TS, 18 tests, 2 security, 23 routes |
| [`survey_crm`](addons/survey_crm.md) | Marketing/Surveys | Generate leads from surveys | 2 | 11 Python, 5 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_mass_mailing`](addons/test_mass_mailing.md) | Marketing/Email Marketing | Mass Mail Tests: feature and performance tests for mass mailing | 6 | 26 Python, 0 XML, 0 JS/TS, 18 tests, 1 security, 0 routes |
| [`utm`](addons/utm.md) | Marketing | Not declared | 2 | 16 Python, 12 XML, 1 JS/TS, 6 tests, 1 security, 0 routes |

## Other / Requires Verification (1 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`printer`](addons/printer.md) | Not declared | Base module to manage external printers (e.g. ePOS, ZPL) | 1 | 10 Python, 5 XML, 10 JS/TS, 3 tests, 1 security, 0 routes |

## Platform & Administration (24 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`api_doc`](addons/api_doc.md) | Hidden | Not declared | 1 | 10 Python, 10 XML, 21 JS/TS, 4 tests, 1 security, 5 routes |
| [`attachment_indexation`](addons/attachment_indexation.md) | Hidden/Tools | Not declared | 1 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`base_import`](addons/base_import.md) | Hidden/Tools | Not declared | 1 | 7 Python, 8 XML, 12 JS/TS, 0 tests, 1 security, 1 routes |
| [`base_import_module`](addons/base_import_module.md) | Hidden/Tools | Not declared | 1 | 12 Python, 2 XML, 3 JS/TS, 3 tests, 1 security, 1 routes |
| [`base_install_request`](addons/base_install_request.md) | Hidden | Not declared | 1 | 6 Python, 4 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`base_report_paper_muncher`](addons/base_report_paper_muncher.md) | Hidden/Tools | Paper Muncher Engine | 1 | 7 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`base_report_wkhtmltox`](addons/base_report_wkhtmltox.md) | Hidden/Tools | wkhtmltopdf rendering engine | 0 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`base_setup`](addons/base_setup.md) | Hidden | Not declared | 2 | 15 Python, 4 XML, 1 JS/TS, 5 tests, 0 security, 3 routes |
| [`base_sparse_field`](addons/base_sparse_field.md) | Hidden | Implementation of sparse fields. | 1 | 7 Python, 1 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`bus`](addons/bus.md) | Hidden | Not declared | 2 | 41 Python, 1 XML, 34 JS/TS, 15 tests, 0 security, 6 routes |
| [`iap`](addons/iap.md) | Hidden/Tools | Basic models and helpers to support In-App Purchase. | 2 | 13 Python, 5 XML, 1 JS/TS, 3 tests, 1 security, 0 routes |
| [`iap_crm`](addons/iap_crm.md) | Hidden/Tools | Bridge between IAP and CRM | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`iap_mail`](addons/iap_mail.md) | Hidden/Tools | Bridge between IAP and mail | 2 | 4 Python, 2 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`onboarding`](addons/onboarding.md) | Hidden | Not declared | 1 | 12 Python, 3 XML, 1 JS/TS, 5 tests, 1 security, 0 routes |
| [`partner_autocomplete`](addons/partner_autocomplete.md) | Hidden/Tools | Auto-complete partner companies' data | 1 | 12 Python, 5 XML, 8 JS/TS, 4 tests, 0 security, 0 routes |
| [`portal`](addons/portal.md) | Hidden | Customer Portal | 6 | 32 Python, 14 XML, 33 JS/TS, 8 tests, 1 security, 16 routes |
| [`privacy_lookup`](addons/privacy_lookup.md) | Hidden | Not declared | 1 | 9 Python, 3 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`rpc`](addons/rpc.md) | Extra Tools | Not declared | 1 | 8 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 6 routes |
| [`snailmail`](addons/snailmail.md) | Hidden/Tools | Not declared | 2 | 19 Python, 5 XML, 10 JS/TS, 5 tests, 1 security, 0 routes |
| [`web`](addons/web.md) | Hidden | Not declared | 1 | 70 Python, 287 XML, 1083 JS/TS, 31 tests, 1 security, 73 routes |
| [`web_hierarchy`](addons/web_hierarchy.md) | Hidden | Not declared | 1 | 6 Python, 3 XML, 10 JS/TS, 0 tests, 0 security, 0 routes |
| [`web_tour`](addons/web_tour.md) | Hidden | Not declared | 1 | 9 Python, 6 XML, 28 JS/TS, 3 tests, 1 security, 0 routes |
| [`web_unsplash`](addons/web_unsplash.md) | Hidden | Find free high-resolution images from Unsplash | 2 | 12 Python, 4 XML, 7 JS/TS, 2 tests, 0 security, 4 routes |
| [`base`](addons/base.md) | Hidden | Not declared | 0 | 107 Python, 88 XML, 1 JS/TS, 42 tests, 2 security, 0 routes |

## Point of Sale (46 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`point_of_sale`](addons/point_of_sale.md) | Sales/Point of Sale | Handle checkouts and payments for shops and restaurants. | 10 | 103 Python, 147 XML, 391 JS/TS, 29 tests, 2 security, 11 routes |
| [`pos_adyen`](addons/pos_adyen.md) | Sales/Point of Sale | Integrate your POS with an Adyen payment terminal | 2 | 13 Python, 2 XML, 5 JS/TS, 2 tests, 0 security, 2 routes |
| [`pos_bancontact_pay`](addons/pos_bancontact_pay.md) | Sales/Point of Sale | Accept Bancontact Pay and Wero QR code payments in POS (Payconiq). | 1 | 20 Python, 3 XML, 12 JS/TS, 5 tests, 0 security, 2 routes |
| [`pos_cashdro`](addons/pos_cashdro.md) | Sales/Point of Sale | Integrate your POS with a Cashdro automatic cash payment device | 1 | 4 Python, 2 XML, 5 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_cashmatic`](addons/pos_cashmatic.md) | Sales/Point of Sale | Integrate your POS with a cash matic automatic cash payment device | 1 | 4 Python, 2 XML, 4 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_discount`](addons/pos_discount.md) | Sales/Point of Sale | Simple Discounts in the Point of Sale  | 1 | 10 Python, 6 XML, 17 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_dpopay`](addons/pos_dpopay.md) | Sales/Point of Sale | Integrate your POS with DPO payment terminal. | 1 | 7 Python, 2 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_edi_ubl`](addons/pos_edi_ubl.md) | Sales/Point of Sale | UBL in the Point of Sale  | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_event`](addons/pos_event.md) | Technical | Link module between Point of Sale and Event | 2 | 16 Python, 12 XML, 34 JS/TS, 2 tests, 1 security, 0 routes |
| [`pos_event_sale`](addons/pos_event_sale.md) | Technical | Link module between pos_sale and pos_event | 3 | 10 Python, 0 XML, 2 JS/TS, 3 tests, 0 security, 0 routes |
| [`pos_glory_cash`](addons/pos_glory_cash.md) | Sales/Point of Sale | Integrate your POS with a Glory automatic cash payment device | 1 | 4 Python, 5 XML, 13 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_hr`](addons/pos_hr.md) | Sales/Point of Sale | Link module between Point of Sale and HR | 2 | 23 Python, 14 XML, 31 JS/TS, 5 tests, 0 security, 0 routes |
| [`pos_hr_restaurant`](addons/pos_hr_restaurant.md) | Sales/Point of Sale | Link module between pos_hr and pos_restaurant | 2 | 4 Python, 0 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_imin`](addons/pos_imin.md) | Sales/Point of Sale | iMin ePOS Printers in PoS | 1 | 4 Python, 1 XML, 4 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_loyalty`](addons/pos_loyalty.md) | Sales/Point Of Sale | Use Coupons, Gift Cards and Loyalty programs in Point of Sale | 2 | 29 Python, 16 XML, 54 JS/TS, 11 tests, 1 security, 0 routes |
| [`pos_mercado_pago`](addons/pos_mercado_pago.md) | Sales/Point of Sale | Integrate your POS with the Mercado Pago Smart Point terminal | 1 | 10 Python, 1 XML, 1 JS/TS, 3 tests, 0 security, 1 routes |
| [`pos_mollie`](addons/pos_mollie.md) | Sales/Point of Sale | Integrate your POS with a Mollie payment terminal | 2 | 8 Python, 1 XML, 4 JS/TS, 2 tests, 0 security, 1 routes |
| [`pos_mrp`](addons/pos_mrp.md) | Sales/Point of Sale | Link module between Point of Sale and Mrp | 2 | 10 Python, 0 XML, 1 JS/TS, 4 tests, 1 security, 0 routes |
| [`pos_online_payment`](addons/pos_online_payment.md) | Not declared | Not declared | 2 | 15 Python, 7 XML, 11 JS/TS, 3 tests, 1 security, 3 routes |
| [`pos_online_payment_self_order`](addons/pos_online_payment_self_order.md) | Sales/Point of Sale | Support online payment in self-order | 2 | 17 Python, 2 XML, 10 JS/TS, 5 tests, 0 security, 2 routes |
| [`pos_partner_autocomplete`](addons/pos_partner_autocomplete.md) | Sales/Point of Sale | Link module between Partner Autocomplete and Point of Sale | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_pine_labs`](addons/pos_pine_labs.md) | Sales/Point of Sale | Integrate your POS with Pine Labs payment terminals | 1 | 6 Python, 2 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_qfpay`](addons/pos_qfpay.md) | Sales/Point of Sale | Integrate your POS with the QFPay terminal in Hong Kong | 1 | 8 Python, 1 XML, 5 JS/TS, 2 tests, 0 security, 1 routes |
| [`pos_razorpay`](addons/pos_razorpay.md) | Sales/Point of Sale | Integrate your POS with a Razorpay payment terminal | 1 | 8 Python, 1 XML, 5 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_repair`](addons/pos_repair.md) | Technical | Link module between Point of Sale and Repair | 2 | 7 Python, 0 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_restaurant`](addons/pos_restaurant.md) | Sales/Point of Sale | Restaurant extensions for the Point of Sale  | 1 | 21 Python, 42 XML, 108 JS/TS, 5 tests, 1 security, 0 routes |
| [`pos_restaurant_loyalty`](addons/pos_restaurant_loyalty.md) | Sales/Point of Sale | Link module between pos_restaurant and pos_loyalty | 2 | 4 Python, 0 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_safaricom`](addons/pos_safaricom.md) | Sales/Point of Sale | Integrate your POS with the Safaricom Payment Provider | 1 | 12 Python, 3 XML, 8 JS/TS, 2 tests, 1 security, 3 routes |
| [`pos_sale`](addons/pos_sale.md) | Sales/Point of Sale | Link module between Point of Sale and Sales | 2 | 22 Python, 9 XML, 30 JS/TS, 4 tests, 1 security, 0 routes |
| [`pos_sale_delivery`](addons/pos_sale_delivery.md) | Hidden | Not declared | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_sale_loyalty`](addons/pos_sale_loyalty.md) | Sales/Point of Sale | Link module between pos_sale and pos_loyalty | 2 | 7 Python, 0 XML, 5 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_sale_margin`](addons/pos_sale_margin.md) | Sales/Point of Sale | Link module between Point of Sale and Sales Margin | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_sale_stock`](addons/pos_sale_stock.md) | Sales/Point of Sale | Link module between PoS Stock and Sales | 2 | 13 Python, 1 XML, 6 JS/TS, 4 tests, 0 security, 0 routes |
| [`pos_self_order`](addons/pos_self_order.md) | Sales/Point Of Sale | Addon for the POS App that allows customers to view the menu on their smartphone. | 5 | 51 Python, 59 XML, 146 JS/TS, 20 tests, 1 security, 18 routes |
| [`pos_self_order_bancontact_pay`](addons/pos_self_order_bancontact_pay.md) | Sales/Point of Sale | Accept Bancontact Pay and Wero QR code payments in a kiosk (Payconiq). | 2 | 11 Python, 1 XML, 6 JS/TS, 3 tests, 0 security, 1 routes |
| [`pos_self_order_event`](addons/pos_self_order_event.md) | Sales/Point Of Sale | Link module between PoS Self Order and PoS Event | 2 | 10 Python, 5 XML, 14 JS/TS, 2 tests, 0 security, 2 routes |
| [`pos_self_order_pine_labs`](addons/pos_self_order_pine_labs.md) | Sales/Point Of Sale | An addon for the Self Order App (KIOSK) that allows customers to pay using the Pine Labs POS Terminal. | 2 | 8 Python, 0 XML, 3 JS/TS, 2 tests, 0 security, 2 routes |
| [`pos_self_order_qfpay`](addons/pos_self_order_qfpay.md) | Sales/Point Of Sale | Addon for the Self Order App that allows customers to pay by QFPay. | 2 | 6 Python, 0 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_self_order_razorpay`](addons/pos_self_order_razorpay.md) | Sales/Point Of Sale | Addon for the Self Order App that allows customers to pay by Razorpay POS Terminal. | 2 | 8 Python, 0 XML, 3 JS/TS, 2 tests, 0 security, 2 routes |
| [`pos_self_order_sale`](addons/pos_self_order_sale.md) | Sales/Point Of Sale | Not declared | 2 | 4 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`pos_self_order_sms`](addons/pos_self_order_sms.md) | Sales/Point Of Sale | Not declared | 2 | 7 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_sms`](addons/pos_sms.md) | Send sms to customer for order confirmation | Not declared | 2 | 8 Python, 3 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_stock`](addons/pos_stock.md) | Sales/Point of Sale | Stock integration for PoS | 2 | 38 Python, 17 XML, 48 JS/TS, 16 tests, 2 security, 0 routes |
| [`pos_stripe`](addons/pos_stripe.md) | Sales/Point of Sale | Integrate your POS with a Stripe payment terminal | 2 | 6 Python, 1 XML, 7 JS/TS, 2 tests, 0 security, 0 routes |
| [`pos_sumup`](addons/pos_sumup.md) | Sales/Point of Sale | Integrate your POS with a SumUp payment terminal | 1 | 8 Python, 1 XML, 7 JS/TS, 2 tests, 0 security, 1 routes |
| [`pos_viva_com`](addons/pos_viva_com.md) | Sales/Point of Sale | Integrate your PoS with a Viva.com payment terminal | 1 | 10 Python, 1 XML, 11 JS/TS, 3 tests, 0 security, 3 routes |

## Productivity & Collaboration (29 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`board`](addons/board.md) | Productivity | Build your own dashboards | 1 | 6 Python, 4 XML, 6 JS/TS, 0 tests, 1 security, 1 routes |
| [`calendar`](addons/calendar.md) | Productivity/Calendar | Schedule employees' meetings | 2 | 47 Python, 39 XML, 59 JS/TS, 20 tests, 1 security, 10 routes |
| [`calendar_sms`](addons/calendar_sms.md) | Productivity/Calendar | Send text messages as event reminders | 2 | 8 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`data_recycle`](addons/data_recycle.md) | Productivity/Data Cleaning | Find old records and archive/delete them | 1 | 7 Python, 6 XML, 3 JS/TS, 2 tests, 1 security, 0 routes |
| [`google_calendar`](addons/google_calendar.md) | Productivity | Not declared | 2 | 35 Python, 6 XML, 4 JS/TS, 11 tests, 1 security, 1 routes |
| [`mail`](addons/mail.md) | Productivity/Discuss | Chat, mail gateway and private channels | 5 | 201 Python, 271 XML, 688 JS/TS, 66 tests, 1 security, 20 routes |
| [`mail_bot`](addons/mail_bot.md) | Productivity/Discuss | Add OdooBot in discussions | 1 | 8 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 1 routes |
| [`mail_bot_hr`](addons/mail_bot_hr.md) | Productivity/Discuss | Bridge module between hr and mailbot. | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mail_group`](addons/mail_group.md) | Not declared | Manage your mailing lists | 2 | 18 Python, 14 XML, 2 JS/TS, 7 tests, 1 security, 9 routes |
| [`mail_tracking`](addons/mail_tracking.md) | Productivity/Discuss | Technical tracking of discussion and message-related data | 1 | 11 Python, 3 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`mail_tracking_mass_mailing`](addons/mail_tracking_mass_mailing.md) | Productivity/Discuss | Track source of messages by mass mailing | 2 | 7 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`mail_tracking_sms`](addons/mail_tracking_sms.md) | Productivity/Discuss | Track source of messages by sms | 2 | 7 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`microsoft_calendar`](addons/microsoft_calendar.md) | Productivity | Not declared | 2 | 29 Python, 6 XML, 3 JS/TS, 10 tests, 1 security, 1 routes |
| [`rating`](addons/rating.md) | Productivity | Not declared | 1 | 14 Python, 4 XML, 9 JS/TS, 3 tests, 1 security, 2 routes |
| [`spreadsheet`](addons/spreadsheet.md) | Productivity/Dashboard | Spreadsheet | 3 | 24 Python, 13 XML, 152 JS/TS, 8 tests, 0 security, 1 routes |
| [`spreadsheet_dashboard`](addons/spreadsheet_dashboard.md) | Productivity/Dashboard | Spreadsheet | 1 | 18 Python, 15 XML, 37 JS/TS, 8 tests, 2 security, 4 routes |
| [`spreadsheet_dashboard_account`](addons/spreadsheet_dashboard_account.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_event_sale`](addons/spreadsheet_dashboard_event_sale.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_hr_expense`](addons/spreadsheet_dashboard_hr_expense.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_hr_timesheet`](addons/spreadsheet_dashboard_hr_timesheet.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_im_livechat`](addons/spreadsheet_dashboard_im_livechat.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_pos_hr`](addons/spreadsheet_dashboard_pos_hr.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_pos_restaurant`](addons/spreadsheet_dashboard_pos_restaurant.md) | Productivity/Dashboard | Spreadsheet | 3 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_sale`](addons/spreadsheet_dashboard_sale.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_sale_timesheet`](addons/spreadsheet_dashboard_sale_timesheet.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_stock_account`](addons/spreadsheet_dashboard_stock_account.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_website_sale`](addons/spreadsheet_dashboard_website_sale.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`spreadsheet_dashboard_website_sale_slides`](addons/spreadsheet_dashboard_website_sale_slides.md) | Productivity/Dashboard | Spreadsheet | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`test_discuss_full`](addons/test_discuss_full.md) | Productivity/Discuss | Test of Discuss with all possible overrides installed. | 14 | 10 Python, 0 XML, 5 JS/TS, 8 tests, 0 security, 0 routes |

## Sales & CRM (53 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`base_address_extended`](addons/base_address_extended.md) | Sales/Sales | Add extra fields on addresses | 1 | 8 Python, 3 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`base_automation`](addons/base_automation.md) | Sales/Sales | Not declared | 5 | 10 Python, 7 XML, 8 JS/TS, 3 tests, 1 security, 1 routes |
| [`base_geolocalize`](addons/base_geolocalize.md) | Sales/Sales | Not declared | 1 | 8 Python, 5 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`contacts`](addons/contacts.md) | Sales/CRM | Centralize your address book | 3 | 7 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`crm`](addons/crm.md) | Sales/CRM | Track leads and close opportunities | 11 | 50 Python, 49 XML, 48 JS/TS, 20 tests, 2 security, 3 routes |
| [`crm_iap_enrich`](addons/crm_iap_enrich.md) | Sales/CRM | Enrich Leads/Opportunities using email address domain | 2 | 8 Python, 5 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`crm_iap_mine`](addons/crm_iap_mine.md) | Sales/CRM | Generate Leads/Opportunities based on country, industries, size, etc. | 2 | 13 Python, 7 XML, 2 JS/TS, 3 tests, 1 security, 0 routes |
| [`crm_livechat`](addons/crm_livechat.md) | Sales/CRM | Create lead from livechat conversation | 2 | 15 Python, 6 XML, 14 JS/TS, 5 tests, 1 security, 0 routes |
| [`crm_mail_plugin`](addons/crm_mail_plugin.md) | Sales/CRM | Turn emails received in your mailbox into leads and log their content as internal notes. | 2 | 6 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 1 routes |
| [`crm_sale_project`](addons/crm_sale_project.md) | Sales/CRM | Project Generation from Opportunities | 2 | 10 Python, 4 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`crm_sms`](addons/crm_sms.md) | Sales/CRM | Add SMS capabilities to CRM | 2 | 4 Python, 1 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`delivery`](addons/delivery.md) | Sales/Delivery | Not declared | 2 | 29 Python, 22 XML, 3 JS/TS, 8 tests, 1 security, 0 routes |
| [`gamification_sale_crm`](addons/gamification_sale_crm.md) | Sales/CRM | Not declared | 2 | 2 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`loyalty`](addons/loyalty.md) | Sales | Use discounts, gift cards, eWallets and loyalty programs in your sales channels | 3 | 21 Python, 17 XML, 5 JS/TS, 2 tests, 1 security, 3 routes |
| [`mail_plugin`](addons/mail_plugin.md) | Sales/CRM | Allows integration with mail plugins. | 3 | 10 Python, 4 XML, 0 JS/TS, 3 tests, 0 security, 10 routes |
| [`mysubscription`](addons/mysubscription.md) | Sales | Backend Subscription App | 2 | 6 Python, 11 XML, 11 JS/TS, 2 tests, 0 security, 0 routes |
| [`partnership`](addons/partnership.md) | Sales/CRM | Not declared | 2 | 13 Python, 7 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`product`](addons/product.md) | Sales/Sales | Not declared | 3 | 57 Python, 44 XML, 22 JS/TS, 17 tests, 2 security, 4 routes |
| [`product_margin`](addons/product_margin.md) | Sales/Sales | Not declared | 1 | 8 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`product_matrix`](addons/product_matrix.md) | Sales/Sales | Technical module: Matrix Implementation | 1 | 6 Python, 5 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale`](addons/sale.md) | Sales/Sales | Sales internal machinery | 3 | 76 Python, 64 XML, 69 JS/TS, 37 tests, 2 security, 14 routes |
| [`sale_crm`](addons/sale_crm.md) | Sales/Sales | Not declared | 2 | 13 Python, 5 XML, 0 JS/TS, 5 tests, 1 security, 0 routes |
| [`sale_edi_ubl`](addons/sale_edi_ubl.md) | Sales/Sales | Not declared | 2 | 10 Python, 1 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`sale_expense`](addons/sale_expense.md) | Sales/Sales | Quotation, Sales Orders, Delivery & Invoicing Control | 2 | 15 Python, 6 XML, 1 JS/TS, 3 tests, 1 security, 0 routes |
| [`sale_expense_margin`](addons/sale_expense_margin.md) | Sales/Sales | Not declared | 2 | 7 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_gelato`](addons/sale_gelato.md) | Sales/Sales | Place orders through Gelato's print-on-demand service | 2 | 22 Python, 8 XML, 0 JS/TS, 5 tests, 0 security, 1 routes |
| [`sale_gelato_stock`](addons/sale_gelato_stock.md) | Sales/Sales | Not declared | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`sale_loyalty`](addons/sale_loyalty.md) | Sales/Sales | Use discounts and loyalty programs in sales orders | 2 | 31 Python, 10 XML, 2 JS/TS, 14 tests, 1 security, 1 routes |
| [`sale_loyalty_delivery`](addons/sale_loyalty_delivery.md) | Sales/Sales | Adds free shipping mechanism in sales orders | 2 | 12 Python, 1 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`sale_management`](addons/sale_management.md) | Sales/Sales | From quotations to invoices | 2 | 19 Python, 14 XML, 24 JS/TS, 6 tests, 1 security, 1 routes |
| [`sale_margin`](addons/sale_margin.md) | Sales/Sales | Not declared | 1 | 10 Python, 4 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_mrp`](addons/sale_mrp.md) | Sales/Sales | Not declared | 2 | 20 Python, 3 XML, 0 JS/TS, 8 tests, 1 security, 0 routes |
| [`sale_mrp_margin`](addons/sale_mrp_margin.md) | Sales/Sales | Not declared | 2 | 4 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_pdf_quote_builder`](addons/sale_pdf_quote_builder.md) | Sales/Sales | Not declared | 1 | 16 Python, 14 XML, 6 JS/TS, 4 tests, 1 security, 1 routes |
| [`sale_product_matrix`](addons/sale_product_matrix.md) | Sales/Sales | Add variants to Sales Order through a grid entry. | 2 | 6 Python, 4 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`sale_project`](addons/sale_project.md) | Sales/Sales | Task Generation from Sales Orders | 3 | 32 Python, 16 XML, 9 JS/TS, 10 tests, 1 security, 0 routes |
| [`sale_project_margin`](addons/sale_project_margin.md) | Sales/Sales | Bridge module between Sales Margin and Project | 2 | 4 Python, 3 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`sale_project_stock`](addons/sale_project_stock.md) | Sales | Adds a full traceability of inventory operations on the profitability report. | 3 | 10 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`sale_project_stock_account`](addons/sale_project_stock_account.md) | Hidden | Technical Bridge | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_purchase`](addons/sale_purchase.md) | Sales/Sales | Sale based on service outsourcing. | 2 | 11 Python, 4 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`sale_purchase_project`](addons/sale_purchase_project.md) | Sales | Technical Bridge | 3 | 7 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_purchase_stock`](addons/sale_purchase_stock.md) | Sales/Sales | SO/PO relation in case of MTO | 3 | 12 Python, 2 XML, 0 JS/TS, 5 tests, 0 security, 0 routes |
| [`sale_service`](addons/sale_service.md) | Sales/Sales | Interaction between Sales and services apps (project and planning) | 1 | 4 Python, 1 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`sale_sms`](addons/sale_sms.md) | Sales/Sales | Ease SMS integration with sales capabilities | 2 | 2 Python, 0 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`sale_stock`](addons/sale_stock.md) | Sales/Sales | Quotation, Sales Orders, Delivery & Invoicing Control | 2 | 40 Python, 24 XML, 6 JS/TS, 17 tests, 1 security, 3 routes |
| [`sale_stock_margin`](addons/sale_stock_margin.md) | Sales/Sales | Not declared | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sale_stock_product_expiry`](addons/sale_stock_product_expiry.md) | Sales/Sales | Not declared | 2 | 8 Python, 1 XML, 2 JS/TS, 3 tests, 0 security, 0 routes |
| [`sale_timesheet`](addons/sale_timesheet.md) | Sales/Sales | Sell based on timesheets | 2 | 47 Python, 18 XML, 5 JS/TS, 22 tests, 2 security, 2 routes |
| [`sale_timesheet_margin`](addons/sale_timesheet_margin.md) | Sales/Sales | Bridge module between Sales Margin and Sales Timesheet | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`sales_team`](addons/sales_team.md) | Sales/Sales | Sales Teams | 2 | 12 Python, 8 XML, 4 JS/TS, 5 tests, 2 security, 0 routes |
| [`sms`](addons/sms.md) | Sales/Sales | SMS Text Messaging | 4 | 31 Python, 20 XML, 15 JS/TS, 4 tests, 1 security, 1 routes |
| [`uom`](addons/uom.md) | Sales/Sales | Not declared | 1 | 8 Python, 5 XML, 2 JS/TS, 3 tests, 2 security, 0 routes |
| [`website_crm_iap_reveal`](addons/website_crm_iap_reveal.md) | Sales/CRM | Generate Leads/Opportunities from your website's traffic | 4 | 12 Python, 7 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |

## Services & Projects (16 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`portal_discuss`](addons/portal_discuss.md) | Services | Not declared | 2 | 10 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`portal_rating`](addons/portal_rating.md) | Services | Not declared | 2 | 9 Python, 10 XML, 19 JS/TS, 0 tests, 0 security, 1 routes |
| [`project`](addons/project.md) | Services/Project | Manage tasks and collaborate on projects | 8 | 82 Python, 74 XML, 145 JS/TS, 39 tests, 2 security, 9 routes |
| [`project_hr_expense`](addons/project_hr_expense.md) | Services/expenses | Project expenses | 2 | 7 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`project_hr_skills`](addons/project_hr_skills.md) | Services/Project | Project skills | 2 | 7 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`project_mail_plugin`](addons/project_mail_plugin.md) | Services/Project | Integrate your inbox with projects | 2 | 6 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 3 routes |
| [`project_mrp`](addons/project_mrp.md) | Services/Project | Monitor MRP using project | 2 | 9 Python, 3 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`project_mrp_account`](addons/project_mrp_account.md) | Services/Project | Monitor MRP account using project | 3 | 11 Python, 3 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`project_mrp_sale`](addons/project_mrp_sale.md) | Services/Project | Technical Bridge | 3 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`project_purchase`](addons/project_purchase.md) | Services/Project | Monitor purchase in project | 2 | 12 Python, 3 XML, 1 JS/TS, 2 tests, 0 security, 1 routes |
| [`project_purchase_stock`](addons/project_purchase_stock.md) | Services/Project | Not declared | 2 | 9 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`project_sale_expense`](addons/project_sale_expense.md) | Services/Project | Not declared | 3 | 9 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`project_sms`](addons/project_sms.md) | Services/Project | Send text messages when project/task stage move | 2 | 10 Python, 4 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`project_stock`](addons/project_stock.md) | Services/Project | Link Stock pickings to Project | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`project_stock_account`](addons/project_stock_account.md) | Services/Project | Handle analytics in Stock pickings with Project | 2 | 9 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`project_todo`](addons/project_todo.md) | Productivity/To-Do | Organize your work with memos and to-do lists | 1 | 17 Python, 8 XML, 28 JS/TS, 10 tests, 1 security, 0 routes |

## Supply Chain & Manufacturing (37 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`barcodes`](addons/barcodes.md) | Supply Chain/Inventory | Scan and Parse Barcodes | 1 | 9 Python, 7 XML, 11 JS/TS, 2 tests, 1 security, 0 routes |
| [`barcodes_gs1_nomenclature`](addons/barcodes_gs1_nomenclature.md) | Supply Chain/Inventory | Parse barcodes according to the GS1-128 specifications | 2 | 8 Python, 2 XML, 6 JS/TS, 2 tests, 0 security, 0 routes |
| [`maintenance`](addons/maintenance.md) | Supply Chain/Maintenance | Track equipment and manage maintenance requests | 1 | 9 Python, 9 XML, 9 JS/TS, 4 tests, 2 security, 0 routes |
| [`mrp`](addons/mrp.md) | Supply Chain/Manufacturing | Manufacturing Orders & BOMs | 3 | 69 Python, 62 XML, 52 JS/TS, 25 tests, 2 security, 0 routes |
| [`mrp_account`](addons/mrp_account.md) | Supply Chain/Manufacturing | Analytic accounting in Manufacturing | 2 | 24 Python, 13 XML, 4 JS/TS, 6 tests, 1 security, 0 routes |
| [`mrp_delivery`](addons/mrp_delivery.md) | Shipping Connectors | Carrier with kits | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mrp_landed_costs`](addons/mrp_landed_costs.md) | Supply Chain/Manufacturing | Landed Costs on Manufacturing Order | 2 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mrp_product_expiry`](addons/mrp_product_expiry.md) | Supply Chain/Manufacturing | Manufacturing Expiry | 2 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mrp_repair`](addons/mrp_repair.md) | Supply Chain/Inventory | Not declared | 2 | 9 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`mrp_subcontracting`](addons/mrp_subcontracting.md) | Supply Chain/Manufacturing | Subcontract Productions | 1 | 28 Python, 25 XML, 12 JS/TS, 4 tests, 1 security, 3 routes |
| [`mrp_subcontracting_account`](addons/mrp_subcontracting_account.md) | Supply Chain/Manufacturing | Not declared | 2 | 7 Python, 0 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`mrp_subcontracting_dropshipping`](addons/mrp_subcontracting_dropshipping.md) | Supply Chain/Purchase | Not declared | 2 | 18 Python, 2 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`mrp_subcontracting_landed_costs`](addons/mrp_subcontracting_landed_costs.md) | Supply Chain/Manufacturing | Advanced views to manage landed cost for subcontracting orders | 2 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`mrp_subcontracting_purchase`](addons/mrp_subcontracting_purchase.md) | Supply Chain/Purchase | Not declared | 2 | 17 Python, 3 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`product_expiry`](addons/product_expiry.md) | Supply Chain/Inventory | Not declared | 1 | 22 Python, 15 XML, 4 JS/TS, 3 tests, 2 security, 0 routes |
| [`project_mrp_stock_landed_costs`](addons/project_mrp_stock_landed_costs.md) | Supply Chain/Manufacturing | Technical Bridge | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`project_stock_landed_costs`](addons/project_stock_landed_costs.md) | Supply Chain/Inventory | Technical Bridge | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`purchase`](addons/purchase.md) | Supply Chain/Purchase | Purchase orders, tenders and agreements | 1 | 38 Python, 33 XML, 21 JS/TS, 13 tests, 2 security, 5 routes |
| [`purchase_alternative`](addons/purchase_alternative.md) | Supply Chain/Purchase | Not declared | 1 | 10 Python, 5 XML, 3 JS/TS, 3 tests, 1 security, 0 routes |
| [`purchase_alternative_sale`](addons/purchase_alternative_sale.md) | Supply Chain/Purchase | Not declared | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`purchase_alternative_stock`](addons/purchase_alternative_stock.md) | Supply Chain/Purchase | Not declared | 2 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`purchase_edi_ubl_bis3`](addons/purchase_edi_ubl_bis3.md) | Supply Chain/Purchase | Not declared | 2 | 9 Python, 3 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`purchase_mrp`](addons/purchase_mrp.md) | Supply Chain/Purchase | Not declared | 2 | 15 Python, 5 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`purchase_product_matrix`](addons/purchase_product_matrix.md) | Supply Chain/Purchase | Add variants to your purchase orders through an Order Grid Entry. | 2 | 6 Python, 4 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`purchase_repair`](addons/purchase_repair.md) | Supply Chain/Purchase | Keep track of linked purchase and repair orders | 2 | 7 Python, 2 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`purchase_requisition`](addons/purchase_requisition.md) | Supply Chain/Purchase | Not declared | 1 | 9 Python, 7 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`purchase_requisition_stock`](addons/purchase_requisition_stock.md) | Supply Chain/Purchase | Not declared | 2 | 8 Python, 2 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`purchase_stock`](addons/purchase_stock.md) | Supply Chain/Purchase | Purchase Orders, Receipts, Vendor Bills for Stock | 2 | 48 Python, 22 XML, 16 JS/TS, 24 tests, 1 security, 0 routes |
| [`repair`](addons/repair.md) | Supply Chain/Inventory | Repair damaged products | 2 | 24 Python, 14 XML, 3 JS/TS, 4 tests, 1 security, 0 routes |
| [`stock`](addons/stock.md) | Supply Chain/Inventory | Manage your stock and logistics activities | 3 | 96 Python, 107 XML, 55 JS/TS, 32 tests, 2 security, 1 routes |
| [`stock_account`](addons/stock_account.md) | Supply Chain/Inventory | Inventory, Logistic, Valuation, Accounting | 2 | 32 Python, 16 XML, 4 JS/TS, 8 tests, 2 security, 0 routes |
| [`stock_delivery`](addons/stock_delivery.md) | Shipping Connectors | Not declared | 3 | 30 Python, 21 XML, 1 JS/TS, 8 tests, 1 security, 0 routes |
| [`stock_dropshipping`](addons/stock_dropshipping.md) | Supply Chain/Inventory | Drop Shipping | 1 | 18 Python, 5 XML, 0 JS/TS, 7 tests, 0 security, 0 routes |
| [`stock_fleet`](addons/stock_fleet.md) | Not declared | Stock Transport Management | 2 | 9 Python, 9 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`stock_landed_costs`](addons/stock_landed_costs.md) | Supply Chain/Inventory | Landed Costs | 2 | 18 Python, 5 XML, 0 JS/TS, 8 tests, 1 security, 0 routes |
| [`stock_maintenance`](addons/stock_maintenance.md) | Supply Chain/Inventory | See lots used in maintenance | 2 | 5 Python, 2 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`stock_sms`](addons/stock_sms.md) | Supply Chain/Inventory | Send text messages when final stock move | 2 | 8 Python, 3 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |

## Testing & Developer Tools (37 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`populate`](addons/populate.md) | Hidden/Tools | Generate synthetic data for an Odoo database | 1 | 30 Python, 0 XML, 0 JS/TS, 0 tests, 1 security, 0 routes |
| [`test_base_automation`](addons/test_base_automation.md) | Hidden | Base Automation Tests: Ensure Flow Robustness | 1 | 8 Python, 0 XML, 1 JS/TS, 5 tests, 1 security, 0 routes |
| [`test_crm_full`](addons/test_crm_full.md) | Hidden/Tests | Not declared | 10 | 5 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`test_event_full`](addons/test_event_full.md) | Hidden/Tests | Not declared | 13 | 12 Python, 2 XML, 4 JS/TS, 10 tests, 0 security, 0 routes |
| [`test_html_field_history`](addons/test_html_field_history.md) | Hidden | Not declared | 1 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`test_import_export`](addons/test_import_export.md) | Hidden | Base Import & Export Tests: Ensure Flow Robustness | 4 | 15 Python, 0 XML, 0 JS/TS, 9 tests, 1 security, 0 routes |
| [`test_mail`](addons/test_mail.md) | Hidden | Mail Tests: performances and tests specific to mail | 4 | 43 Python, 3 XML, 17 JS/TS, 36 tests, 1 security, 0 routes |
| [`test_mail_full`](addons/test_mail_full.md) | Hidden | Mail Tests: performances and tests specific to mail with all sub-modules | 12 | 21 Python, 2 XML, 11 JS/TS, 16 tests, 1 security, 5 routes |
| [`test_mail_sms`](addons/test_mail_sms.md) | Hidden | SMS Tests: performances and tests specific to SMS | 5 | 18 Python, 0 XML, 0 JS/TS, 15 tests, 1 security, 0 routes |
| [`test_populate`](addons/test_populate.md) | Hidden/Tests | Test module for Odoo's Populate | 1 | 38 Python, 1 XML, 0 JS/TS, 35 tests, 1 security, 0 routes |
| [`test_resource`](addons/test_resource.md) | Hidden | Not declared | 1 | 14 Python, 0 XML, 0 JS/TS, 11 tests, 1 security, 0 routes |
| [`test_sale_product_configurators`](addons/test_sale_product_configurators.md) | Hidden | Test Suite for Sale Product Configurator | 3 | 6 Python, 0 XML, 12 JS/TS, 4 tests, 0 security, 0 routes |
| [`test_sale_purchase_edi_ubl`](addons/test_sale_purchase_edi_ubl.md) | Hidden | Sale & Purchase Order EDI Tests: Ensure Flow Robustness | 2 | 4 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_spreadsheet`](addons/test_spreadsheet.md) | Hidden | Spreadsheet Test, mainly to test the mixin behavior | 1 | 6 Python, 1 XML, 0 JS/TS, 2 tests, 2 security, 0 routes |
| [`test_translation_mode`](addons/test_translation_mode.md) | Hidden | In-context and interactive translation mode to streamline the module translation process using Weblate | 1 | 7 Python, 3 XML, 8 JS/TS, 0 tests, 0 security, 0 routes |
| [`test_utm`](addons/test_utm.md) | Hidden | UTM Tests: tests specific to the UTM module | 1 | 7 Python, 0 XML, 0 JS/TS, 4 tests, 1 security, 0 routes |
| [`test_website`](addons/test_website.md) | Hidden | Website Test, mainly for module install/uninstall tests | 3 | 35 Python, 8 XML, 19 JS/TS, 28 tests, 2 security, 37 routes |
| [`test_website_modules`](addons/test_website_modules.md) | Hidden | Not declared | 8 | 7 Python, 0 XML, 1 JS/TS, 5 tests, 0 security, 0 routes |
| [`test_website_slides_full`](addons/test_website_slides_full.md) | Hidden/Tests | Not declared | 3 | 4 Python, 2 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_assetsbundle`](addons/test_assetsbundle.md) | Hidden/Tests | Not declared | 1 | 10 Python, 8 XML, 7 JS/TS, 4 tests, 0 security, 1 routes |
| [`test_base`](addons/test_base.md) | Hidden/Tests | Not declared | 1 | 112 Python, 10 XML, 0 JS/TS, 107 tests, 1 security, 0 routes |
| [`test_install_auto`](addons/test_install_auto.md) | Hidden/Tools | Not declared | 1 | 4 Python, 1 XML, 0 JS/TS, 4 tests, 0 security, 0 routes |
| [`test_install_base`](addons/test_install_base.md) | Hidden/Tools | Not declared | 1 | 2 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_install_fail`](addons/test_install_fail.md) | Hidden/Tools | Not declared | 1 | 2 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_data_module`](addons/test_data_module.md) | Hidden/Tests | Not declared | 0 | 1 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`test_data_module_install`](addons/test_data_module_install.md) | Hidden/Tests | Not declared | 1 | 4 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_http`](addons/test_http.md) | Hidden/Tests | Not declared | 4 | 27 Python, 2 XML, 0 JS/TS, 20 tests, 0 security, 44 routes |
| [`test_inherit`](addons/test_inherit.md) | Hidden/Tests | Not declared | 2 | 11 Python, 1 XML, 0 JS/TS, 3 tests, 1 security, 0 routes |
| [`test_inherit_depends`](addons/test_inherit_depends.md) | Hidden/Tests | Not declared | 2 | 5 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_inherits_depends`](addons/test_inherits_depends.md) | Hidden/Tests | Not declared | 1 | 5 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_l10n`](addons/test_l10n.md) | Hidden/Tests | Not declared | 1 | 5 Python, 0 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`test_lint`](addons/test_lint.md) | Hidden/Tests | Not declared | 1 | 29 Python, 0 XML, 0 JS/TS, 27 tests, 0 security, 0 routes |
| [`test_main_flows`](addons/test_main_flows.md) | Hidden/Tests | Not declared | 6 | 5 Python, 0 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`test_tests`](addons/test_tests.md) | Hidden/Tests | Not declared | 2 | 16 Python, 1 XML, 0 JS/TS, 11 tests, 1 security, 0 routes |
| [`test_translation`](addons/test_translation.md) | Hidden/Tests | Not declared | 2 | 11 Python, 3 XML, 2 JS/TS, 7 tests, 1 security, 0 routes |
| [`test_uninstall`](addons/test_uninstall.md) | Hidden/Tests | Not declared | 1 | 3 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`test_web`](addons/test_web.md) | Hidden/Tests | Not declared | 2 | 24 Python, 0 XML, 2 JS/TS, 20 tests, 0 security, 0 routes |

## Website & eCommerce (56 modules)
| Module | Manifest category | Summary | Dependencies | Evidence |
|---|---|---|---:|---|
| [`html_builder`](addons/html_builder.md) | Not declared | Generic html builder | 1 | 7 Python, 81 XML, 214 JS/TS, 2 tests, 0 security, 0 routes |
| [`html_editor`](addons/html_editor.md) | Hidden | A Html Editor component and plugin system. | 3 | 26 Python, 75 XML, 395 JS/TS, 11 tests, 1 security, 17 routes |
| [`http_routing`](addons/http_routing.md) | Hidden | Web Routing | 1 | 11 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 2 routes |
| [`im_livechat`](addons/im_livechat.md) | Website/Live Chat | Chat with your website visitors | 4 | 70 Python, 78 XML, 185 JS/TS, 24 tests, 2 security, 38 routes |
| [`theme_default`](addons/theme_default.md) | Theme | Not declared | 1 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`website`](addons/website.md) | Website/Website | Enterprise website builder | 11 | 103 Python, 418 XML, 674 JS/TS, 49 tests, 2 security, 65 routes |
| [`website_address_autocomplete`](addons/website_address_autocomplete.md) | Website/Website | Assist your users with automatic completion & suggestions when filling their address | 2 | 9 Python, 3 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_blog`](addons/website_blog.md) | Website/Website | Publish blog posts, announces, news | 3 | 18 Python, 27 XML, 33 JS/TS, 7 tests, 2 security, 4 routes |
| [`website_cf_turnstile`](addons/website_cf_turnstile.md) | Website/Website | Not declared | 1 | 5 Python, 2 XML, 7 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_crm`](addons/website_crm.md) | Website/Website | Generate leads from a contact form | 2 | 12 Python, 6 XML, 4 JS/TS, 4 tests, 1 security, 0 routes |
| [`website_crm_livechat`](addons/website_crm_livechat.md) | Website/Website | View livechat sessions for leads | 3 | 8 Python, 1 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_crm_partner_assign`](addons/website_crm_partner_assign.md) | Website/Website | Publish your resellers/partners and forward leads to them | 7 | 19 Python, 17 XML, 2 JS/TS, 4 tests, 1 security, 5 routes |
| [`website_crm_sms`](addons/website_crm_sms.md) | Website/Website | Allows to send sms to website visitor that have lead | 2 | 6 Python, 0 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_customer`](addons/website_customer.md) | Website/Website | Publish your customer references | 3 | 9 Python, 4 XML, 1 JS/TS, 2 tests, 1 security, 2 routes |
| [`website_event`](addons/website_event.md) | Marketing/Events | Publish events, sell tickets | 5 | 28 Python, 35 XML, 23 JS/TS, 10 tests, 2 security, 9 routes |
| [`website_event_booth`](addons/website_event_booth.md) | Marketing/Events | Events, display your booths on your website | 2 | 10 Python, 6 XML, 1 JS/TS, 2 tests, 1 security, 6 routes |
| [`website_event_booth_exhibitor`](addons/website_event_booth_exhibitor.md) | Marketing/Events | Event Booths, automatically create a sponsor. | 2 | 9 Python, 6 XML, 3 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_event_booth_sale`](addons/website_event_booth_sale.md) | Marketing/Events | Events, sell your booths online | 3 | 11 Python, 2 XML, 4 JS/TS, 3 tests, 0 security, 1 routes |
| [`website_event_booth_sale_exhibitor`](addons/website_event_booth_sale_exhibitor.md) | Marketing/Events | Bridge module between website_event_booth_exhibitor and website_event_booth_sale. | 2 | 4 Python, 0 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_event_crm`](addons/website_event_crm.md) | Website/Website | Not declared | 2 | 7 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`website_event_exhibitor`](addons/website_event_exhibitor.md) | Marketing/Events | Event: manage sponsors and exhibitors | 1 | 14 Python, 14 XML, 2 JS/TS, 3 tests, 1 security, 3 routes |
| [`website_event_sale`](addons/website_event_sale.md) | Website/Website | Sell event tickets online | 3 | 21 Python, 5 XML, 4 JS/TS, 7 tests, 0 security, 1 routes |
| [`website_event_track`](addons/website_event_track.md) | Marketing | Sponsors, Tracks, Agenda, Event News | 1 | 29 Python, 33 XML, 11 JS/TS, 8 tests, 1 security, 14 routes |
| [`website_event_track_live`](addons/website_event_track_live.md) | Marketing/Events | Support live tracks: streaming, participation, youtube | 1 | 7 Python, 5 XML, 3 JS/TS, 0 tests, 0 security, 1 routes |
| [`website_event_track_live_quiz`](addons/website_event_track_live_quiz.md) | Marketing/Events | Bridge module to support quiz features during "live" tracks.  | 2 | 4 Python, 3 XML, 2 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_event_track_quiz`](addons/website_event_track_quiz.md) | Marketing/Events | Quizzes on tracks | 2 | 10 Python, 12 XML, 2 JS/TS, 0 tests, 1 security, 5 routes |
| [`website_forum`](addons/website_forum.md) | Website/Website | Manage a forum with FAQ and Q&A | 3 | 34 Python, 35 XML, 21 JS/TS, 13 tests, 1 security, 41 routes |
| [`website_google_map`](addons/website_google_map.md) | Website/Website | Show your company address on Google Maps | 2 | 4 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 1 routes |
| [`website_hr_recruitment`](addons/website_hr_recruitment.md) | Website/Website | Manage your online hiring process | 2 | 15 Python, 11 XML, 7 JS/TS, 3 tests, 2 security, 5 routes |
| [`website_hr_recruitment_livechat`](addons/website_hr_recruitment_livechat.md) | Website/Live Chat | Chatbot for the HR Recruitment | 2 | 2 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_links`](addons/website_links.md) | Website/Website | Generate trackable & short URLs | 2 | 10 Python, 5 XML, 6 JS/TS, 4 tests, 1 security, 0 routes |
| [`website_livechat`](addons/website_livechat.md) | Website/Live Chat | Chat with your website visitors | 2 | 28 Python, 9 XML, 37 JS/TS, 11 tests, 1 security, 2 routes |
| [`website_mail`](addons/website_mail.md) | Website/Website | Website Module for Mail | 2 | 7 Python, 1 XML, 2 JS/TS, 0 tests, 0 security, 2 routes |
| [`website_mail_group`](addons/website_mail_group.md) | Not declared | Add a website snippet for the mail groups. | 2 | 8 Python, 5 XML, 3 JS/TS, 2 tests, 0 security, 1 routes |
| [`website_mass_mailing`](addons/website_mass_mailing.md) | Website/Website | Attract visitors to subscribe to mailing lists | 3 | 12 Python, 12 XML, 18 JS/TS, 7 tests, 1 security, 2 routes |
| [`website_mass_mailing_event`](addons/website_mass_mailing_event.md) | Marketing/Email Marketing/Website | Add pre-filled snippets in mass_mailing with an event snapshot | 2 | 2 Python, 3 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_mass_mailing_sms`](addons/website_mass_mailing_sms.md) | Website/Website | Attract visitors to subscribe to mailing lists | 2 | 6 Python, 3 XML, 0 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_partner`](addons/website_partner.md) | Website/Website | Partner module for website | 1 | 6 Python, 4 XML, 0 JS/TS, 0 tests, 0 security, 1 routes |
| [`website_partnership`](addons/website_partnership.md) | Website/Website | Publish your partners on your website | 2 | 7 Python, 7 XML, 1 JS/TS, 0 tests, 1 security, 1 routes |
| [`website_payment`](addons/website_payment.md) | Website/Website | Payment integration with website | 3 | 10 Python, 7 XML, 3 JS/TS, 2 tests, 0 security, 3 routes |
| [`website_profile`](addons/website_profile.md) | Website/Website | Access the website profile of the users | 3 | 12 Python, 5 XML, 5 JS/TS, 3 tests, 1 security, 8 routes |
| [`website_project`](addons/website_project.md) | Website/Website | Add a task suggestion form to your website | 2 | 8 Python, 3 XML, 2 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_sale`](addons/website_sale.md) | Website/Website | Sell your products online | 8 | 123 Python, 108 XML, 165 JS/TS, 58 tests, 3 security, 62 routes |
| [`website_sale_collect`](addons/website_sale_collect.md) | Website/Website | Not declared | 3 | 31 Python, 18 XML, 8 JS/TS, 12 tests, 0 security, 3 routes |
| [`website_sale_gelato`](addons/website_sale_gelato.md) | Website/Website | Not declared | 2 | 10 Python, 2 XML, 0 JS/TS, 3 tests, 0 security, 0 routes |
| [`website_sale_loyalty`](addons/website_sale_loyalty.md) | Website/Website | Use coupon, promotion, gift cards and loyalty programs in your eCommerce store | 3 | 27 Python, 10 XML, 12 JS/TS, 11 tests, 1 security, 8 routes |
| [`website_sale_mass_mailing`](addons/website_sale_mass_mailing.md) | Website/Website | Let new customers sign up for a newsletter during checkout | 3 | 9 Python, 3 XML, 1 JS/TS, 2 tests, 0 security, 0 routes |
| [`website_sale_mrp`](addons/website_sale_mrp.md) | Website/Website | Manage Kit product inventory & availability | 2 | 8 Python, 0 XML, 2 JS/TS, 2 tests, 0 security, 1 routes |
| [`website_sale_project`](addons/website_sale_project.md) | Website/Website | Bridge module between website_sale and project | 2 | 4 Python, 1 XML, 1 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_sale_slides`](addons/website_sale_slides.md) | Website/eLearning | Sell your courses online | 2 | 14 Python, 14 XML, 5 JS/TS, 3 tests, 0 security, 1 routes |
| [`website_sale_stock`](addons/website_sale_stock.md) | Website/Website | Manage product inventory & availability | 3 | 31 Python, 17 XML, 17 JS/TS, 16 tests, 0 security, 2 routes |
| [`website_slides`](addons/website_slides.md) | Website/eLearning | Manage and publish an eLearning platform | 5 | 47 Python, 65 XML, 75 JS/TS, 16 tests, 2 security, 39 routes |
| [`website_slides_forum`](addons/website_slides_forum.md) | Website/eLearning | Allows to link forum on a course | 2 | 9 Python, 9 XML, 0 JS/TS, 2 tests, 1 security, 0 routes |
| [`website_slides_survey`](addons/website_slides_survey.md) | Website/eLearning | Add certification capabilities to your courses | 2 | 15 Python, 21 XML, 3 JS/TS, 4 tests, 1 security, 3 routes |
| [`website_sms`](addons/website_sms.md) | Website/Website | Allows to send sms to website visitor | 2 | 4 Python, 1 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
| [`website_timesheet`](addons/website_timesheet.md) | Website/Website | Allow hiding timesheet information in the portal | 2 | 4 Python, 0 XML, 0 JS/TS, 0 tests, 0 security, 0 routes |
