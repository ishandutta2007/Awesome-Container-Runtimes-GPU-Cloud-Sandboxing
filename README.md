# Awesome-Container-Runtimes-GPU-Cloud-Sandboxing

## Top Container Runtimes & GPU Cloud Sandboxing Ecosystem



**Curated List of SaaS/Hosted Platforms & Open-Source GitHub Projects**  

*Focused on GPU-Accelerated Container Runtimes, Isolated AI Agent Sandboxes, MicroVMs, Serverless GPU Clouds & Kernel-Level Isolation*  

**Last updated: November 2026**



This repository tracks notable **SaaS/hosted platforms** and **open-source projects** for **Container Runtimes & GPU Cloud Sandboxing**. These tools isolate, schedule, accelerate, and execute untrusted AI-generated code, GPU-accelerated containers, and multi-tenant workloads across bare-metal GPU clusters, microVMs, rootless container runtimes, and serverless GPU clouds.



**Examples** include RunPod, Lambda Labs, CoreWeave, Vast.ai, Together AI, Modal, Anyscale, FluidStack, JarvisLabs, Crusoe Cloud, and NVIDIA/OpenShell (the category leaders and popular runtimes). 



**Open-source emphasis**: This section is heavily expanded with every major active project for secure AI agent & GPU sandboxing (`NVIDIA/OpenShell`, `gVisor`, `Kata Containers`, `Firecracker`, `E2B`, `Daytona`), GPU-aware OCI container runtimes (`NVIDIA Container Toolkit`, `containerd`, `CRI-O`, `Podman`), and distributed GPU cluster schedulers (`Ray`, `SkyPilot`, `dstack`) — ideal for AI infrastructure engineers, MLOps architects, platform teams, and security researchers.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)

- [SaaS/Hosted Platforms](#saashosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Support & Share](#support--share)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global GPU-as-a-Service (GPUaaS) and GPU Cloud infrastructure sector is estimated at **$43.6B to $50B+ in 2026** (growing at a 20–30%+ CAGR), transitioning heavily from exploratory training clusters to continuous, production-grade AI agent sandboxes and low-latency inference workloads. The sector exhibits a **moderately fragmented, multi-tiered structure**: top-tier hyperscalers (AWS, Azure, GCP, OCI) command foundational enterprise spend (>60%), while high-growth specialized "neoclouds" (CoreWeave, Crusoe, Lambda, Modal) capture massive market share on price-performance, bare-metal InfiniBand fabrics, and developer ergonomics, flanked by peer-to-peer/decentralized marketplaces (Vast.ai) addressing cost-sensitive spot execution.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue Scale | Starting Pricing | Free Tier / Trial Limits | Key Capabilities & Architecture |
| :--- | :--- | :--- | :--- | :--- |
| **[Crusoe Cloud](https://crusoe.ai)** | **$30.9B Valuation** (~$2B ARR) | ~$2.00/hr (On-demand GPU instances; H100 SXM ~$2.30–$3.00/hr) | **No Free Tier / No Free Trial** (Enterprise evaluation credits issued selectively via sales team) | Climate-aligned high-density GPU infrastructure powered by stranded/clean energy; managed Kubernetes, Slurm, and InfiniBand networking. |
| **[CoreWeave](https://coreweave.com)** | **$27B–$28B Market Cap** (~$13B ARR guidance) | ~$1.28/hr (RTX A6000; H100 SXM5 ~$2.06/hr, A100 80GB ~$2.21/hr) | **CoreWeave Forge Free Plan** ($0/mo for experiment tracking & model evaluation); $50 one-time developer credits on signup; no free GPU hours. | Specialized bare-metal Kubernetes GPU cloud with InfiniBand fabrics; zero egress fees and high-performance NVMe/object storage. |
| **[FluidStack](https://fluidstack.io)** | **$18B Valuation** (~$660M ARR) | ~$1.50/hr (Starting on-demand GPU rate; H100 ~$1.50–$2.30/hr) | **No Free Tier / No Free Trial** (Enterprise contracts and custom deployments only; no public self-service tier) | High-speed bare-metal and containerized GPU cloud clusters tailored for LLM training labs, custom data centers, and multi-cloud brokers. |
| **[Modal](https://modal.com)** | **$15.75B Valuation** (~$1B ARR) | $0.00/mo base + $0.00005/core-sec CPU, ~$0.00016/sec (T4 ~$0.59/hr, A100 80GB ~$3.40/hr) | **Permanent Free Starter Tier**: $30/month recurring free compute credits, 3 seats, 100 max containers, 10 GPU concurrency limit, 1 TiB/month egress. | Serverless cloud compute and sub-second container sandboxing; Python-native GPU scheduling for isolated AI agent execution and inference. |
| **[Lambda Labs](https://lambdalabs.com)** | **$14.5B Valuation** (~$1.5B ARR) | ~$0.79/hr (A10; H100 SXM ~$2.49–$2.99/hr billed per minute) | **No Free Tier / No Free Trial** (Paid accounts only with credit card validation; zero developer trial credits) | Developer-centric AI cloud with 1-Click Clusters, pre-configured ML container runtimes, zero egress charges, and on-demand H100/B200 nodes. |
| **[Together AI](https://together.ai)** | **$8.3B Valuation** | ~$0.14 per 1M tokens (Serverless inference) / ~$3.99/hr (Dedicated H100 GPU clusters) | **No Free Tier** ($15 minimum initial prepaid deposit required; Startup grant program offers $15K–$50K credits upon application) | Unified AI acceleration platform pairing serverless model endpoints, dedicated GPU clusters, and isolated Python code interpreter sandboxes. |
| **[Anyscale](https://anyscale.com)** | **$1.65B Valuation** (Acquired by Nscale; ~$100M ARR) | ~$0.0135/hr (CPU instances), ~$0.57/hr (T4 GPU), ~$4.96/hr (A100 GPU) | **Permanent Free Account Tier** with community support + **$100 one-time free trial credits** for new developer signups. | Managed Ray compute platform for scalable distributed AI workloads, multi-node GPU clusters, and serverless Ray Serve endpoints. |
| **[RunPod](https://runpod.io)** | **$1.0B Valuation** (~$240M ARR) | ~$0.16/hr (Community Cloud RTX A5000), ~$0.34/hr (RTX 4090), Secure Cloud H100 from ~$2.69/hr | **No Free Tier / No Free Trial** (Requires pre-funded account balance; per-second billing with zero egress fees) | Globally distributed container pods, serverless GPU workers, and custom Docker template deployments across community and secure data centers. |
| **[JarvisLabs.ai](https://jarvislabs.ai)** | **~$1.2M ARR** (Private / Bootstrapped) | ~$0.44/hr (NVIDIA L4), ~$1.49/hr (A100 80GB), H100 from ~$2.69/hr | **No Free Tier / No Free Trial** ($5 minimum wallet balance top-up required to launch; pause/resume storage at ~$0.005/GB/day) | Instant Jupyter/VS Code GPU containers, pause-and-resume persistent storage, spot instances (up to 56% off), and lightweight Python SDK. |
| **[Vast.ai](https://vast.ai)** | **Early-Stage Venture Backed** (~$4M funding) | ~$0.20/hr (Starting RTX 3080/4090 spot rates; H100 from ~$0.90–$2.40/hr) | **No Free Tier / No Free Trial** (Prepaid deposit required before instance startup; unallocated balance refundable) | Decentralized peer-to-peer GPU marketplace providing low-cost Docker container execution with real-time bidding, spot pricing, and search filters. |







## Open-Source GitHub Projects



- **[NVIDIA/OpenShell](https://github.com)**  

  Open-source secure runtime and sandboxing environment from NVIDIA engineered for isolating autonomous AI agents, shell execution, and GPU-accelerated developer workflows.



- **[NVIDIA Container Toolkit (`NVIDIA/nvidia-container-toolkit`)](https://github.com)**  

  Foundational open-source toolkit enabling Docker, `containerd`, `CRI-O`, and Podman to automatically expose NVIDIA GPUs, CUDA drivers, and CDI specs inside Linux containers.



- **[gVisor (`google/gvisor`)](https://github.com)**  

  Open-source application kernel written in Go (`runsc`) that intercepts container syscalls in user space to provide strong VM-like isolation for untrusted code execution and AI sandboxes.



- **[Kata Containers (`kata-containers/kata-containers`)](https://github.com)**  

  Open-source OCI-compatible container runtime that runs every container inside its own lightweight hardware-virtualized microVM (QEMU, Cloud Hypervisor, Firecracker) with PCIe GPU passthrough.



- **[Firecracker (`firecracker-microvm/firecracker`)](https://github.com)**  

  Minimalist, high-security open-source Virtual Machine Monitor (VMM) written in Rust by AWS for launching isolated multi-tenant microVMs in milliseconds.



- **[E2B (`e2b-dev/e2b`)](https://github.com)**  

  Open-source cloud runtime and SDK powered by Firecracker microVMs built specifically for running untrusted LLM-generated code, stateful terminals, and AI agent sandboxes safely.



- **[Ray (`ray-project/ray`)](https://github.com)**  

  Leading open-source unified compute framework for scaling Python and AI workloads across multi-node GPU clusters with distributed actor scheduling and Ray Serve.



- **[SkyPilot (`skypilot-org/skypilot`)](https://github.com)**  

  Open-source broker framework for running AI, batch jobs, and GPU containers seamlessly across AWS, GCP, Azure, Lambda, RunPod, Vast.ai, and Kubernetes with automatic spot recovery.



- **[dstack (`dstackai/dstack`)](https://github.com)**  

  Open-source container orchestrator designed specifically for AI workloads, simplifying GPU provisioning, dev environments, and distributed training across any cloud or on-prem GPU server.



- **[containerd (`containerd/containerd`) & runc (`opencontainers/runc`)](https://github.com)**  

  Industry-standard CNCF open-source container runtime and OCI low-level executor powering Kubernetes, Docker, and cloud GPU node pools worldwide.



- **[Daytona (`daytonaio/daytona`)](https://github.com)**  

  Open-source elastic sandbox and development environment manager providing sub-second isolated container runtimes for AI agents and developer workspaces.



### Additional Strong Open-Source Options



- **[Sysbox (`nestybox/sysbox`)](https://github.com)** for an open-source enhanced `runc` container runtime capable of running Docker-in-Docker, systemd, and Kubernetes inside unprivileged rootless containers safely.

- **[Podman (`containers/podman`)](https://github.com)** and **[Apptainer / Singularity (`apptainer/apptainer`)](https://github.com)** for daemonless, rootless container runtimes widely used on multi-tenant HPC and university GPU clusters.

- **[HAMi (`Project-HAMi/HAMi`)](https://github.com)** and **[NVIDIA GPU Operator (`NVIDIA/gpu-operator`)](https://github.com)** for open-source GPU virtualization, vGPU fractional sharing, and automated Kubernetes GPU driver/toolkit lifecycle management.

- **[Cloud Hypervisor (`cloud-hypervisor/cloud-hypervisor`)](https://github.com)** for a modern, Rust-based Virtual Machine Monitor optimized for cloud-native workloads and VFIO GPU passthrough.

- **[Microsandbox (`microsandbox/microsandbox`)](https://github.com)** for self-hosted, fast-booting microVM sandboxes engineered for executing untrusted AI agent code locally or on-prem.



**Frameworks for building custom systems**: Combine **NVIDIA/OpenShell** or **gVisor / Kata Containers** for hardened container and AI-agent sandboxing, **NVIDIA Container Toolkit + HAMi** for fractional GPU sharing, and **SkyPilot** or **Ray** for multi-cloud GPU cluster orchestration.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS/hosted or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Support & Share



If you find this curated list helpful, consider supporting the project:



- ⭐ **Star this repository** to help others discover it.

- 🍴 **Fork & Share** it with your team, friends, or community on X/Twitter, LinkedIn, and Reddit.

- ☕ **Buy me a coffee / Sponsor** my open-source work on [GitHub Sponsors](https://github.com) — featuring tiers for profile badges, README shoutouts, logo placements, and prioritized bug fixes/features!



[![Sponsor @ishandutta2007](https://shields.io)](https://github.com)



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Standard OCI containers (`runc`) share the host Linux kernel; when executing untrusted AI-generated code or multi-tenant workloads, always use hardware microVMs (`Firecracker`, `Kata Containers`, `E2B`) or user-space syscall kernels (`gVisor`) alongside strict network egress controls.

- GPU cloud workloads and multi-node clusters incur rapid compute charges; configure automatic idle shutdowns, spot-instance fallbacks, and VRAM/disk quotas.



---



**Made for AI infrastructure engineers, MLOps architects, platform teams, security researchers, and open-source contributors.**  

Let's make container runtimes and GPU cloud sandboxing more open, isolated, and portable.
