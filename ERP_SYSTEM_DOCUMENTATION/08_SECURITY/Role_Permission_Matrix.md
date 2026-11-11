# Role-Permission Matrix — Phase 8

A complete deployment matrix is generated from `Group_Inventory.csv`, `Model_Access_Inventory.csv`, `Record_Rule_Inventory.csv`, and `Route_Security_Matrix.csv`. The source snapshot contains 192 group declarations, 2,577 access rows, and 11 record rules.

| Security layer | Evidence | What can be concluded statically | Runtime requirement |
|---|---|---|---|
| Groups/roles | `Group_Inventory.csv` | Declared group XML IDs, names, categories, implied groups | Loaded group graph and assigned users |
| Model CRUD | `Model_Access_Inventory.csv` | Declared model/group CRUD flags | Effective access after module installation |
| Record rules | `Record_Rule_Inventory.csv` | Declared domains/group bindings/CRUD flags | Domain evaluation, company context, inheritance |
| Routes | `Route_Security_Matrix.csv` | Auth/type/CSRF/CORS/bearer metadata | Actual dispatch and provider/session state |

Do not treat this static matrix as proof that an actor can or cannot perform an action in a configured tenant.
