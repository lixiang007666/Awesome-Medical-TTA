# Awesome-Medical-TTA

A structured repository for medical image Test-Time Adaptation (TTA/CTTA) papers.

## Overview

- [`docs/taxonomy.md`](docs/taxonomy.md): Primary/Secondary classification rules
- [`docs/papers/tta.md`](docs/papers/tta.md): TTA paper table
- [`docs/papers/ctta.md`](docs/papers/ctta.md): CTTA paper table
- [`notes/paper_template.md`](notes/paper_template.md): per-paper note template
- [`bib/README.md`](bib/README.md): bibliography storage conventions
- [`assets/README.md`](assets/README.md): figures/tables asset conventions

## Classification Rules (Summary)

- Each paper must have exactly one `Primary Class`.
- Additional method attributes go into `Secondary Tags`.
- A class is kept independent only when paper count >= 2.
- Otherwise, place papers in `Emerging/Other` temporarily and split later.

## Primary Classes (Shared by TTA and CTTA)

1. Entropy/Confidence-Driven
2. Self-Training/Pseudo-Label
3. Prompt/PEFT Adaptation
4. Memory/Continual Stabilization
5. Prior-Constrained Adaptation
6. Augmentation/Invariance Consistency
7. Emerging/Other

## Conflict Resolution (How to Choose Primary Class)

1. Choose by the core update mechanism (what is actually optimized/updated at test time).
2. If still ambiguous, follow the paper's claimed core contribution (title/abstract/method).
3. If still tied, use this priority:
   `Prompt/PEFT > Memory/Continual > Self-Training/Pseudo-Label > Entropy/Confidence > Prior-Constrained > Augmentation/Invariance > Emerging/Other`.

## Contribution Template

Please add papers in [`notes/paper_template.md`](notes/paper_template.md), then register them in `docs/papers/tta.md` or `docs/papers/ctta.md` with:

`Year | Paper | Venue | Primary Class | Secondary Tags | Setting | Modality | Task | Dataset/Benchmark | Link | Code | Notes`

## Current Paper Lists

- TTA papers: [`docs/papers/tta.md`](docs/papers/tta.md)
- CTTA papers: [`docs/papers/ctta.md`](docs/papers/ctta.md)
