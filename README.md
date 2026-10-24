<p align="center">
  <img src="assets/hero.png" alt="Accelerated computing study desk connected to an AI data center" width="100%">
</p>

<h1 align="center">NVIDIA NCA-AIIO Study Notes</h1>

<p align="center">
  An independent, exam-blueprint-aligned path through AI infrastructure and operations.
</p>

<p align="center">
  <a href="https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-operations-associate/"><img alt="Exam NCA-AIIO" src="https://img.shields.io/badge/Exam-NCA--AIIO-76B900?style=flat-square"></a>
  <img alt="50 questions" src="https://img.shields.io/badge/Questions-50-17212B?style=flat-square">
  <img alt="60 minutes" src="https://img.shields.io/badge/Time-60_min-17212B?style=flat-square">
  <a href="LICENSE"><img alt="CC BY 4.0 license" src="https://img.shields.io/badge/License-CC_BY_4.0-00AEEF?style=flat-square"></a>
</p>

> [!IMPORTANT]
> This is an unofficial learning resource, not an exam dump. It is not affiliated with or endorsed by NVIDIA. Product capabilities and exam details change; verify them with the linked official sources.

## Start here

| 1. Find your gaps | 2. Learn by domain | 3. Prove understanding |
|:---:|:---:|:---:|
| [Take the diagnostic →](practice/questions.md) | [Open the study plan →](STUDY-PLAN.md) | [Try the practical labs →](labs/README.md) |
| 15 original scenario questions | Fast 16-hour or four-week route | Observation and design exercises |

## Exam snapshot

Verified **2026-10-22** against the [official certification page](https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-operations-associate/):

| Item | Current detail |
|---|---|
| Level | Associate |
| Format | 50 questions, online proctored |
| Time | 60 minutes |
| Price | USD 125 (check regional pricing) |
| Prerequisite | Basic understanding of data-center infrastructure |
| Validity | Two years |

## Blueprint and suggested study time

| Domain | Exam weight | 16-hour plan |
|---|---:|---:|
| [Essential AI Knowledge](domains/01-essential-ai-knowledge.md) | 38% | 6 hours |
| [AI Infrastructure](domains/02-ai-infrastructure.md) | 40% | 6.5 hours |
| [AI Operations](domains/03-ai-operations.md) | 22% | 3.5 hours |

## How to use this repository

1. Take the [diagnostic quiz](practice/questions.md) without notes.
2. Read the three domain guides in blueprint order.
3. Complete the [hands-on labs](labs/README.md) on any machine with Docker; an NVIDIA GPU is optional.
4. Review every missed question with the [answer explanations](practice/answers.md).
5. Use the [cram sheet](CRAM-SHEET.md) during the final review—not as your only preparation.
6. Recheck the [official NVIDIA page](https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-operations-associate/) before booking.

## Learning objectives

By the end, you should be able to:

- distinguish AI, machine learning, deep learning, training, and inference;
- explain why GPUs suit parallel AI workloads and where CPUs still matter;
- map CUDA, cuDNN, TensorRT, Triton, NIM, DCGM, GPU Operator, and Base Command Manager to their roles;
- reason about compute, memory, storage, power, cooling, and network bottlenecks;
- select among PCIe, NVLink, Ethernet, InfiniBand, GPUDirect RDMA, and GPUDirect Storage;
- explain DPU offload, acceleration, and isolation;
- distinguish MIG, time-slicing, passthrough, and vGPU;
- choose meaningful GPU health, utilization, and workload metrics.

## The platform in one picture

```mermaid
flowchart BT
    H[GPU · DPU · Network · Storage] --> D[Driver · CUDA · Container Runtime]
    D --> L[cuDNN · NCCL · Accelerated Libraries]
    L --> O[TensorRT · Triton · NIM · RAPIDS]
    O --> W[Training · Inference · Data Science Workloads]
    M[DCGM · GPU Operator · Schedulers] -. observe and operate .-> D
    M -. manage .-> W
```

The exam rewards knowing both the layers and their boundaries: optimization is not serving, monitoring is not scheduling, and GPU enablement is not application autoscaling.

## Repository map

- [`STUDY-PLAN.md`](STUDY-PLAN.md) — two practical schedules
- [`domains/`](domains/) — blueprint-aligned study notes
- [`practice/`](practice/) — original questions and explained answers
- [`labs/`](labs/) — safe observation exercises
- [`CRAM-SHEET.md`](CRAM-SHEET.md) — last-day comparisons
- [`GLOSSARY.md`](GLOSSARY.md) — high-frequency terms
- [`resources/SOURCES.md`](resources/SOURCES.md) — primary sources and freshness notes

## Integrity and scope

All questions here are original and test public concepts. Do not contribute recalled live-exam questions, proprietary course screenshots, answer dumps, or confidential material. Exact product specifications are deliberately kept out of the core notes unless they illustrate a concept; always verify current product documentation.

<details>
<summary><strong>Why this guide avoids memorizing long specification tables</strong></summary>

Product limits change across architectures and software releases. The notes teach durable selection cues first, then point to primary documentation for current limits. That makes the guide useful beyond a single exam revision.

</details>

## License

Text and original diagrams are licensed under [CC BY 4.0](LICENSE). NVIDIA product names are trademarks of their respective owner.
