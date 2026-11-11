# Component Architecture

## Source-to-clone mapping

| Source boundary | Clone boundary | Evidence/status |
|---|---|---|
| `odoo-bin`, `odoo/cli/`, service runtime | Application bootstrap and CLI | VERIFIED |
| `odoo/http/` and controller routes | API/router layer | VERIFIED |
| `odoo/orm/`, registry, SQL DB | Persistence abstraction and transaction manager | VERIFIED source; clone design equivalent |
| `odoo/modules/` and manifests | Module registry/dependency loader | VERIFIED |
| Addon models/services | Domain modules/application services | VERIFIED source; technology-independent translation |
| XML/JS/TS/assets | Frontend/view/component layer | VERIFIED |
| Cron/background/bus | Job/event processing | VERIFIED capability family |
| Optional providers | Integration adapters | VERIFIED capability family |

Components are logical boundaries. The source does not establish independent deployable services.
