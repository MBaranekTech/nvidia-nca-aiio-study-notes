# Original Practice Questions

Choose the best answer. These are independently written study questions, not recalled exam content.

1. A training job shows 20% GPU utilization while CPU cores are saturated preparing images. What should be addressed first?
   - A. Add more GPUs
   - B. Optimize or parallelize the input pipeline
   - C. Enable MIG
   - D. Lower network MTU

2. Which component primarily optimizes neural-network inference graphs and kernels?
   - A. TensorRT
   - B. DCGM
   - C. Slurm
   - D. BlueField

3. A Kubernetes team needs automated deployment of drivers, device plugin, Container Toolkit, and DCGM Exporter. What best fits?
   - A. Triton
   - B. GPU Operator
   - C. Horizontal Pod Autoscaler
   - D. NCCL

4. A supported application needs a direct data path between storage and GPU memory. Which technology is most relevant?
   - A. CUDA P2P
   - B. GPUDirect Storage
   - C. MIG
   - D. NVML

5. Why may eight GPUs fail to provide 8× the performance of one GPU?
   - A. GPUs cannot execute in parallel
   - B. Communication, synchronization, I/O, and serial work add overhead
   - C. CPUs disable GPU memory
   - D. Distributed jobs use only inference

6. Which metric most directly indicates a cooling-related GPU constraint?
   - A. Model parameter count
   - B. Thermal throttle reason with elevated temperature
   - C. Storage capacity
   - D. Scheduler queue length

7. What is a primary DPU value proposition?
   - A. Replace all GPUs for model training
   - B. Offload and isolate infrastructure services
   - C. Increase dataset labels
   - D. Compile CUDA kernels

8. Which statement best compares MIG and time-slicing?
   - A. Both guarantee identical hardware isolation
   - B. Time-slicing has stronger memory isolation
   - C. MIG partitions supported hardware resources; time-slicing shares execution over time
   - D. MIG is a storage protocol

9. A team needs GPU health checks, diagnostics, and fleet telemetry. Which tool is the closest match?
   - A. DCGM
   - B. TensorRT
   - C. cuDNN
   - D. NIM

10. Which workload characteristic most often increases sensitivity to scale-out network latency?
    - A. Tightly synchronized distributed training
    - B. A single CPU-only script
    - C. Offline archive storage
    - D. BMC firmware inventory

11. What does a PUE of 1.2 describe?
    - A. GPU utilization is 120%
    - B. Total facility energy is 1.2 times IT equipment energy
    - C. Every rack uses 1.2 kW
    - D. Cooling uses no energy

12. A NIC must directly exchange data with GPU memory over a supported PCIe topology. Which capability applies?
    - A. GPUDirect RDMA
    - B. GPUDirect Storage
    - C. CUDA P2P only
    - D. vGPU

13. Which statement about containers is most accurate?
    - A. They eliminate host driver compatibility concerns
    - B. They package applications, but GPU access still depends on compatible host integration
    - C. They automatically scale cluster nodes
    - D. They replace the workload scheduler

14. Which factor most strongly favors cloud for a short experimental project?
    - A. A requirement to own the physical rack
    - B. Rapid provisioning and elastic capacity
    - C. Guaranteed zero data-transfer cost
    - D. No need for governance

15. What is the best operational objective?
    - A. Keep every GPU at 100% utilization regardless of workload
    - B. Optimize service goals, reliability, and useful work per cost using contextual metrics
    - C. Alert on every metric sample
    - D. Avoid collecting application metrics
