# Environment Variables — Phase 11

Static source inspection identified **72** environment-variable names or configuration environment mappings. Values are intentionally excluded. The complete list is [`Environment_Variable_Inventory.csv`](Environment_Variable_Inventory.csv).

These names include PostgreSQL connection variables, Odoo runtime/test/browser/profile controls, HTTP/socket integration variables, proxy/webhook-related values, and standard process environment variables. A name's presence does not prove that a deployment sets it or that a feature is enabled.
