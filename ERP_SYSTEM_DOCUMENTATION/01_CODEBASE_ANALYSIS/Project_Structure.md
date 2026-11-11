# Project Structure

| Area | Evidence | Responsibility |
|---|---|---|
| `odoo/` | Core Python package | Server, ORM, HTTP, module loading, CLI, services, tools. |
| `odoo/addons/` | Core addons | Base framework extensions and test/support modules shipped with the server. |
| `addons/` | 647 manifests | Business applications, integrations, localizations, web features, and tests. |
| `setup/` | Packaging and IOT builder assets | Installation, packaging, Windows/IOT support. |
| `debian/` | Debian packaging | Service unit, configuration, install/remove scripts, package metadata. |
| `.github/` | CI/issue metadata | Repository contribution and issue configuration. |
| Root files | `odoo-bin`, `setup.py`, `requirements.txt`, `README.md`, `SECURITY.md` | Entry point, packaging, dependencies, project guidance, disclosure guidance. |

The authoritative file-by-file inventory is `Repository_Inventory.csv`.
