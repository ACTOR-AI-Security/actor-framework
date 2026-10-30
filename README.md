# ACTOR

**AI Controls for Trust, Oversight, and Resilience**

ACTOR is an open, tool-neutral security control framework for the full AI estate: agents, models, the data they learn from and read, AI platforms, and how people use AI.

Its premise is simple. AI is a new class of actor. An agent acts like a user but is not a person. A model runs like software but is not deterministic. Both can be manipulated by what they read, agents can act beyond their instructions, and both change over time. Existing frameworks secure people and conventional systems, and they remain essential. ACTOR adds the controls AI needs alongside them, and governs the people who use, build, and oversee it.

> **Status: v0.1.1 public draft for comment.** The comment period is open until **January 15, 2027**. Feedback received by then will shape v0.2. See [How to comment](#how-to-comment).

### [Read the full framework](FRAMEWORK.md)

[Control spreadsheet (CSV)](controls/actor-controls.csv) | [Control data (JSON)](controls/actor-controls.json) | [How to comment](#how-to-comment)

## What makes ACTOR different

- **Agents are security principals.** Every agent is identifiable as itself, with delegated authority and a human owner. Agents never sign in with a person's credentials.
- **Humans hold authority, agents hold capability.** High-impact actions need a human approval the agent cannot satisfy, up to hardware-bound approval for critical actions.
- **Assume manipulation and misbehavior.** Controls limit what a manipulated or misbehaving AI can do, not only whether it happens.
- **A loop, not a checklist.** A new tool, a model update, drift, or an incident sends a system back through the cycle.
- **An overlay, not a new program.** Most controls extend practices you already run, such as vendor risk, incident response, and identity management.
- **Works for vendor AI too.** Controls say how to meet them when a vendor runs the AI, through admin settings or vendor assurance, not only when you build it yourself.
- **Tiered and testable.** Foundational, Managed, and Advanced tiers let any organization start where it is, and every control is written so an auditor can test it.

## At a glance

125 controls across seven functions: 50 Foundational, 64 Managed, 11 Advanced.

| Function | Code | Controls |
| --- | --- | --- |
| Govern | GVN | 22 |
| Inventory | INV | 9 |
| Delegate | DEL | 19 |
| Harden | HRD | 28 |
| Defend | DEF | 18 |
| Monitor | MTR | 17 |
| Respond | RSP | 12 |

## Where to start

1. **Pick your deployment profile.** Consumed (you use vendor AI as delivered), Configured (you also build agents or assistants on vendor platforms), or Built (you also develop or host your own AI). Controls outside your profile do not apply.
2. **Start with the 18 ACTOR Essentials.** They address the most common real AI failures for organizations that mainly use vendor AI.
3. **Work through your tier.** Controls marked Extends add AI scope to something you already do. Controls marked New are AI-specific work.

See [Adopting ACTOR](FRAMEWORK.md#adopting-actor-alongside-your-existing-program) for the Essentials list, profile counts, and the practices each control extends. The [control spreadsheet](controls/actor-controls.csv) can be filtered by profile, tier, and Essentials.

## How to comment

This is a draft, and practitioner feedback is the point of publishing it. Every comment is read.

- **Specific feedback on a control:** open an issue with the [Control change](../../issues/new/choose) template.
- **A risk ACTOR misses:** open an issue with the [Gap report](../../issues/new/choose) template.
- **Anything else:** open a General feedback issue, or start a conversation in [Discussions](../../discussions).
- **No GitHub account?** Contact Robert Fernandes on LinkedIn.

Read [CONTRIBUTING.md](CONTRIBUTING.md) before commenting. It explains what makes feedback most useful and the terms that apply.

## Repository contents

| Path | What it is |
| --- | --- |
| [FRAMEWORK.md](FRAMEWORK.md) | The full framework: thesis, principles, definitions, all controls, tiers, adoption guidance, and mappings |
| [controls/actor-controls.csv](controls/actor-controls.csv) | Every control as a spreadsheet, ready for GRC tools |
| [controls/actor-controls.json](controls/actor-controls.json) | Every control as structured JSON |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to comment and contribute |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Expected behavior in this project |
| [ROADMAP.md](ROADMAP.md) | What is planned for v0.2 and beyond |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [TRADEMARK.md](TRADEMARK.md) | Use of the ACTOR name |
| [LICENSE](LICENSE) | CC BY 4.0 license |

## Citing ACTOR

Cite controls with the framework name before the ID, for example **ACTOR DEL-ID-01**. See [CITATION.cff](CITATION.cff) for a formal citation.

## License

The ACTOR framework text and control data are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). You may use, share, and adapt them, including commercially, as long as you give credit.

Suggested attribution: "ACTOR Framework by Robert Fernandes, licensed under CC BY 4.0."

The ACTOR name identifies the official framework. See [TRADEMARK.md](TRADEMARK.md).

Created by Robert Fernandes.
