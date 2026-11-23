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

- [SaaS/Hosted Platforms](#saashosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Support & Share](#support--share)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Modal](https://modal.com)**  

  Serverless cloud compute and container sandbox platform engineered for AI/ML workloads, offering sub-second cold starts, Python-native GPU scheduling, and isolated code sandboxes.



- **[RunPod](https://runpod.io)**  

  Globally distributed GPU cloud platform providing instant Docker container pods, serverless GPU workers, and custom template deployments for AI training and inference.



- **[CoreWeave](https://coreweave.com)**  

  Specialized GPU-accelerated cloud infrastructure provider built on bare-metal Kubernetes with InfiniBand networking for large-scale AI training and inference clusters.



- **[Lambda Labs (Lambda Cloud)](https://lambdalabs.com)**  

  Developer-focused GPU cloud platform offering on-demand H100/B200 instances, 1-Click Clusters, and pre-configured ML container environments.



- **[Together AI](https://together.ai)**  

  Cloud AI acceleration platform combining serverless open-source model inference, dedicated GPU clusters, and isolated Python code-interpreter sandboxes.



- **[Anyscale](https://anyscale.com)**  

  Managed cloud platform built by the creators of Ray for scaling distributed AI workloads, multi-node GPU clusters, and serverless compute endpoints.



- **[Vast.ai](https://vast.ai)**  

  Decentralized GPU cloud marketplace enabling low-cost Docker container execution across globally distributed host machines with flexible hardware filtering.



- **[FluidStack](https://fluidstack.io)**  

  Cloud GPU platform delivering high-speed bare-metal and containerized NVIDIA GPU clusters for AI labs, enterprises, and inference workloads.



- **[Crusoe Cloud](https://crusoe.ai)**  

  Climate-aligned AI cloud infrastructure powered by stranded and clean energy, offering managed Kubernetes, Slurm clusters, and high-density GPU VMs.



- **[JarvisLabs.ai](https://jarvislabs.ai)**  

  Streamlined GPU cloud platform tailored for AI researchers and developers with instant Jupyter/VS Code containers, pause/resume storage, and Python SDK automation.





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
