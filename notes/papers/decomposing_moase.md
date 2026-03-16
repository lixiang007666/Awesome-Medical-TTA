# Decomposing the Neurons - Paper Card

## Basic Info
- Year: 2024
- Venue: arXiv (preprint)
- Task: Primarily Classification (also reports segmentation settings)
- Modality: Cross-domain benchmarks (classification-focused)
- Setting: Continual Test-Time Adaptation (CTTA)
- Link: https://arxiv.org/abs/2405.16486
- Code: https://github.com/RoyZry98/MoASE-Pytorch

## Problem
- In Continual Test-Time Adaptation (CTTA), the model is continuously updated on non-stationary target streams.
- Domain-wise updates can interfere with each other, causing catastrophic forgetting.
- Existing stabilization strategies (memory, entropy, pseudo-label) still struggle with cross-domain feature conflict.

## Main Idea
- The paper proposes MoASE (Mixture of Activation Sparsity Experts), which decomposes adaptation into multiple expert subnetworks.
- A router dynamically selects experts for each target sample to realize domain-aware processing.
- Activation sparsity is introduced so only a subset of neurons is active per inference/update.
- Gating and stabilization objectives are used to keep continual adaptation stable.
- By separating domain-specific adaptation routes, MoASE reduces cross-domain interference and forgetting.

## Method Classification
- Core Method: Mixture-of-Experts Adaptation
- Secondary Method: Activation Sparsity

## Adaptation Properties
- Setting: Continual Test-Time Adaptation
- Supervision Signal: Entropy-based self-supervised signal (paper-reported)
- Adaptation Object: Expert routing/gating and sparse neuron activation patterns

## Data & Experiment
- Dataset: ImageNet-C/domain-shift benchmarks + segmentation settings (verify exact benchmark names from paper)
- Backbone: CNN/ResNet-style backbones
- Metric: Top-1 accuracy and segmentation metrics
- Cost: Additional expert routing and gating computation
- Memory Requirement: Multiple expert branches and routing states

## Strengths
1. Mitigates cross-domain interference at architectural level via expert decomposition.
2. Activation sparsity improves selective adaptation and reduces destructive updates.
3. Shows stronger continual robustness under non-stationary domain shift.

## Weaknesses
1. MoE structure increases model complexity and inference overhead.
2. Router/gating introduces extra hyperparameters and tuning burden.
3. Gains may shrink when domain differences are small.

## Repro Notes
- Number of experts is a key hyperparameter.
- Router is typically implemented as linear projection with softmax gating.
- Activation sparsity ratio and gating threshold are sensitive knobs.
- Sensitivity under non-stationary stream order should be checked in ablation.
