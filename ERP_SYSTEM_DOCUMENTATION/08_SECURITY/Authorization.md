# Authorization — Phase 8

## Model access rights

The static access inventory contains 2,577 CSV rows. CRUD permission distribution:

- `cru` enabled: 236 rows
- `r` enabled: 845 rows
- `crud` enabled: 1,320 rows
- `cr` enabled: 22 rows
- `ru` enabled: 36 rows
- `cu` enabled: 9 rows
- `cud` enabled: 44 rows
- `u` enabled: 21 rows
- `c` enabled: 16 rows
- `rud` enabled: 5 rows
- `rd` enabled: 2 rows
- `d` enabled: 9 rows
- `crd` enabled: 2 rows
- `ud` enabled: 7 rows
- `cd` enabled: 3 rows


## Record rules

The XML inventory contains 11 access-rule declarations. Domains, groups, operation, and active flags are retained in `Record_Rule_Inventory.csv`; evaluation after inheritance and module loading requires a running registry.

## Route authorization

The route security matrix records auth/CSRF/readonly/CORS/bearer metadata for every extracted endpoint. It does not infer a group permission from `auth='user'`; ORM access and record-rule enforcement remain separate checks.
