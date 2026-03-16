# TopoTTA - Paper Card

## Basic Info
- Year: 2025
- Venue: ICCV 2025
- Task: Tubular Structure Segmentation
- Modality: Medical images (vessel-like tubular structures)
- Setting: Continual Test-Time Adaptation (CTTA)
- Link: https://arxiv.org/pdf/2508.00442
- Code: N/A

## Method Classification
- Core Method: Topology / Structure-Driven Adaptation
- Secondary Method: Pseudo-label Alignment

## Problem
- Under domain shift, tubular structure segmentation often suffers from topology breakage (disconnections or wrong connections).
- Many TTA/CTTA methods optimize pixel-wise objectives but do not explicitly preserve structural continuity.
- TopoTTA targets structure-consistent adaptation so predictions remain topologically plausible across target-domain stream shift.

## Main Idea
- TopoTTA injects topology-aware constraints into test-time adaptation for tubular structures.
- A topology-enhanced module improves structural feature sensitivity, and hard topology samples are emphasized during adaptation.
- Pseudo-label alignment is used to gradually correct structural errors and adapt to target-domain appearance changes.
- The overall effect is better topological continuity while adapting on target data.

## Adaptation Properties
- Setting: Continual Test-Time Adaptation
- Supervision Signal: Topology-guided pseudo labels
- Adaptation Object: Feature representation with topology-aware constraints

## Strengths
1. Explicitly models topology, which is critical for vessel/tubular segmentation.
2. Reduces structure breakage compared with purely pixel-driven adaptation.
3. Does not rely on a dedicated memory bank.

## Weaknesses
1. Method design is task-specific and may transfer less effectively beyond tubular segmentation.
2. Topology-aware objectives add extra test-time computation.
3. Still depends on pseudo-label quality under severe domain shift.

## Repro Notes
- Verify exact benchmark names and backbone settings from the paper.
- Topology-hard sample generation is a key component to reproduce reported gains.
- Pseudo-label quality control is important for stability.
- Test-time cost should include both topology processing and pseudo-label refinement overhead.
