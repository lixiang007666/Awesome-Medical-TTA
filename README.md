# Awesome-Medical-TTA

A structured repository for medical image Test-Time Adaptation (TTA/CTTA) papers.

## Quick List (Preview)

This section only shows part of the list as preview.
Full tables are maintained in:
- `docs/papers/tta.md`
- `docs/papers/ctta.md`

| Year | Paper | Track | Venue | Core Method | Secondary Method | Task | Link | Code | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2021 | Tent: Fully Test-time Adaptation by Entropy Minimization | TTA | ICLR | Entropy/Confidence-Driven | N/A | Classification | [arXiv](https://arxiv.org/abs/2006.10726) | [GitHub](https://github.com/DequanWang/tent) | Canonical entropy minimization baseline |
| 2021 | T3A: Test-Time Classifier Adjustment Module for Model-Agnostic Domain Generalization | TTA | NeurIPS | Entropy/Confidence-Driven | Memory/Continual Stabilization | Classification | [OpenReview](https://openreview.net/forum?id=e_yvNqkJKAW) | [GitHub](https://github.com/matsuolab/T3A) | Classifier adjustment at test time |
| 2022 | DLTTA: Dynamic Learning Rate for Test-time Adaptation on Cross-domain Medical Images | TTA | IEEE TMI | Entropy/Confidence-Driven | N/A | Segmentation | [arXiv](https://arxiv.org/abs/2205.13723) | [GitHub](https://github.com/med-air/DLTTA) | Medical-focused dynamic adaptation |
| 2025 | PASS: Test-Time Prompting to Adapt Styles and Semantic Shapes in Medical Image Segmentation | TTA | IEEE TMI | Prompt/PEFT Adaptation | Prior-Constrained Adaptation | Segmentation | [arXiv](https://arxiv.org/abs/2410.01573) | [GitHub](https://github.com/EndoluminalSurgicalVision-IMR/PASS.git) | Prompt-based segmentation adaptation |
| 2022 | Continual Test-Time Domain Adaptation (CoTTA) | CTTA | CVPR | Memory/Continual Stabilization | Augmentation/Invariance Consistency | Classification | [PDF](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Continual_Test-Time_Domain_Adaptation_CVPR_2022_paper.pdf) | [GitHub](https://github.com/qinenergy/cotta) | Representative CTTA baseline |
| 2024 | Each Test Image Deserves A Specific Prompt: Continual Test-Time Adaptation for 2D Medical Image Segmentation | CTTA | CVPR | Prompt/PEFT Adaptation | Memory/Continual Stabilization | Segmentation | [arXiv](https://arxiv.org/pdf/2311.18363) | [GitHub](https://github.com/Chen-Ziyang/VPTTA) | CTTA with test-image prompt |

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
│   ├── README.md
│   ├── tta.bib
│   └── ctta.bib
└── assets/
    └── README.md
```

## Classification Rules (Summary)

- Each paper must have exactly one `Core Method`.
- Each paper can have zero or one `Secondary Method` (`N/A` if not needed).
- Use one consistent method label per paper across the repository.
- Use venue publication year as `Year` whenever available (journal/conference year first).

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
- If useful, record one additional strategy as `Secondary Method`; otherwise use `N/A`.


## Contribution Template

Please add papers in [`notes/paper_template.md`](notes/paper_template.md), then register them in `docs/papers/tta.md` or `docs/papers/ctta.md` with:

`Year | Paper | Venue | Core Method | Secondary Method | Task | Link | Code | Notes`

## How to Maintain

Add paper note -> assign one `Core Method` -> optionally assign one `Secondary Method` -> add one row to `docs/papers/tta.md` or `docs/papers/ctta.md`.

## Current Paper Lists

- TTA papers: [`docs/papers/tta.md`](docs/papers/tta.md)
- CTTA papers: [`docs/papers/ctta.md`](docs/papers/ctta.md)
