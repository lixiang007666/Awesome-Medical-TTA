# Awesome-Medical-TTA

A structured repository for medical image Test-Time Adaptation (TTA/CTTA) papers.

## Current Papers (All)

This section shows all currently collected papers.
Detailed tables are also maintained in:
- `docs/papers/tta.md`
- `docs/papers/ctta.md`

| Year | Paper | Track | Core Method | Secondary Method | Link |
| --- | --- | --- | --- | --- | --- |
| 2021 | Tent: Fully Test-time Adaptation by Entropy Minimization | TTA | Entropy/Confidence-Driven | N/A | [arXiv](https://arxiv.org/abs/2006.10726) |
| 2021 | T3A: Test-Time Classifier Adjustment Module for Model-Agnostic Domain Generalization | TTA | Entropy/Confidence-Driven | Memory/Continual Stabilization | [OpenReview](https://openreview.net/forum?id=e_yvNqkJKAW) |
| 2022 | DLTTA: Dynamic Learning Rate for Test-time Adaptation on Cross-domain Medical Images | TTA | Entropy/Confidence-Driven | N/A | [arXiv](https://arxiv.org/abs/2205.13723) |
| 2025 | A3-TTA: Adaptive Anchor Alignment Test-Time Adaptation for Image Segmentation | TTA | Prior-Constrained Adaptation | Entropy/Confidence-Driven | [arXiv](https://arxiv.org/abs/2602.03292) |
| 2025 | PASS: Test-Time Prompting to Adapt Styles and Semantic Shapes in Medical Image Segmentation | TTA | Prompt/PEFT Adaptation | Prior-Constrained Adaptation | [arXiv](https://arxiv.org/abs/2410.01573) |
| 2025 | Free on the Fly: Enhancing Flexibility in Test-Time Adaptation with Online EM | TTA | Memory/Continual Stabilization | Entropy/Confidence-Driven | [arXiv](https://arxiv.org/abs/2507.06973) |
| 2025 | CertainTTA: Estimating Uncertainty for Test-Time Adaptation on Medical Image Segmentation | TTA | Emerging/Other | Entropy/Confidence-Driven | [DOI](https://doi.org/10.1016/j.inffus.2025.103300) |
| 2022 | Continual Test-Time Domain Adaptation (CoTTA) | CTTA | Memory/Continual Stabilization | Augmentation/Invariance Consistency | [PDF](https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Continual_Test-Time_Domain_Adaptation_CVPR_2022_paper.pdf) |
| 2024 | Each Test Image Deserves A Specific Prompt: Continual Test-Time Adaptation for 2D Medical Image Segmentation | CTTA | Prompt/PEFT Adaptation | Memory/Continual Stabilization | [arXiv](https://arxiv.org/pdf/2311.18363) |
| 2025 | TopoTTA: Topology-Enhanced Test-Time Adaptation for Tubular Structure Segmentation | CTTA | Prior-Constrained Adaptation | Memory/Continual Stabilization | [arXiv](https://arxiv.org/pdf/2508.00442) |
| 2026 | SicTTA: Single Image Continual Test Time Adaptation for Medical Image Segmentation | CTTA | Memory/Continual Stabilization | Entropy/Confidence-Driven | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S1361841525004050) |
| 2025 | SAM-aware Test-time Adaptation for Universal Medical Image Segmentation | CTTA | Prior-Constrained Adaptation | Prompt/PEFT Adaptation | [arXiv](https://arxiv.org/pdf/2506.05221) |
| 2025 | Domain Consistency Learning for Continual Test-Time Adaptation in Image Semantic Segmentation | CTTA | Augmentation/Invariance Consistency | Memory/Continual Stabilization | [DOI](https://doi.org/10.1016/j.patcog.2025.111585) |

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
