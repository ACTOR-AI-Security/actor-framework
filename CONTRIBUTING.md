# Contributing to ACTOR

ACTOR is a public draft for comment. It improves through practitioner feedback, and every comment is read. Thank you for helping.

The comment period for v0.1.0 is open until **December 15, 2026**. Comments received after that date are still welcome and are considered for later versions.

## Who should comment

Anyone who secures, audits, governs, builds, or buys AI: CISOs and security leaders, security architects and engineers, auditors and GRC professionals, privacy and legal teams, MSPs and vCISOs, AI developers, and researchers. You do not need to review the whole framework. Feedback on one function or one control is valuable.

## What helps most

- **Is a control right?** Is it technically achievable today, realistic at its tier, and testable by an auditor?
- **Is something missing?** A real AI risk ACTOR does not address, ideally with an example.
- **Is something wrong for your environment?** How a control works, or fails, for vendor AI, a regulated industry, or a small organization.
- **Is the adoption guidance right?** The ACTOR Essentials list, deployment profiles, and the New or Extends tags.
- **Mappings.** How ACTOR controls align with NIST, ISO/IEC 42001, the CSA AI Controls Matrix, MITRE ATLAS, OWASP, and others. These are a v0.2 priority.

The most useful feedback names the control ID, says what is wrong, proposes new wording, and explains why.

## How to comment

1. Go to the [Issues](../../issues) tab and choose **New issue**.
2. Pick a template:
   - **Control change**: new wording, a tier change, or a new control.
   - **Gap report**: a risk ACTOR does not cover.
   - **General feedback**: anything else, such as structure, clarity, or adoption.
3. Before opening an issue, check whether someone has already raised the same point. If so, add your view to that issue.

For open-ended questions and conversation, use [Discussions](../../discussions). If you do not use GitHub, contact Robert Fernandes on LinkedIn.

## What happens to your feedback

- The maintainer reviews every issue, labels it, and responds.
- Accepted changes appear in the next version, and the [changelog](CHANGELOG.md) records them.
- If a suggestion is not adopted, the issue explains why before it is closed.
- Final decisions on the framework's content rest with the maintainer.

## Requirements for contributors

By opening an issue, posting in Discussions, or otherwise submitting a contribution, you agree that:

- **Same license.** Your contribution is licensed under CC BY 4.0, the same license as the project, so it can be incorporated into ACTOR and shared under that license.
- **Your right to share.** The contribution is your own work, or you have permission to share it.
- **No confidential information.** You will not include confidential or non-public information belonging to your employer, your clients, or anyone else, including internal configurations, incident details, or vendor information shared under NDA. Describe scenarios in general terms.
- **No vulnerabilities.** Do not post details of an unpatched vulnerability in a specific product. Report it to the vendor through its disclosure process.
- **Credit.** Contributors whose suggestions are adopted may be acknowledged in the project. Say in your issue if you prefer not to be named.
- **Conduct.** You follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Writing style for proposed control wording

- One outcome per control, stated as what is true when the control is in place.
- Tool-neutral. Name a mechanism or example only when it clarifies, never a required product or vendor.
- Short declarative sentences in plain practitioner language.
- Testable. An auditor should be able to tell whether it is met, and what evidence would show it.
- Use the defined terms in [FRAMEWORK.md](FRAMEWORK.md#definitions-and-conventions), such as risk rating and action risk level.
- No control may depend on a control at a higher tier.
- No unsourced statistics.

## Control IDs

IDs follow FUNCTION-CATEGORY-NN, such as DEL-ID-01. Published IDs are not renumbered. A retired control keeps its ID and is marked as withdrawn in the changelog.

## Pull requests

Issues are the preferred way to propose changes during the comment period. If you open a pull request, keep it to one change, and update FRAMEWORK.md and both files in controls/ so they stay consistent.
