# User Roles and Personas

## Evidence boundary

The source repository contains authorization groups, model-access declarations, route authentication metadata, and authentication modules. It does not define a single universal business-role taxonomy for every deployment. Therefore, the clone uses capability personas below as implementation viewpoints, not claims that each is a named source role.

| Persona | Evidence basis | Clone responsibility | Status |
|---|---|---|---|
| System operator | CLI, configuration, deployment, migration, service evidence | Install, configure, upgrade, monitor, back up, and restore | INFERRED |
| Authenticated business user | User/session/authentication and protected route/model evidence | Use authorized business capabilities | VERIFIED capability family |
| Portal/public actor | Public routes, portal/auth modules, website/ecommerce evidence | Access explicitly public or portal surfaces only | VERIFIED capability family |
| Scheduler/worker | Cron, scheduled files, background service evidence | Execute asynchronous work with controlled permissions | VERIFIED capability family |
| Integration provider | 204 integration records and route/webhook evidence | Exchange data with configured external systems | VERIFIED capability family |
| Developer/module maintainer | Manifest, ORM, extension, migration, test evidence | Build and maintain modules | INFERRED |

Named roles and permissions must be generated from the security inventories during later phases; no generic Admin/Manager/Employee matrix is asserted here.
