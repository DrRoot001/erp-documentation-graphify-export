# Deployment Guide — Phase 11

## Verified deployment targets

- Debian/systemd packaging is present (`debian/odoo.service`, `debian/odoo.conf`).
- Python package installation is present (`setup.py`, `requirements.txt`, `setup/odoo`).
- Windows and IoT setup assets are present under `setup/win32` and `setup/iot_box_builder`.
- PostgreSQL is the persistence dependency established by source and package requirements.

Dockerfiles, Docker Compose manifests, Kubernetes manifests, and cloud-provider deployment definitions were not found in the inspected repository snapshot. TLS termination, reverse proxying, load balancing, process scaling, database HA, object storage, and monitoring are deployment responsibilities rather than verified repository deployment topology.

Machine-readable evidence is in [`Deployment_Artifact_Inventory.csv`](Deployment_Artifact_Inventory.csv).
