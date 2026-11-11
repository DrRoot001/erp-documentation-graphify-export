# Backup and Recovery

The source provides application/database dump and restore functionality, including zip/dump/pg_dump paths and optional filestore handling. A clone must provide encrypted, access-controlled backups; database and file-storage consistency; retention; off-site copies; restore validation; point-in-time strategy where required; and documented recovery procedures.

Production schedule, retention, encryption/key management, replication, RPO/RTO, and DR topology are `UNKNOWN`/Not Found in the source and require explicit deployment decisions.
