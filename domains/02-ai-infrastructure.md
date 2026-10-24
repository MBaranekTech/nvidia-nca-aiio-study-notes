# Domain 2 — AI Infrastructure (40%)

## 1. Start with the workload

Infrastructure choices follow the workload: model size, precision, dataset, batch size, latency target, concurrency, reliability, data locality, compliance, and budget. A bottleneck may be compute, GPU memory capacity, memory bandwidth, interconnect, network, storage, CPU input pipeline, power, or cooling.

Vertical scaling adds capability within a node; horizontal scaling adds nodes. Scaling efficiency falls when communication, synchronization, storage, or imbalance dominates useful computation.

## 2. GPU topology

- **PCIe** connects devices to the host and can support GPU peer access.
- **NVLink** provides high-bandwidth GPU-to-GPU connectivity in supported systems.
- **NVSwitch** creates high-bandwidth, many-GPU connectivity within supported platforms.
- **InfiniBand or high-speed Ethernet** provide scale-out node-to-node fabrics.

Topology matters: nominal GPU count says little about communication paths, locality, oversubscription, or end-to-end performance.

## 3. Data paths that sound alike

| Technology | Endpoints | Main benefit |
|---|---|---|
| CUDA P2P | GPU ↔ GPU in a supported system topology | Avoids staging through host memory |
| GPUDirect RDMA | GPU memory ↔ third-party PCIe device, commonly a NIC | Direct network/device transfers |
| GPUDirect Storage | GPU memory ↔ supported storage path | Avoids CPU bounce buffering for data I/O |

Identify both endpoints before selecting the technology.

## 4. Network design

AI clusters commonly separate traffic by purpose: compute, storage, in-band management, and out-of-band management. Designs vary; four fabrics are not a universal law.

Important concepts include bandwidth, latency, jitter, loss, congestion, oversubscription, topology, redundancy, and east-west traffic. Distributed training is sensitive to collective communication and tail latency. RDMA permits direct memory access with low CPU overhead; RoCE carries RDMA over Ethernet and requires a carefully engineered fabric, while InfiniBand is a purpose-built high-performance fabric.

## 5. Storage and data pipeline

Capacity alone is insufficient. Consider throughput, IOPS, latency, metadata rate, small-file behavior, parallel access, caching, locality, durability, and checkpoint patterns. If GPUs wait for data, faster GPUs will not solve the pipeline bottleneck.

## 6. Facilities: power and cooling

Plan beyond device TDP. Include CPUs, memory, networking, storage, power conversion, redundancy, rack density, growth headroom, and cooling overhead. Heat removed equals power consumed at steady state. High-density deployments may require liquid cooling and facility changes.

Useful facility concepts:

- **kW** is instantaneous power; **kWh** is energy over time.
- **PUE** = total facility energy / IT equipment energy; closer to 1 is better.
- Redundant feeds and cooling improve availability but add cost and capacity requirements.
- Nameplate maximum, design load, and measured typical load are different inputs.

## 7. On-premises versus cloud

| On-premises | Cloud |
|---|---|
| Greater physical control and data locality | Faster access and elastic capacity |
| Up-front capital and longer procurement | Consumption pricing and service availability constraints |
| Facility and lifecycle responsibility | Provider operates underlying facility |
| Can be economical at steady high utilization | Can be economical for variable or temporary demand |

Hybrid decisions involve data gravity, network egress, sovereignty, skills, utilization, lead time, and operational model—not only hourly compute price.

## 8. DPU mental model

A DPU such as NVIDIA BlueField handles infrastructure services using dedicated compute and accelerators. Remember three verbs: **offload**, **accelerate**, and **isolate** networking, storage, and security tasks. This can free host CPU cycles and separate infrastructure control from tenant workloads.

## Self-check

1. Why can doubling GPU count produce much less than 2× speedup?
2. Which data path fits GPU-to-storage traffic?
3. Why is rack power not the sum of GPU TDP values?
4. When might cloud elasticity outweigh a higher steady-state unit cost?
