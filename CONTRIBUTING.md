# Contributing to ACTOR

ACTOR improves through practitioner feedback. Thank you for helping.

## Ways to contribute

- **Suggest a control change.** Open an issue using the "Control change" template. Include the control ID, the proposed wording, and why.
- **Report a gap.** Open an issue describing the risk ACTOR does not cover, with a real-world example if you can.
- **Propose a mapping.** Mappings to other frameworks (NIST, ISO/IEC 42001, CSA AICM, MITRE ATLAS, and others) are a v0.2 priority.
- **Share implementation experience.** Pilot results and evidence examples are especially valuable.

## Writing style for control statements

- One outcome per control, stated as what is true when the control is in place.
- Tool-neutral. Name a mechanism or example only when it clarifies, never a required product.
- Short declarative sentences. Plain practitioner language.
- No unsourced statistics.

## Control IDs

IDs follow FUNCTION-CATEGORY-NN, such as DEL-ID-01. Published IDs are not renumbered. A retired control keeps its ID and is marked as withdrawn in the changelog.

## Pull requests

The source of truth for controls is the control data. Use the defined terms in FRAMEWORK.md, such as risk rating and action risk level. No control may depend on a control at a higher tier. If you change a control, update FRAMEWORK.md and both files in controls/ so they stay consistent.

## Review terms

This is a confidential review draft. Please do not share it, quote it, or publish it without the author's permission.

## Terms for feedback and contributions

By sharing feedback, suggestions, or contributions with the author, you agree that:

- You have the right to share them, and they are your own work or you have permission to share them.
- You grant Robert Fernandes a perpetual, worldwide, royalty-free, irrevocable license to use, modify, and publish them as part of ACTOR, including under CC BY 4.0 or any later license for the project.
- You will not include confidential information belonging to your employer, your clients, or anyone else.
- Contributions are acknowledged in the project unless you ask not to be named.
