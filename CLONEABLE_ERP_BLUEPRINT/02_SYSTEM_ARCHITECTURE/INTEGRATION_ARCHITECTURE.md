# Integration Architecture

Static evidence identifies 204 integration records and 37 authentication/security capability modules. Integration activation, credentials, rate limits, provider availability, and deployment topology are configuration-dependent.

```mermaid
flowchart LR
 ERP[ERP SYSTEM logical core] <--> AUTH[LDAP / OAuth / passkey / TOTP]
 ERP <--> MSG[SMTP / mail / SMS]
 ERP <--> PAY[Payment providers]
 ERP <--> CLOUD[Cloud storage]
 ERP <--> GOOGLE[Google services]
 ERP <--> IOT[IoT devices/services]
 ERP <--> TAX[Localization and e-invoicing networks]
 ERP <--> EXT[Other optional adapters]
```

Clone adapters must isolate provider-specific protocols, protect credentials, define timeout/retry behavior, and expose operational health. Exact provider contracts are specified only when present in the API/integration inventories.
