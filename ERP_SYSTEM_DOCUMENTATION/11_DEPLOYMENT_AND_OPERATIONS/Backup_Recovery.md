# Backup and Recovery — Phase 11

## Implemented database operations

The source includes database dump and restore functionality in `odoo/modules/db.py` and the database CLI (`odoo/cli/db.py`). Supported application-level dump formats are `zip` and `dump`/`pg_dump`; the implementation can include the filestore for zip backups. Restore operations include options for neutralizing or preserving database identity, as implemented by the CLI.

## Not established by the codebase

A production backup schedule, retention policy, encryption/key management, off-site replication, RPO/RTO, restore cadence, disaster-recovery topology, and PostgreSQL HA configuration are **Not Found in Codebase**. These must be designed, tested, and documented for the target deployment.
