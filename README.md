# Awesome-Medical-TTA

A structured repository for medical image Test-Time Adaptation (TTA/CTTA) papers.

## Quick List (Preview)

This section only shows part of the list as preview.
Full tables are maintained in:
- `docs/papers/tta.md`
- `docs/papers/ctta.md`

<table>
  <thead>
    <tr>
      <th>Year</th>
      <th style="width:42%;">Paper</th>
      <th>Track</th>
      <th>Venue</th>
      <th>Core Method</th>
      <th>Secondary Method</th>
      <th>Task</th>
      <th>Link</th>
      <th>Code</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2021</td>
      <td>Tent: Fully Test-time Adaptation by Entropy Minimization</td>
      <td>TTA</td>
      <td>ICLR</td>
      <td>Entropy/Confidence-Driven</td>
      <td>N/A</td>
      <td>Classification</td>
      <td><a href="https://arxiv.org/abs/2006.10726">arXiv</a></td>
      <td><a href="https://github.com/DequanWang/tent">GitHub</a></td>
      <td>Canonical entropy minimization baseline</td>
    </tr>
    <tr>
      <td>2021</td>
      <td>T3A: Test-Time Classifier Adjustment Module for Model-Agnostic Domain Generalization</td>
      <td>TTA</td>
      <td>NeurIPS</td>
      <td>Entropy/Confidence-Driven</td>
      <td>Memory/Continual Stabilization</td>
      <td>Classification</td>
      <td><a href="https://openreview.net/forum?id=e_yvNqkJKAW">OpenReview</a></td>
      <td><a href="https://github.com/matsuolab/T3A">GitHub</a></td>
      <td>Classifier adjustment at test time</td>
    </tr>
    <tr>
      <td>2022</td>
      <td>DLTTA: Dynamic Learning Rate for Test-time Adaptation on Cross-domain Medical Images</td>
      <td>TTA</td>
      <td>IEEE TMI</td>
      <td>Entropy/Confidence-Driven</td>
      <td>N/A</td>
      <td>Segmentation</td>
      <td><a href="https://arxiv.org/abs/2205.13723">arXiv</a></td>
      <td><a href="https://github.com/med-air/DLTTA">GitHub</a></td>
      <td>Medical-focused dynamic adaptation</td>
    </tr>
    <tr>
      <td>2025</td>
      <td>PASS: Test-Time Prompting to Adapt Styles and Semantic Shapes in Medical Image Segmentation</td>
      <td>TTA</td>
      <td>IEEE TMI</td>
      <td>Prompt/PEFT Adaptation</td>
      <td>Prior-Constrained Adaptation</td>
      <td>Segmentation</td>
      <td><a href="https://arxiv.org/abs/2410.01573">arXiv</a></td>
      <td><a href="https://github.com/EndoluminalSurgicalVision-IMR/PASS.git">GitHub</a></td>
      <td>Prompt-based segmentation adaptation</td>
    </tr>
    <tr>
      <td>2022</td>
      <td>Continual Test-Time Domain Adaptation (CoTTA)</td>
      <td>CTTA</td>
      <td>CVPR</td>
      <td>Memory/Continual Stabilization</td>
      <td>Augmentation/Invariance Consistency</td>
      <td>Classification</td>
      <td><a href="https://openaccess.thecvf.com/content/CVPR2022/papers/Wang_Continual_Test-Time_Domain_Adaptation_CVPR_2022_paper.pdf">PDF</a></td>
      <td><a href="https://github.com/qinenergy/cotta">GitHub</a></td>
      <td>Representative CTTA baseline</td>
    </tr>
    <tr>
      <td>2024</td>
      <td>Each Test Image Deserves A Specific Prompt: Continual Test-Time Adaptation for 2D Medical Image Segmentation</td>
      <td>CTTA</td>
      <td>CVPR</td>
      <td>Prompt/PEFT Adaptation</td>
      <td>Memory/Continual Stabilization</td>
      <td>Segmentation</td>
      <td><a href="https://arxiv.org/pdf/2311.18363">arXiv</a></td>
      <td><a href="https://github.com/Chen-Ziyang/VPTTA">GitHub</a></td>
      <td>CTTA with test-image prompt</td>
    </tr>
  </tbody>
</table>

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
