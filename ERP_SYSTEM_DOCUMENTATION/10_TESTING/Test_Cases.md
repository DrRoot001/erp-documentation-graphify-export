# Test Cases — Phase 10

## Evidence-linked cases

`Evidence_Test_Cases.csv` contains one machine-readable, non-executed evidence case for each of the **3,470** discovered test files. Each case points to the source artifact and preserves the distinction between an implemented test artifact and an executed result.

| Field | Meaning |
|---|---|
| Test Case ID | Stable evidence identifier (`TC-EVID-nnnn`) |
| Source Test File | Repository path to the test artifact |
| Module | Nearest manifest-owning module, or `core` |
| Layer | Backend/model, HTTP/integration, or Browser/static |
| Objective Evidence | Execution objective derived from the source artifact |
| Actual Result | Blank until execution |
| Status | `Not Executed` for this phase |

## QA execution requirements

Before marking a case passed, record the exact command, database configuration, selected modules, browser/runtime version, fixture data, external-service mocks, and failure output where applicable.
