# Cram Sheet

## High-value distinctions

- **Training:** learns weights; forward + backward passes; usually throughput oriented.
- **Inference:** consumes learned weights; usually latency/cost oriented.
- **CUDA:** platform/runtime. **cuDNN:** neural-network primitives. **TensorRT:** inference optimization/runtime. **Triton:** model server. **NIM:** packaged inference microservice.
- **DCGM:** GPU health/telemetry. **Base Command Manager:** cluster management. **GPU Operator:** Kubernetes GPU software lifecycle.
- **NVLink/NVSwitch:** scale-up GPU connectivity. **InfiniBand/Ethernet:** scale-out network connectivity.
- **P2P:** GPU ↔ GPU. **GPUDirect RDMA:** GPU ↔ NIC/PCIe device. **GDS:** GPU ↔ storage.
- **MIG:** hardware partitioning and isolation on supported GPUs. **Time-slicing:** temporal sharing without equivalent memory/fault isolation.
- **DPU:** offload, accelerate, isolate infrastructure services.
- **kW:** power. **kWh:** energy. **PUE:** facility energy / IT energy.

## Scenario cues

| If the question emphasizes… | First concept to evaluate |
|---|---|
| GPU health, XID, ECC, temperature | DCGM |
| Kubernetes driver/device-plugin lifecycle | GPU Operator |
| Optimized inference execution | TensorRT |
| Serving models over APIs | Triton or NIM; inspect packaging/support cues |
| Collective operations across GPUs | NCCL + topology/fabric |
| Direct storage-to-GPU path | GPUDirect Storage |
| Network device directly accessing GPU memory | GPUDirect RDMA |
| Tenant isolation on one supported GPU | MIG or vGPU, depending deployment model |
| CPU cycles consumed by networking/security | DPU |
| GPUs frequently idle during input | Data/CPU/storage/network pipeline |

## Exam method

At 50 questions in 60 minutes, average time is 72 seconds each. First identify the domain and the exact constraint. Eliminate answers that solve a neighboring problem. Mark uncertain questions, keep moving, and use remaining time to review absolutes such as “always,” “only,” and “every.”
