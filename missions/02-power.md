# Level 02 — The Power Ceiling

## Briefing
Your VRAM-perfect layout violates the rack power budget.

## Objective
Add power as a hard placement constraint.

## Tasks
Assign fictional/clearly sourced power assumptions to GPU servers. Calculate per-node and rack totals, headroom, and how many simultaneously busy nodes the power envelope supports.

## Constraint change
Reduce available rack power by 15%. Decide whether to reduce density, cap concurrent work, choose different hardware, or accept lower throughput.

## Evidence
- capacity-vs-power table
- before/after placement
- tradeoff statement

## Victory condition
The model can reject a configuration that fits by GPU count but not by power.
