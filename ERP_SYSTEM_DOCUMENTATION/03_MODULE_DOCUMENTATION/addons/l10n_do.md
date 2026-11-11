# Module: l10n_do

- **Module ID:** MOD-166
- **Domain classification:** See `../Module_Hierarchy.md`
- **Source path:** `addons/l10n_do`
- **Manifest:** `addons/l10n_do/__manifest__.py`
- **Implementation assessment:** Fully implemented artifact surface
- **Application flag:** `not declared`
- **Category:** `Accounting/Localizations/Account Charts`
- **License:** `LGPL-3`

## 1. Overview

**Purpose:** No manifest summary declared

**Manifest description:**

Localization Module for Dominican Republic
===========================================

Catálogo de Cuentas e Impuestos para República Dominicana, Compatible para
**Internacionalización** con **NIIF** y alineado a las normas y regulaciones
de la Dirección General de Impuestos Internos (**DGII**).

**Este módulo consiste de:**

- Catálogo de Cuentas Estándar (alineado a DGII y NIIF)
- Catálogo de Impuestos con la mayoría de Impuestos Preconfigurados
        - ITBIS para compras y ventas
        - Retenciones de ITBIS
        - Retenciones de ISR
        - Grupos de Impuestos y Retenciones:
                - Telecomunicaiones
                - Proveedores de Materiales de Construcción
                - Personas Físicas Proveedoras de Servicios
        - Otros impuestos
- Secuencias Preconfiguradas para manejo de todos los NCF
        - Facturas con Valor Fiscal (para Ventas)
        - Facturas para Consumidores Finales
        - Notas de Débito y Crédito
        - Registro de Proveedores Informales
        - Registro de Ingreso Único
        - Registro de Gastos Menores
        - Gubernamentales
- Posiciones Fiscales para automatización de impuestos y retenciones
        - Cambios de Impuestos a Exenciones (Ej. Ventas al Estado)
        - Cambios de Impuestos a Retenciones (Ej. Compra Servicios al Exterior)
        - Entre otros

**Nota:**
Esta localización, aunque posee las secuencias para NCF, las mismas no pueden
ser utilizadas sin la instalación de módulos de terceros o desarrollo
adicional.

Estructura de Codificación del Catálogo de Cuentas:
===================================================

**Un dígito** representa la categoría/tipo de cuenta del del estado financiero.
**1** - Activo        **4** - Cuentas de Ingresos y Ganancias
**2** - Pasivo        **5** - Costos, Gastos y Pérdidas
**3** - Capital       **6** - Cuentas Liquidadoras de Resultados

**Dos dígitos** representan los rubros de agrupación:
11- Activo Corriente
21- Pasivo Corriente
31- Capital Contable

**Cuatro dígitos** se asignan a las cuentas de mayor: cuentas de primer orden
1101- Efectivo y Equivalentes de Efectivo
2101- Cuentas y Documentos por pagar
3101- Capital Social

**Seis dígitos** se asignan a las sub-cuentas: cuentas de segundo orden
110101 - Caja
210101 - Proveedores locales

**Ocho dígitos** son para las cuentas de tercer orden (las visualizadas
en Odoo):
1101- Efectivo y Equivalentes
110101- Caja
11010101 Caja General

**Scope evidence:** The module contains 23 files, including 9 Python, 8 XML, and 0 JavaScript/TypeScript files. The manifest declares dependencies: `account`, `l10n_latam_invoice_document`.

## 2. Module structure

- Model/business logic files: 4
- Controller/API files: 0
- XML/data/view/template files: 8
- Browser asset files: 0
- Security files: 0
- Test files: 0
- Scheduled/automation evidence files: 0
- Reporting evidence files: 0

## 3. Actors and permissions

The repository does not define one universal role model. Actors are therefore documented only where implementation surfaces establish them: authenticated users/portal users through controllers, administrators/operators through configuration and module lifecycle, and developers/QA through test artifacts. Exact groups, model permissions, and record rules require evaluating the module security XML/CSV in a configured database.

**Security evidence:** Not found in module

## 4. Functionalities

### Model and business logic

- **Description:** 4 model declarations, 7 methods, 0 constraint handlers, 0 onchange handlers, and 0 dependency declarations.
- **Evidence:** `addons/l10n_do/models/res_partner.py:7`, `addons/l10n_do/models/template_do.py:6`, `addons/l10n_do/models/account_tax.py:5`, `addons/l10n_do/models/account_move.py:4`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

### User interface and data

- **Description:** 8 XML files and 0 JavaScript/TypeScript files; static XML analysis found 57 record/template/menu identifiers.
- **Evidence:** `addons/l10n_do/demo/demo_account_journal.xml:3`, `addons/l10n_do/demo/demo_res_partner.xml:3`, `addons/l10n_do/demo/demo_company.xml:3`, `addons/l10n_do/demo/demo_company.xml:16`, `addons/l10n_do/data/account_tax_report_data.xml:3`, `addons/l10n_do/data/account_tax_report_data.xml:10`, `addons/l10n_do/data/account_tax_report_data.xml:17`, `addons/l10n_do/data/account_tax_report_data.xml:23`, `addons/l10n_do/data/account_tax_report_data.xml:29`, `addons/l10n_do/data/account_tax_report_data.xml:34`, `addons/l10n_do/data/account_tax_report_data.xml:41`, `addons/l10n_do/data/account_tax_report_data.xml:46`
- **Success condition:** The corresponding implementation is loaded and executes its configured operation.
- **Failure conditions:** Missing dependency, invalid input, access denial, database error, external-service failure, or rendering/test failure as applicable.
- **Status:** Implemented artifact surface; runtime enablement and exact behavior require verification.

## 5. Screens and user interface

- XML files: 8; representative identifiers: `demo_edi_sales_journal`, `demo_res_partner_tostadores`, `base.partner_demo_company_do`, `base.demo_company_do`, `tax_report`, `tax_report_balance`, `account_tax_report_total_operaciones`, `account_tax_report_2A`, `account_tax_report_2A2_base`, `account_tax_report_2A2_base_tag`, `account_tax_report_2A3_base`, `account_tax_report_2A3_base_tag`, `account_tax_report_2A4_base`, `account_tax_report_2A4_base_tag`, `account_tax_report_2A5_base`, `account_tax_report_2A5_base_tag`, `account_tax_report_2A6_base`, `account_tax_report_2A6_base_tag`, `account_tax_report_2A7_base`, `account_tax_report_2A7_base_tag`
- Menus: 0; representative evidence: Not found in module
- Templates: 0; representative evidence: Not found in module
- View/action field declarations: 4; representative evidence: `addons/l10n_do/views/account_move_views.xml:5`, `addons/l10n_do/views/account_move_views.xml:7`, `addons/l10n_do/views/account_tax_views.xml:5`, `addons/l10n_do/views/account_tax_views.xml:7`
- Browser assets: 0; representative files: Not found in module
- Route URLs, labels, fields, access restrictions, empty/loading/error states, and inherited view results require runtime/UI inspection; they are not inferred from filenames.

## 6. Business workflows

Static evidence supports the following module-level workflow pattern: module installation/update resolves manifest dependencies, loads Python/XML/assets/security declarations, and exposes configured models/controllers/views/jobs/reports. Domain-specific state transitions must be traced from the model methods, XML actions, controllers, and tests listed below. No workflow is marked complete solely from a module name.

- **Entry point evidence:** `addons/l10n_do/__manifest__.py`
- **HTTP entry points:** Not found in module
- **Scheduled entry points:** Not found in module
- **Report entry points:** Not found in module

## 7. Database interactions

- Model declarations: 4
- Representative model evidence: inherits `res.partner` (addons/l10n_do/models/res_partner.py:7); inherits `account.chart.template` (addons/l10n_do/models/template_do.py:6); inherits `account.tax` (addons/l10n_do/models/account_tax.py:5); inherits `account.move` (addons/l10n_do/models/account_move.py:4)
- CRUD operations, fields, constraints, indexes, and relationships are implemented in the referenced Python models and materialized in PostgreSQL at runtime. A deployment-specific schema is required for exact column/constraint documentation.

## 8. APIs and services

- Controller files: 0
- Route declarations: 0
- Route evidence: Not found in module
- Authentication mode, request/response schemas, pagination, idempotency, rate limits, retries, and external contracts require route-by-route source/runtime verification.

## 9. Module dependencies

- Declared dependencies: `account`, `l10n_latam_invoice_document`
- Upstream dependencies are resolved by the module graph; downstream extensions may inherit or extend this module through their own manifests and model/view inheritance.

## 10. Implementation assessment

- **Fully implemented artifact evidence:** Yes
- **Backend/model evidence:** Present
- **UI/data evidence:** Present
- **API evidence:** Not found
- **Security evidence:** Not found
- **Test evidence:** Not found
- **Runtime status:** Requires verification in a configured Odoo instance; static artifacts do not establish installation, enablement, production behavior, or test pass status.

## 11. Complete source inventory

- `addons/l10n_do/__init__.py`
- `addons/l10n_do/__manifest__.py`
- `addons/l10n_do/data/account_account_tag_data.xml`
- `addons/l10n_do/data/account_tax_report_data.xml`
- `addons/l10n_do/data/l10n_latam_document_type_data.xml`
- `addons/l10n_do/data/template/account.account-do.csv`
- `addons/l10n_do/data/template/account.fiscal.position-do.csv`
- `addons/l10n_do/data/template/account.tax-do.csv`
- `addons/l10n_do/data/template/account.tax.group-do.csv`
- `addons/l10n_do/demo/demo_account_journal.xml`
- `addons/l10n_do/demo/demo_company.xml`
- `addons/l10n_do/demo/demo_res_partner.xml`
- `addons/l10n_do/i18n/es_419.po`
- `addons/l10n_do/i18n/l10n_do.pot`
- `addons/l10n_do/models/__init__.py`
- `addons/l10n_do/models/account_move.py`
- `addons/l10n_do/models/account_tax.py`
- `addons/l10n_do/models/res_partner.py`
- `addons/l10n_do/models/template_do.py`
- `addons/l10n_do/tools/__init__.py`
- `addons/l10n_do/tools/partner_identifiers.py`
- `addons/l10n_do/views/account_move_views.xml`
- `addons/l10n_do/views/account_tax_views.xml`
