# Configuration Guide — Phase 11

Odoo configuration is implemented through `odoo/tools/config.py`, which registers CLI/config-file options, environment mappings, defaults, and type conversion. The repository contains **75** option declarations in the inspected configuration registry.

| Configuration area | Evidence |
|---|---|
| Configuration registry | `odoo/tools/config.py` |
| Debian example | `debian/odoo.conf` |
| Service invocation | `debian/odoo.service` |
| Machine-readable options | [`Configuration_Option_Inventory.csv`](Configuration_Option_Inventory.csv) |

Important option families include database connection and pooling, addon/module loading, HTTP/gevent ports, proxy mode, database filtering, test execution, logging, SMTP, workers, limits, and upgrade scripts. Exact defaults and validation are source-defined; review the inventory and source before changing production values.
