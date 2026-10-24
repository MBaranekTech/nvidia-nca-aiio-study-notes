# Practice Answers and Explanations

1. **B.** The CPU input pipeline is starving the GPU; adding accelerators leaves the bottleneck in place.
2. **A.** TensorRT optimizes and runs inference. DCGM monitors GPUs; Slurm schedules jobs; BlueField is a DPU platform.
3. **B.** GPU Operator manages these Kubernetes GPU-enablement components. Autoscalers solve different scaling problems.
4. **B.** GPUDirect Storage targets storage-to-GPU data movement while avoiding a CPU bounce buffer.
5. **B.** Scale adds overhead and exposes bottlenecks; useful parallel work rarely grows perfectly with device count.
6. **B.** Temperature alone is context; an explicit thermal-throttling reason links heat to performance restriction.
7. **B.** A DPU offloads, accelerates, and isolates networking, storage, and security services.
8. **C.** MIG provides hardware partitions on supported products. Time-slicing interleaves access without equivalent isolation.
9. **A.** DCGM supplies GPU telemetry, health, diagnostics, topology, and job statistics.
10. **A.** Synchronized workers wait on collective communication, making fabric latency and stragglers important.
11. **B.** PUE is total facility energy divided by IT equipment energy.
12. **A.** The endpoints are a third-party PCIe device (NIC) and GPU memory: GPUDirect RDMA.
13. **B.** A container improves portability but does not contain the kernel driver; compatible host/runtime integration remains necessary.
14. **B.** Cloud can reduce procurement lead time and match temporary demand. The other claims are not inherent cloud benefits.
15. **B.** A single utilization metric is not the mission; outcome, reliability, efficiency, and workload context are.

## Score interpretation

- **13–15:** strong foundation; investigate every miss and verify current product specifics.
- **10–12:** solid start; revisit the relevant domain and retest later.
- **0–9:** work through all domain notes and the official fundamentals course before another timed attempt.

This short quiz does not predict an exam result or cover every blueprint objective.
