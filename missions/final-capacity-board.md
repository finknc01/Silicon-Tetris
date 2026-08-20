# Final — The Capacity Board

## Briefing
Mosaic’s executives give you a budget, one rack/power envelope, a workload deck, and growth targets. They want one recommendation and the consequences of saying yes.

## Challenge
Feed the scenario into your Python/YAML capacity model or a well-structured spreadsheet/script if the Python tool is not built yet. Produce at least three candidate architectures.

## Required output
- workload demand summary
- GPU/VRAM placement
- power/cooling assumptions
- network bottleneck check
- storage/checkpoint check
- cost/BOM
- headroom and growth triggers
- rejected alternatives
- top three risks

## Twist
After selecting a design, randomly change two constraints and rerun the model rather than manually rewriting the conclusion.

## Victory condition
Silicon-Tetris is complete when requirements become reproducible inputs, constraints become explicit rules, and the recommendation changes predictably when the scenario changes.
