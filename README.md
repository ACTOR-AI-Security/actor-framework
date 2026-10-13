# ACTOR

**AI Controls for Trust, Oversight, and Resilience**

ACTOR is an open, tool-neutral security control framework for the full AI estate: agents, models, the data they learn from and read, AI platforms, and how people use AI.

Its premise is simple. AI is a new class of actor. An agent acts like a user but is not a person. A model runs like software but is not deterministic. Both can be manipulated by what they read, and both change over time. Existing frameworks secure people and conventional systems, and they remain essential. ACTOR adds the controls AI needs alongside them, and governs the people who use, build, and oversee it.

> **Status:** v0.1.0, draft for public comment. Feedback is welcome through [issues](../../issues).

## What makes ACTOR different

- **Agents are principals.** Every agent gets its own identity, delegated authority, and a human owner. Users do not sign agents in with their own credentials.
- **Humans hold authority, agents hold capability.** High-impact actions need a human approval the agent cannot satisfy, up to hardware-bound approval for critical actions.
- **Assume manipulation.** Controls limit what a manipulated AI can do, not only whether it gets manipulated.
- **A loop, not a checklist.** A new tool, a model update, drift, or an incident sends a system back through the cycle.
- **Tiered.** Foundational, Managed, and Advanced tiers let any organization start where it is.
- **Mapped.** Controls align to NIST CSF 2.0, the NIST AI RMF, and the OWASP LLM Top 10, with more mappings planned.

## At a glance

106 controls across seven functions: 36 Foundational, 54 Managed, 16 Advanced.

| Function | Code | Controls |
| --- | --- | --- |
| Govern | GVN | 18 |
| Inventory | INV | 9 |
| Delegate | DEL | 14 |
| Harden | HRD | 23 |
| Defend | DEF | 18 |
| Monitor | MTR | 12 |
| Respond | RSP | 12 |

## Repository contents

| Path | What it is |
| --- | --- |
| [FRAMEWORK.md](FRAMEWORK.md) | The full framework: thesis, principles, all controls, tiers, and mappings |
| [controls/actor-controls.csv](controls/actor-controls.csv) | Every control as a spreadsheet, ready for GRC tools |
| [controls/actor-controls.json](controls/actor-controls.json) | Every control as structured JSON |
| [ROADMAP.md](ROADMAP.md) | What is planned for v0.2 and beyond |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to suggest changes |
| [CHANGELOG.md](CHANGELOG.md) | Version history |

## Citing ACTOR

Cite controls with the framework name before the ID, for example **ACTOR DEL-ID-01**. See [CITATION.cff](CITATION.cff) for a formal citation.

## License

The ACTOR framework text and control data are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). You may use, adapt, and build on it, including commercially, with attribution.

The ACTOR name is used to identify the official framework. See [TRADEMARK.md](TRADEMARK.md).

Created by Robert Fernandes.
