# Changelog

## v0.1.0 public draft for comment (2026-10-23)

Published for public comment under CC BY 4.0. The comment period is open until January 15, 2027.

Before publication, the draft went through private review and the changes below.

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

Aligned with NIST's key practices for incident readiness and response in highly capable AI agents (October 2026):

- Added agent misbehavior without an attacker to the thesis and to design principle 5.
- RSP-PL-01 now covers actions beyond instructions, near-misses, and severity criteria.
- DEF-TL-06 now stops high-risk agents when monitoring fails.
- RSP-IM-01 now includes other parties an agent affected.
- New controls: restricting agent-created persistence (DEL-LA-04), protecting logs and monitors from agents (MTR-LG-05), and verifying controls before a halted agent resumes (RSP-CN-04).

After publication:

- INV-SH-01 now names models and AI runtimes installed on endpoints, which network monitoring cannot see.
- DEL-ID-02, DEL-LC-01, and DEL-LC-02 now cover AI workload identities, such as service accounts and API keys used by AI pipelines, not only agents. Added a definition of AI workload identity.
- Thanks to an early reviewer for raising non-human identities and locally hosted agents.
- DEL-DG-02 now limits delegated agents to the access their task requires, not the user's full access, and adds a test that the agent cannot reach beyond its task.
- DEL-LA-02 now requires an administrator, not the agent's user or builder, to approve any expansion of an agent's permissions.
- New DEL-AP-05 (Foundational): approvals for critical actions, and high actions the organization designates, require phishing-resistant MFA at the time of approval and are recorded as evidence. DEL-AP-02 now covers only the out-of-band channel and server-side binding.
- HRD-DV-03 now requires qualified review of applications and scripts that people outside a development team build with AI, before they process company data, connect to company systems, or are shared.
- DEL-AP-05 now distinguishes platforms that can require phishing-resistant MFA per approval from those that cannot. Where per-action authentication is unavailable, approvers authenticate with phishing-resistant MFA at platform sign-in with short session lifetimes, and per-action authentication is adopted when supported. This keeps the control achievable on current vendor platforms.
- DEL-AP-01 now states that an approval issued by another agent or automated system is not human approval, and that approvals do not carry over to agents the approved agent invokes.
- DEL-LC-02 now requires that a retired agent's identity be disabled first and deleted after a defined waiting period, so undocumented dependencies surface while the agent can still be restored.

To make adoption proportional:

- Added ACTOR Essentials, a starting set of Foundational controls for organizations that mainly use vendor AI.
- Added deployment profiles (Consumed, Configured, Built) so controls that do not apply drop out without a separate rationale.
- Marked each control as New or Extends, naming the existing practice it extends.
- Added relation, extends, profiles, and essentials fields to the control data.

Before review, overlapping controls were consolidated so each requirement appears once and can be assessed once. Merges: pre-deployment review and risk assessment (GVN-RK-02), action risk levels and approval thresholds (DEL-AP-01), single-action approvals and approval fatigue (DEL-AP-03), platform identity and administrator access (HRD-CF-02), model integrity and safe loading (HRD-SC-04), data intake and quarantine (HRD-PV-03), dataset versioning and lineage (HRD-PV-04), contributor control and change logging (DEF-PS-01), evaluation after updates (MTR-DR-02), pre-release and ongoing adversarial testing (MTR-TS-02, later split into MTR-TS-02 and MTR-TS-03), containment runbooks (RSP-CN-01), and backup, rollback, and restore (RSP-CN-02).

- Seven functions: Govern, Inventory, Delegate, Harden, Defend, Monitor, Respond.
- 123 controls: 50 Foundational, 62 Managed, 11 Advanced.
- Function-level mapping to NIST CSF 2.0, NIST AI RMF, and the OWASP LLM Top 10 (2025).
- Machine-readable control data in CSV and JSON.
