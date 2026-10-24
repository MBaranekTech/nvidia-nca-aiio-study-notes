# NVIDIA NCA-AIIO Study Notes

An independent, exam-blueprint-aligned guide for the **NVIDIA-Certified Associate: AI Infrastructure and Operations (NCA-AIIO)** certification.

> [!IMPORTANT]
> This is an unofficial learning resource, not an exam dump. It is not affiliated with or endorsed by NVIDIA. Product capabilities and exam details change; verify them with the linked official sources.

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

### Blueprint and suggested study time

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

## License

Text and original diagrams are licensed under [CC BY 4.0](LICENSE). NVIDIA product names are trademarks of their respective owner.
