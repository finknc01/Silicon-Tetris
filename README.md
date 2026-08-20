# Silicon-Tetris

> **The workloads keep coming, the rack has limits, and every “perfect” GPU plan breaks something else. Fit the compute puzzle before memory, power, network, storage, or budget runs out.**

## Project status

| Field | Current state |
|---|---|
| **Status** | **Planned — workload modeling begins early; final planner later in the roadmap** |
| **Current stage** | Campaign authored; no capacity recommendation, cost model, or sizing result is claimed complete |
| **Lab environment** | Laptop-based modeling with explicit workload assumptions and dated/cited hardware specifications |
| **Evidence rule** | Separate measured values, vendor specifications, assumptions, estimates, and simplified models |
| **Last plan sync** | 2026-08-19 |

## Purpose

Silicon-Tetris is a capacity-planning project. Fictional **Mosaic Systems** has training, fine-tuning, batch-inference, and latency-sensitive inference workloads competing for finite GPU memory, compute, rack power, network bandwidth, storage throughput, and money.

The project starts with manual reasoning and evolves toward a small reproducible planner.

> **What should we buy or allocate, which constraint becomes the bottleneck first, and how does the answer change when the assumptions change?**

## Skills developed

- workload characterization and capacity planning
- VRAM/compute/concurrency reasoning
- power/headroom constraints
- network and storage demand modeling
- cost/budget tradeoffs
- growth/sensitivity analysis
- Python/YAML or equivalent reproducible modeling
- explicit assumptions and rejected alternatives

## Capacity campaign

The files in [`missions/`](missions/) are authoritative. Mission 03 network constraints can be deferred if the Weeks 19–20 physical-infrastructure block is already full; it should be completed before the final model.

| Mission | Constraint added | Primary outcome |
|---|---|---|
| [00 — Workload Deck](missions/00-workload-deck.md) | Define the demand before choosing hardware | explicit workload requirements |
| [01 — VRAM](missions/01-vram.md) | Fit workloads to accelerator memory/capacity | placement reasoning |
| [02 — Power](missions/02-power.md) | Add rack/facility power ceilings and headroom | feasible power envelope |
| [03 — Network](missions/03-network.md) | Add communication/fabric constraints | network bottleneck check |
| [04 — Storage](missions/04-storage.md) | Add dataset/checkpoint demand | storage bottleneck check |
| [05 — Budget](missions/05-budget.md) | Constrain cost | cost-aware candidate designs |
| [06 — Priorities](missions/06-priorities.md) | Resolve conflicting workload importance | explicit prioritization rules |
| [07 — Growth](missions/07-growth.md) | Add future demand/headroom | growth triggers and sensitivity |
| [Final — Capacity Board](missions/final-capacity-board.md) | Compare multiple candidate architectures and rerun after changed constraints | reproducible recommendation |

## Modeling rule

A capacity model is only as credible as its inputs. Every input should state whether it is:

- measured locally
- vendor-specified
- estimated from a cited source
- a fictional scenario assumption
- deliberately simplified for the model

Do not turn public list prices or vendor peak specifications into claims about actual production cost/performance without stating the limitation.

## Reproducibility target

The final project should accept structured workload/constraint inputs—preferably Python + YAML, though a transparent spreadsheet/script is acceptable—and produce repeatable candidate comparisons. Changing an input should change the recommendation through explicit rules rather than manual rewriting.

## Completion condition

Silicon-Tetris is complete when requirements become reproducible inputs, constraints become explicit rules, at least three candidate designs can be compared, and the recommendation changes predictably when power, budget, workload, or growth assumptions change.
