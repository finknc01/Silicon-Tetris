# Level 04 — Checkpoint Tax

## Briefing
Compute and network fit. Shared storage cannot absorb simultaneous dataset reads and checkpoints.

## Objective
Add storage throughput/IOPS/checkpoint demand to the resource puzzle.

## Tasks
Estimate read and checkpoint write demand for each workload card. Model a shared storage ceiling and optional local-cache tier. Calculate what happens when checkpoint windows overlap.

## Constraint change
Force three training jobs to checkpoint in the same five-minute window. Propose staggered scheduling, local staging, or storage expansion and quantify the effect with your assumptions.

## Evidence
- storage demand timeline
- peak vs average demand
- mitigation comparison

## Victory condition
The plan recognizes storage as a schedulable/capacity dependency rather than an infinite background service.
