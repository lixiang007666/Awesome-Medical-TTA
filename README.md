# Awesome-Medical-TTA

A structured repository for medical image Test-Time Adaptation (TTA/CTTA) papers.

## Quick List (Preview)

This is a short homepage preview. The full tables are maintained in `docs/papers/`.

| Year | Paper | Track | Core Method | Link |
| --- | --- | --- | --- | --- |
| 2021 | Tent: Fully Test-time Adaptation by Entropy Minimization | TTA | Entropy/Confidence-Driven | [arXiv](https://arxiv.org/abs/2006.10726) |
| 2021 | T3A: Test-Time Classifier Adjustment Module for Model-Agnostic Domain Generalization | TTA | Entropy/Confidence-Driven | [OpenReview](https://openreview.net/forum?id=e_yvNqkJKAW) |
| 2022 | DLTTA: Dynamic Learning Rate for Test-time Adaptation on Cross-domain Medical Images | TTA | Entropy/Confidence-Driven | [arXiv](https://arxiv.org/abs/2205.13723) |
| 2025 | PASS: Test-Time Prompting to Adapt Styles and Semantic Shapes in Medical Image Segmentation | TTA | Prompt/PEFT Adaptation | [arXiv](https://arxiv.org/abs/2410.01573) |
| 2022 | Continual Test-Time Domain Adaptation (CoTTA) | CTTA | Memory/Continual Stabilization | [PDF](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Continual_Test-Time_Domain_Adaptation_CVPR_2022_paper.pdf) |
| 2024 | Each Test Image Deserves A Specific Prompt: CTTA for 2D Medical Segmentation | CTTA | Prompt/PEFT Adaptation | [arXiv](https://arxiv.org/pdf/2311.18363) |

## Overview

- [`docs/taxonomy.md`](docs/taxonomy.md): Core method taxonomy and classification rules
- [`docs/papers/tta.md`](docs/papers/tta.md): TTA paper table
- [`docs/papers/ctta.md`](docs/papers/ctta.md): CTTA paper table
- [`notes/paper_template.md`](notes/paper_template.md): per-paper note template
- [`bib/README.md`](bib/README.md): bibliography storage conventions
- [`assets/README.md`](assets/README.md): figures/tables asset conventions

## Repository Structure

```text
.
├── README.md
├── docs/
│   ├── taxonomy.md
│   └── papers/
│       ├── tta.md
│       └── ctta.md
├── notes/
│   └── paper_template.md
├── bib/
│   └── README.md
└── assets/
    └── README.md
```

## Classification Rules (Summary)

- Each paper must have exactly one `Core Method`.
- Use one consistent method label per paper across the repository.

## Core Method Classes (Shared by TTA and CTTA)

1. Entropy/Confidence-Driven
2. Self-Training/Pseudo-Label
3. Prompt/PEFT Adaptation
4. Memory/Continual Stabilization
5. Prior-Constrained Adaptation
6. Augmentation/Invariance Consistency
7. Emerging/Other

## Conflict Resolution (How to Choose Core Method)

- Pick the method that best represents the paper's main contribution.
- If multiple strategies are used, choose the one that drives the core test-time update.


## Contribution Template

Please add papers in [`notes/paper_template.md`](notes/paper_template.md), then register them in `docs/papers/tta.md` or `docs/papers/ctta.md` with:

`Year | Paper | Venue | Core Method | Task | Link | Code | Notes`

## How to Maintain

Add paper note -> assign one `Core Method` -> add one row to `docs/papers/tta.md` or `docs/papers/ctta.md`.

## Current Paper Lists

- TTA papers: [`docs/papers/tta.md`](docs/papers/tta.md)
- CTTA papers: [`docs/papers/ctta.md`](docs/papers/ctta.md)
