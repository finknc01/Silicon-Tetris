# Capacity Model Input Contract

The starter YAML files define the **inputs**, not the planner implementation.

## `inputs/workloads.yaml`
Each workload may contain:
- `name`: unique identifier;
- `type`: training / fine_tuning / batch_inference / realtime_inference;
- `priority`: policy importance;
- `minimum_gpus` and `target_gpus`;
- `minimum_vram_per_gpu_gb`;
- compute-time estimate;
- network sensitivity;
- checkpoint behavior;
- latency/availability requirements where relevant.

## `inputs/hardware_catalog.yaml`
The starter catalog is fictional. Hardware entries provide candidate GPU attributes; node profiles combine GPU choice with node-level power, rack, network, storage, and cost inputs.

Do not bury derived values in the input file if the planner can calculate them. For example, node power should be calculated from GPU count × GPU power + non-GPU power.

## `inputs/constraints.yaml`
Defines global limits and policy requirements such as budget, rack power, space, network/storage capacity, reserve headroom, and planning horizon.

## Planner expectations
The future planner should:
1. parse these files;
2. validate required fields and reject malformed inputs clearly;
3. evaluate whether candidate configurations satisfy hard constraints;
4. identify the first/most important constraint when a design fails;
5. calculate cost/power/capacity rather than hiding answers in YAML;
6. produce a human-readable summary plus structured output;
7. return the same result for the same inputs;
8. rerun cleanly after one constraint changes.

## Evidence labels
If the project later uses real hardware or prices, record whether each value is:
- measured;
- public vendor specification;
- dated public price;
- derived;
- fictional/scenario assumption.
