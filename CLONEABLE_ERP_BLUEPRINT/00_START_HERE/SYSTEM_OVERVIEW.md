# System Overview

## Verified source product

The source snapshot identifies itself as Odoo 20.0. It is a Python/PostgreSQL modular business application platform with a core framework and 666 addon manifests spanning business applications, localizations, integrations, web/client capabilities, tests, and deployment support.

## Clone target

The clone target is an ERP SYSTEM with equivalent documented capabilities, workflows, data semantics, access behavior, integrations, and operational responsibilities. Equivalence is defined by the requirements and evidence registers, not by reproducing Odoo class names or internal APIs.

## Source baseline

| Evidence | Count |
|---|---:|
| Repository files inventoried | 50,889 |
| Addon manifests | 666 |
| Python files | 9,529 |
| JavaScript/TypeScript files | 6,899 |
| XML files | 6,101 |
| Controller-derived route records | 669 |
| ORM entity declarations | 4,209 |
| ORM field declarations | 17,272 |
| ORM relationship declarations | 5,290 |
| Model-access declarations | 2,577 |
| Test artifacts | 3,470 |
| Functional requirements | 2,963 |

These are static evidence counts. They are not claims about a particular installed tenant, runtime coverage, performance, or production topology.

## Two architecture views

1. **Original implementation view:** Odoo core, addon manifests, Python ORM, PostgreSQL, HTTP routing, XML/client assets, access declarations, scheduled work, and integrations.
2. **Cloneable logical view:** frontend, API, application services, domain modules, persistence, authorization, event/background processing, integrations, files, reporting, cache, and observability.

The second view is the implementation contract for a new team; the first view preserves source traceability.
