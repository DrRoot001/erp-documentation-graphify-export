# Security Requirements

1. Enforce route authentication metadata and transport protections.
2. Enforce model access for each operation before persistence.
3. Apply record rules with company/tenant context.
4. Preserve least privilege and group inheritance semantics.
5. Do not expose secrets in logs or documentation.
6. Log security-relevant failures and administrative changes according to deployment policy.
7. Test both allowed and denied paths using the 587 source security-test artifacts as a coverage baseline.
8. Treat unverified runtime behavior as `UNKNOWN` until exercised in a configured environment.

Items 1–3 are directly supported by route, ACL, and record-rule evidence; items 4–8 combine evidence with clone safety requirements and are labeled `INFERRED`/`ASSUMPTION` where not directly declared.
