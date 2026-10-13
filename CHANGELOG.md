# Changelog

## v0.1.0 (2026-10-13)

Initial draft for private review.

After an internal review from CISO, compliance, and audit perspectives:

- Added definitions, organization-defined value, lettered requirement, not-applicable, and conformance conventions.
- Clarified scope: fairness, consumer protection, AI disclosure, attacker AI, and model risk management are out of scope. ACTOR alone does not demonstrate legal compliance.
- Added Data as an Applies to value.
- Split basic agent logging (MTR-LG-01) from trace ID linkage (new MTR-LG-04), and pre-release testing (MTR-TS-02) from independent red teaming (new MTR-TS-03).
- Moved GVN-CO-02, DEL-DG-02, DEL-LA-02, DEL-AP-04, HRD-DP-02, and DEF-OU-01 to Foundational. Moved MTR-TS-02 to Managed.
- Rewrote DEL-AP-02 so approval binding is enforced on the server side, and DEL-AP-04 to follow applicable law on consequential decisions.
- Strengthened third-party contract terms, retention and legal hold, notification, and board reporting.

After a second review for auditability and technical feasibility:

- Rewrote controls so each has a testable requirement and producible evidence, and so organizations that only use vendor AI services can meet them.
- Added conventions for implementation mode (Operated, Configured, Assured), platform limits, existing systems and contracts, absolute requirements, review records, and in-place versus operating tier claims.
- Added definitions for vendor assistants, configured agents, built AI systems, session agents, trust boundary, human approval and review, and qualified person.
- Split exceptions (GVN-RK-03, now Foundational) from risk appetite (new GVN-RK-04), and session agent limits (DEL-ID-03, now Foundational) from session agent isolation (new DEL-ID-04).
- New controls: holding new vendor AI features for review (HRD-CF-05), managed configuration of endpoint AI agents (HRD-CF-06), tenant restrictions on approved AI services (HRD-DP-07), protection of derived AI data such as embeddings and memory (HRD-DP-08), and security of MCP and tool servers the organization exposes (HRD-DV-05).
- Moved GVN-CO-03 and DEF-OU-03 to Foundational, MTR-DR-03 to Managed, and MTR-LG-04 to Advanced.

Before review, overlapping controls were consolidated so each requirement appears once and can be assessed once. Merges: pre-deployment review and risk assessment (GVN-RK-02), action risk levels and approval thresholds (DEL-AP-01), single-action approvals and approval fatigue (DEL-AP-03), platform identity and administrator access (HRD-CF-02), model integrity and safe loading (HRD-SC-04), data intake and quarantine (HRD-PV-03), dataset versioning and lineage (HRD-PV-04), contributor control and change logging (DEF-PS-01), evaluation after updates (MTR-DR-02), pre-release and ongoing adversarial testing (MTR-TS-02, later split into MTR-TS-02 and MTR-TS-03), containment runbooks (RSP-CN-01), and backup, rollback, and restore (RSP-CN-02).

- Seven functions: Govern, Inventory, Delegate, Harden, Defend, Monitor, Respond.
- 119 controls: 48 Foundational, 60 Managed, 11 Advanced.
- Function-level mapping to NIST CSF 2.0, NIST AI RMF, and the OWASP LLM Top 10 (2025).
- Machine-readable control data in CSV and JSON.
