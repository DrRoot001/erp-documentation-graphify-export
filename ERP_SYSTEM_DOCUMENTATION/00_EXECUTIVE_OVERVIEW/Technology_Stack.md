# Technology Stack

| Layer | Verified implementation |
|---|---|
| Language/runtime | Python; release metadata requires Python >= 3.12 and supports through 3.14 (`odoo/release.py:31`). |
| Web/server | Werkzeug, gevent, threaded/prefork server code, HTTP routing and sessions (`odoo/service/server.py`, `odoo/http/`). |
| Persistence | PostgreSQL through psycopg2 and Odoo ORM/registry (`setup.py`, `odoo/sql_db.py`, `odoo/orm/`). |
| Frontend | JavaScript/TypeScript browser client, XML templates/views, SCSS/CSS assets. |
| Data/config | Python addon manifests, XML/CSV/JSON/SQL data, INI-style configuration. |
| Reporting/export | QWeb/XML reporting, PDF/reportlab/pypdf, XLSX/openpyxl/xlsxwriter dependencies. |
| Integrations | LDAP, OAuth, SMTP/mail, Google, payment providers, cloud storage, IoT, localization/e-invoicing, and other optional addons; activation is manifest/configuration dependent. |
| Testing | Python test modules under addon `tests` packages and test support modules. |
| Packaging/deployment | `setup.py`, `requirements.txt`, Debian packaging, systemd service, Windows/IOT setup assets. |

The complete dependency declarations are in `01_CODEBASE_ANALYSIS/Dependency_Analysis.md`; secret values are not copied into this package.
