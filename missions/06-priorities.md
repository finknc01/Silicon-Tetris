# Level 06 — Mixed Workload Chaos

## Briefing
Research wants long training jobs. Product wants low-latency inference. Finance wants high utilization. They all share the same fleet.

## Objective
Model priorities, reservations, queues, fragmentation, and utilization-vs-SLA tradeoffs.

## Tasks
Assign priority classes and service goals. Simulate a simple scheduling period manually or with Python. Compare a utilization-maximizing policy against a policy that reserves capacity for latency-sensitive workloads.

## Surprise
A critical inference workload arrives while the cluster is 90% allocated.

## Evidence
- scheduling timeline
- SLA misses
- utilization comparison
- policy recommendation

## Victory condition
You can show why 100% utilization may be a bad capacity-planning goal.
