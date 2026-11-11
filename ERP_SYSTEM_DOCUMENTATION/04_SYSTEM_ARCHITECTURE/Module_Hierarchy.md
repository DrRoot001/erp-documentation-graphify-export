# Module Hierarchy

The repository contains 666 manifest-backed modules. The complete hierarchy is represented by the module catalog and dependency declarations; the following diagram shows the verified structural relationship:

```mermaid
flowchart TD
  ERP[ERP SYSTEM]
  CORE[Core server and base addons]
  APPS[Business and web addons]
  INT[Integration and localization addons]
  TEST[Test and support addons]
  ERP --> CORE
  ERP --> APPS
  ERP --> INT
  ERP --> TEST
  CORE --> GRAPH[Manifest dependency graph]
  APPS --> GRAPH
  INT --> GRAPH
  TEST --> GRAPH
```

Use `03_MODULE_DOCUMENTATION/Module_Catalog.md` and each linked addon page for the exhaustive module list.

