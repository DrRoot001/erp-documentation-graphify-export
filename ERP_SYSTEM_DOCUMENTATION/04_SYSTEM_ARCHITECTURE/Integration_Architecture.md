# Integration Architecture

Integration capability is addon-based. Static evidence includes LDAP/OAuth/passkey/TOTP authentication, Google services, cloud storage providers, payment providers, SMS, IoT, localization/e-invoicing, and mail-related modules. Each integration is optional and its credentials/configuration are deployment-specific.

```mermaid
flowchart LR
  ODOO[ERP SYSTEM server]
  AUTH[LDAP / OAuth / passkey / TOTP]
  CLOUD[Cloud storage]
  GOOGLE[Google services]
  PAY[Payment providers]
  MSG[Mail / SMS providers]
  IOT[IoT devices/services]
  TAX[Localization / e-invoicing networks]
  ODOO <--> AUTH
  ODOO <--> CLOUD
  ODOO <--> GOOGLE
  ODOO <--> PAY
  ODOO <--> MSG
  ODOO <--> IOT
  ODOO <--> TAX
```
