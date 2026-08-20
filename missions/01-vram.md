# Level 01 — VRAM Tetris

## Briefing
Mosaic owns enough raw GPU compute on paper, but several jobs still cannot run.

## Objective
Reason about accelerator count, VRAM capacity, fragmentation, concurrency, and placement.

## Build
Define a fictional inventory of GPU types with different VRAM capacities. Attempt to place the workload deck under simple rules: one job per GPU, multi-GPU jobs, reserved headroom, and optionally fractional/sharing assumptions where appropriate.

## Constraint change
Increase one model’s memory requirement by 25% and make a previously easy packing invalid.

## Evidence
- placement table
- stranded/unused VRAM calculation
- rejected-job reasons
- alternative packing strategy

## Victory condition
You can explain why total fleet VRAM is not equivalent to usable VRAM for a specific job mix.
