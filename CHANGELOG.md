# Changelog

## v0.1.2 (2026-11-04)

A maintenance release during the comment period. No control IDs changed and no controls were removed, so references to earlier IDs remain valid. Changes align the Delegate function with the ten design tenets for agent identity, authentication, and authorization that NIST published in October 2026, and with public comments on those tenets. They also close gaps in how ACTOR protects data that AI systems log, store, and learn from.

- New DEL-ID-05 (Advanced): in agents the organization builds or hosts, agent identity is bound to the workload and its approved configuration through workload attestation or an equivalent mechanism.
- New DEL-DG-05 (Advanced): signed task mandates state the intended outcome, permitted actions, limits, and expiry. They are passed downstream and checked before high and critical actions.
- New DEL-LA-05 (Managed): no standing write or high-impact permissions while agents are idle, task-scoped grants that expire, and separation of duties for agent permissions.
- New DEF-TL-07 (Managed): agent access and approval decisions are made by deterministic mechanisms. Model or classifier output can inform a decision but cannot grant access or allow an action on its own.
- DEL-AP-01 now requires action risk levels to account for reversibility. Actions that cannot be reversed are at least high.
- DEF-TL-03 now checks the agent's current authority, so a revoked credential, halted agent, or expired task scope blocks the next action, and current risk signals can require approval or block.
- MTR-LG-05 is now lettered. It adds append-only or tamper-evident logs for high-risk agents, and requires the approval record or mandate to be kept with each high and critical action, along with halts, revocations, and actions attempted after revocation.
- New HRD-DP-09 (Managed): people who label training data or review AI inputs and outputs see only the data their task needs, in a controlled environment, with logged access.
- New HRD-DP-10 (Managed): AI systems give the model only the data the task needs. Retrieval results and tool output are limited, and whole mailboxes, folders, or tables are not placed in context by default.
- New HRD-PV-05 (Managed): synthetic, anonymized, and de-identified training data is tested before use to confirm it does not reproduce source records or identify real people.
- New HRD-MP-02 (Advanced): models trained or fine-tuned on sensitive data are tested before release for whether they reproduce training records or reveal what was in their training data.
- New MTR-LG-06 (Managed): sensitive data is removed or masked before it reaches observability, analytics, or debugging tools, and debug captures and traces are deleted on a set schedule.
- HRD-CF-04 now covers the data stores behind AI systems: vector databases, caches, message queues, and storage for training data and model files.
- HRD-DP-06 and DEF-OU-02 now check text inside files, images, and audio, where the tool can extract it.
- New MTR-BH-04 (Managed): decoy credentials, records, or files are placed where AI systems and agents can reach them but have no reason to use them, and any access alerts and is investigated. Prompted by the SANS SEC530 checklist "Zero Trust for AI Agents" (Valenzuela, 2026).
- HRD-DV-02 now also requires agents the organization configures or acquires to be threat modeled against a recognized agentic threat list, such as the OWASP Top 10 for Agentic Applications, before deployment. It applies to the Configured profile as well as Built.
- New definition: task mandate.
- The term session agent is retired. DEL-ID-01, DEL-ID-03, and DEL-ID-04 now name browsing, desktop, and coding agents directly, and the definitions define each. The scope is unchanged: agents that operate inside a person's signed-in browser, desktop, or terminal.
- New informative mapping of the NIST agent identity design tenets to ACTOR controls, in the Standards mapping section.
- New view of ACTOR controls organized by NIST CSF 2.0 category and subcategory, so organizations running a CSF program can place ACTOR controls in their existing profile.
- New six-step procedure in the adoption section for adding ACTOR to an existing control program, using the Extends table, the crosswalk, and the CSF view.
- Control count is 135: 50 Foundational, 71 Managed, 14 Advanced. Profiles: Consumed 94, Configured 110, Built 135.

## v0.1.1 (2026-10-30)

A maintenance release during the comment period. No control IDs changed and no controls were removed, so references to v0.1.0 IDs remain valid. Changes came from an independent practitioner review of the public draft.

- New DEF-OU-04 (Managed): model-generated code, queries, and commands inside applications and pipelines are reviewed by a person or run in a documented, tested sandbox before they touch production. DEF-TL-05 already covered code run by agents.
- New DEF-OU-05 (Managed): input-side screening for customer-facing AI, against the same content policy DEF-OU-03 applies to output.
- HRD-SC-02 now requires that a detected change to a remote MCP server's tool names, descriptions, or parameters blocks the tool until it is re-approved, since a changed description can carry new instructions to the model.
- GVN-RK-01 now states a floor for high risk: health, money, employment, legal rights, and write access to systems of record.
- New "Recommended values" section and a recommended_value column in the control data, giving reference frequencies and thresholds for every organization-defined value. Guidance, not requirements.
- Compound controls DEL-AP-04 and HRD-DV-03 are now lettered into separately testable parts, with the same IDs.
- Overlapping controls now state their scope and cross-reference each other instead of restating a requirement: DEF-TL-01 and DEF-IN-01; RSP-CN-01, RSP-CN-04, and DEF-TL-06; RSP-IV-02 and RSP-CN-02; MTR-DR-01 and HRD-DV-01; MTR-LG-03 and MTR-LG-01; DEL-LA-01 and DEL-DG-02; GVN-PO-01 and HRD-CF-02.
- INV-AS-01 states that reconciliation uses INV-SH-01 discovery results where they exist but does not depend on them. Design principle 9 now says the same in general.
- The Assured implementation mode now says re-confirmation happens at each GVN-TP-03 reassessment, or annually where GVN-TP-03 is not in place.
- The Advanced tier description now includes organizations seeking independent assurance of any AI system, which is why MTR-TS-03 applies to all.
- Control-level crosswalk to NIST CSF 2.0, SP 800-53 Rev 5, NIST AI RMF 1.0, OWASP LLM Top 10 (2025), and OWASP Agentic Top 10 (2026), in FRAMEWORK.md, in controls/actor-crosswalk.csv, and as columns in the control data. Informative, not equivalence.
- Control count is 125: 50 Foundational, 64 Managed, 11 Advanced. Profiles: Consumed 92, Configured 104, Built 125.

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
- 135 controls: 50 Foundational, 71 Managed, 14 Advanced.
- Function-level mapping to NIST CSF 2.0, NIST AI RMF, and the OWASP LLM Top 10 (2025).
- Machine-readable control data in CSV and JSON.
