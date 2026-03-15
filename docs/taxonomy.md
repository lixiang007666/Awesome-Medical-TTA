# Taxonomy for Medical TTA/CTTA

This repository uses a one-paper-one-core-method rule for stable statistics and review writing.

## Core Method Classes

- Entropy/Confidence-Driven
- Self-Training/Pseudo-Label
- Prompt/PEFT Adaptation
- Memory/Continual Stabilization
- Prior-Constrained Adaptation
- Augmentation/Invariance Consistency
- Emerging/Other

## Conflict Resolution Rules

1. Select the core method by the dominant update/optimization mechanism at test time.
2. If ambiguous, follow the paper's core claim in title, abstract, and method.
3. If still ambiguous, apply this tie-breaker priority:
   `Prompt/PEFT > Memory/Continual > Self-Training/Pseudo-Label > Entropy/Confidence > Prior-Constrained > Augmentation/Invariance > Emerging/Other`.

## Class Split Rule (Minimum Viable Maintenance)

- Keep a class independent only when paper count >= 2.
- If count < 2, keep those papers in `Emerging/Other`.
- Promote to an independent class once accumulated count reaches 2.
