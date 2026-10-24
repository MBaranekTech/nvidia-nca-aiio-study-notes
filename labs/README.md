# Hands-on Labs

These labs reinforce operational reasoning. They do not reproduce the certification exam. Commands are read-only unless explicitly described.

## Lab 1 — Inspect a GPU host

On a host with an NVIDIA GPU and driver:

```bash
nvidia-smi
nvidia-smi --query-gpu=name,temperature.gpu,power.draw,utilization.gpu,memory.used,memory.total --format=csv
nvidia-smi topo -m
```

Questions: Which values describe capacity, instantaneous activity, health, and topology? What extra evidence would you need before declaring a bottleneck?

## Lab 2 — Compare CPU and GPU container assumptions

Run a normal container, then inspect the NVIDIA Container Toolkit documentation before attempting a GPU container. Write down which layers live in the image and which remain on the host: kernel driver, CUDA user-space libraries, application, and orchestration integration.

## Lab 3 — Build a monitoring hypothesis

For each symptom, name at least three possible causes and the next metric/log to inspect:

- low GPU utilization;
- falling clocks;
- training throughput drops only at multi-node scale;
- periodic stalls during checkpoints;
- pods remain pending despite an apparently idle GPU.

## Lab 4 — Design a small cluster

Sketch four GPU nodes and label:

- scale-up versus scale-out links;
- compute, storage, in-band management, and out-of-band management traffic;
- shared storage and checkpoint path;
- scheduler/orchestrator;
- telemetry flow;
- redundant power and cooling assumptions.

Then identify the first three measurements you would collect during a slow distributed-training incident.
