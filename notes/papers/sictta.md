# SicTTA - Paper Card

## Basic Info

- Year: 2026
- Venue: Medical Image Analysis (MedIA)
- Task: Segmentation
- Modality: Medical image segmentation benchmarks in the paper (multi-center setting)
- Setting: Single-image Continual Test-Time Adaptation
- Link: https://www.sciencedirect.com/science/article/pii/S1361841525004050
- Code: https://github.com/HiLab-git/SicTTA

## Problem

- Many TTA methods depend on batch statistics or pseudo-labels, which are unstable when only one test image is available.
- In medical deployment, continual domain shift across scanners/sites can accumulate adaptation errors over time.
- SicTTA targets robust single-image CTTA without relying on pseudo-label supervision.

## Main Idea

- SicTTA identifies source-friendly target (SFT) samples with relatively reliable predictions and stores them in a memory pool.
- It uses a compact density criterion to score reliability and update the SFT pool.
- For each incoming test image, it retrieves similar SFT samples and performs similarity-driven feature fusion.
- This memory-guided fusion stabilizes adaptation and reduces drift in continual single-image inference.

## Method Classification

- Core Method: Memory / Continual Stabilization
- Secondary Method: Feature Alignment (similarity-driven feature fusion)
- Supervision Signal: Memory-based reliable sample retrieval
- Adaptation Object: Feature representation and normalization-related adaptation behavior

## Data & Experiment

- Dataset: Cross-domain medical segmentation benchmarks used in paper
- Backbone: U-Net style segmentation backbones
- Metric: Dice score
- Cost: Extra similarity retrieval and feature fusion at test time
- Memory Requirement: Dynamic SFT feature/sample pool (FIFO-style maintenance)

## Strengths

1. Matches realistic single-image test-time setting where batch statistics are unavailable.
2. Reduces dependence on pseudo-labels and improves continual stability.
3. Uses reliable historical samples to mitigate error accumulation.

## Weaknesses

1. Sensitive to SFT sample quality; noisy memory can degrade adaptation.
2. Requires memory pool and retrieval, increasing compute/memory overhead.
3. May weaken when target stream has very few reliable samples under extreme shifts.

## Repro Notes

- Memory pool size strongly affects stability/performance.
- Similarity retrieval is based on feature embedding similarity.
- FIFO maintenance keeps the SFT pool adaptive over stream progression.
- Validate stream order sensitivity in ablations.
