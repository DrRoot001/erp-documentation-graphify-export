# Installation Guide — Phase 11

## Verified installation surfaces

The repository provides a Python package entry point (`setup.py`), the `setup/odoo` launcher, dependency declarations in `requirements.txt` and `setup.py`, Debian packaging, and platform-specific setup assets. The runtime requires a compatible Python version, PostgreSQL, configured addon paths, and a service/process strategy.

The Debian service starts `/usr/bin/odoo` as the `odoo` user/group with `/etc/odoo/odoo.conf` and logs to `/var/log/odoo/odoo-server.log` (`debian/odoo.service`). The repository does not establish a universal production installation command for every operating system.

## Requirements requiring environment verification

- Python version is derived from `odoo/release.py` and enforced by package metadata.
- PostgreSQL client/server compatibility and credentials must be supplied by deployment.
- Python dependencies are declared in `setup.py` and `requirements.txt`; optional LDAP support is declared as an extra.
- Browser, PDF, geospatial, payment, IoT, and external-service capabilities may require additional system packages or credentials.

No secret values are reproduced in this documentation.
