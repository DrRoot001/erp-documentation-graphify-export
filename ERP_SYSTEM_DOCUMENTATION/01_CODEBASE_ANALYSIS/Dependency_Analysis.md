# Dependency Analysis

## Internal dependency mechanism

Addon manifests declare `depends`, data files, demo data, assets, installability, and application flags. The module graph and loading pipeline are implemented in `odoo/modules/module_graph.py`, `odoo/modules/loading.py`, and `odoo/modules/module.py`. A module is therefore coupled to its declared dependencies and to the shared ORM registry.

## Most referenced addon dependencies

| Dependency | Referenced by manifests |
|---|---:|
| `account` | 158 |
| `point_of_sale` | 48 |
| `mail` | 44 |
| `account_edi_ubl_cii` | 41 |
| `base` | 41 |
| `web` | 34 |
| `payment` | 25 |
| `sale` | 25 |
| `website` | 21 |
| `base_setup` | 20 |
| `sms` | 18 |
| `portal` | 17 |
| `digest` | 17 |
| `l10n_syscohada` | 17 |
| `crm` | 16 |
| `hr` | 15 |
| `website_sale` | 15 |
| `mass_mailing` | 15 |
| `spreadsheet_dashboard` | 13 |
| `l10n_account_withholding_tax` | 12 |
| `stock_account` | 11 |
| `stock` | 11 |
| `sale_stock` | 11 |
| `mrp` | 11 |
| `web_tour` | 10 |
| `event` | 10 |
| `project` | 10 |
| `l10n_fr_account` | 10 |
| `resource` | 9 |
| `utm` | 9 |
| `sale_management` | 9 |
| `account_debit_note` | 9 |
| `pos_self_order` | 9 |
| `phone_validation` | 8 |
| `sale_project` | 8 |
| `html_editor` | 8 |
| `l10n_gcc_invoice` | 8 |
| `l10n_latam_invoice_document` | 8 |
| `l10n_din5008` | 8 |
| `purchase` | 8 |

## Runtime/package dependencies

`setup.py` declares the Python runtime dependencies. Important categories include PostgreSQL (`psycopg2`), HTTP/server (`werkzeug`, `gevent`, `greenlet`, `requests`, `urllib3`), security/crypto (`cryptography`, `passlib`, `pyopenssl`), XML/document processing (`lxml`, `docutils`, `Jinja2`), media/reporting (`pillow`, `reportlab`, `pypdf`, `openpyxl`, `xlsxwriter`), localization/standards (`babel`, `python-stdnum`, `zeep`), and device support (`pyserial`, `pyusb`). Optional LDAP support is declared through the `ldap` extra.

## External integrations

Integration addons are present for authentication providers, Google services, cloud storage, payment acquirers, SMS, IoT, localization/e-invoicing, and other services. Presence of an addon is not proof that the integration is enabled or configured in a deployment.
