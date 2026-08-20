# Level 03 — The Network Wall

## Briefing
The training team gets every GPU it requested. Scaling efficiency still collapses.

## Objective
Include network bandwidth, topology, oversubscription, and east-west traffic in capacity planning.

## Tasks
Give multi-node training cards an estimated communication demand. Define a leaf/uplink bandwidth model and calculate aggregate offered load under concurrent jobs. Identify placements that concentrate too much traffic on one bottleneck.

## Constraint change
Double the number of distributed jobs without changing the network.

## Evidence
- traffic matrix
- oversubscription/bottleneck calculation
- placement before/after topology awareness

## Victory condition
Your capacity model can say “GPUs are available, but the fabric is the limiting resource.”
