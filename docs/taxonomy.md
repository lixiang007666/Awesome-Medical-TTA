# Taxonomy for Medical TTA/CTTA

This repository uses a one-paper-one-core-method rule with an optional secondary method.

## Core Method Classes

- Entropy/Confidence-Driven
- Self-Training/Pseudo-Label
- Prompt/PEFT Adaptation
- Memory/Continual Stabilization
- Prior-Constrained Adaptation
- Augmentation/Invariance Consistency
- Emerging/Other

## Secondary Method Rule

- `Secondary Method` is optional and can contain at most one label.
- Prefer using paper-native method terms (e.g., `Feature Alignment`, `Prototype Matching`) or set to `N/A`.
- `Secondary Method` must not duplicate `Core Method`.
- If `Secondary Method` is used, add a short reason in `Notes` (one sentence).

## Conflict Resolution Rules

1. Select the core method by the dominant update/optimization mechanism at test time.
2. If ambiguous, follow the paper's core claim in title, abstract, and method.
3. Optionally add one `Secondary Method` for the most important auxiliary strategy; otherwise use `N/A`.
