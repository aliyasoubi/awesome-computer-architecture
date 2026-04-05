# [Awesome Computer Architecture](https://github.com/aliyasoubi/awesome-computer-architecture) 
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome computer architecture resources, including simulators, benchmarks, tools, and tutorials. This repository serves as a robust resource for researchers, graduate students, and hardware engineering enthusiasts.

## Table of Contents
- [Books](#books)
- [Conferences](#conferences)
- [Simulators](#simulators)
  - [CPU Simulators](#cpu-simulators)
  - [GPU/Accelerator Simulators](#gpuaccelerator-simulators)
  - [Memory System Simulators](#memory-system-simulators)
  - [Full-System/Cloud Simulators](#full-systemcloud-simulators)
  - [RTL/FPGA Simulators](#rtlfpga-simulators)
  - [Specialized/Historical Tools](#specializedhistorical-tools)
- [Benchmarks](#benchmarks)
- [Tools for Research](#tools-for-research)
- [ISA References & Specs](#isa-references--specs)
- [Compilers & Binary Analysis](#compilers--binary-analysis)
- [Traces & Datasets](#traces--datasets)
- [Tutorials](#tutorials)
- [Cutting-Edge Research & Emerging Architectures](#cutting-edge-research--emerging-architectures)
  - [AI & Large Language Model (LLM) Hardware](#ai--large-language-model-llm-hardware)
  - [Advanced Packaging & Chiplets (2.5D/3D Integration)](#advanced-packaging--chiplets-25d3d-integration)
  - [Memory Disaggregation & Processing-in-Memory (PIM)](#memory-disaggregation--processing-in-memory-pim)
  - [Hardware Security & Confidential Computing](#hardware-security--confidential-computing)
- [Elite Research Labs in Computer Architecture & Systems](#elite-research-labs-in-computer-architecture--systems)
- [Hall of Fame](#hall-of-fame)
- [How to Contribute](#how-to-contribute)
- [License](#license)


---

## Books

Essential reading materials for computer architecture, ranging from foundational concepts to advanced quantitative analysis.

| Book | Author(s) | Focus | Link |
|------|-----------|-------|------|
| **Computer Architecture: A Quantitative Approach** | Hennessy & Patterson | The definitive guide for graduate-level architecture. | [Link](https://store.elsevier.com/eu/book/9780128119051/computer-architecture) |
| **Computer Organization and Design (RISC-V Edition)** | Patterson & Hennessy | Best for undergraduate basics and RISC-V fundamentals. | [Link](https://store.elsevier.com/eu/book/9780128203316/computer-organization-and-design-risc-v-edition) |
| **Digital Design and Computer Architecture** | Harris & Harris | Connecting logic gates to processor design. | [Link](https://store.elsevier.com/eu/book/9780123944245/digital-design-and-computer-architecture) |
| **Modern Processor Design** | Shen & Lipasti | Deep dive into superscalar processor microarchitecture. | [Link](https://www.waveland.com/browse.php?t=384) |

---

## Conferences

The top-tier (Tier-1) academic conferences where the latest computer architecture research is published.

| Conference | Description | Focus Area | Link |
|------------|-------------|------------|------|
| **ISCA** | Int'l Symposium on Computer Architecture | The premier forum for new ideas in computer architecture. | [ACM SIGARCH](https://www.sigarch.org/events/isca/) |
| **MICRO** | Int'l Symposium on Microarchitecture | Advanced microarchitecture and compiler techniques. | [MICRO](https://www.microarch.org/) |
| **HPCA** | Int'l Symposium on High-Performance Computer Architecture | High-performance system design and analysis. | [IEEE TCCA](https://www.computer.org/communities/technical-committees/tcca) |
| **ASPLOS** | Architectural Support for Programming Languages and OS | The intersection of hardware, OS, and compilers. | [ACM SIGARCH](https://www.sigarch.org/events/asplos/) |

---

## Simulators

### CPU Simulators
| Simulator | Description | Use Case | Link |
|-----------|-------------|----------|------|
| **gem5** | Modular, open-source CPU/SoC simulator. | Cache, branch prediction, OoO CPUs. | [gem5.org](https://www.gem5.org/) |
| **QEMU** | Fast full-system emulator. | OS/software prototyping. | [qemu.org](https://www.qemu.org/) |
| **SST** | Parallel simulator for large-scale systems. | HPC/SoC co-design. | [sst-simulator.org](https://sst-simulator.org/) |
| **MARSSx86** | Cycle-accurate x86 simulator. *(low activity)* | x86 microarchitecture analysis. | [marss86.org](https://marss86.org/) |
| **ZSim** | Fast, scalable x86-64 multicore simulator. | Cache hierarchy and NUCA research. | [ZSim](https://github.com/s5z/zsim) |
| **Sniper** | Interval-based multicore simulator. | Large-scale CMP performance studies. | [Sniper](https://snipersim.org/) |
| **ChampSim** | Trace-driven simulator for branch prediction and prefetching. | De-facto standard for branch/prefetch research (ISCA/MICRO). | [ChampSim](https://github.com/ChampSim/ChampSim) |

### GPU/Accelerator Simulators
| Simulator | Description | Use Case | Link |
|-----------|-------------|----------|------|
| **GPGPU-Sim** | Cycle-accurate NVIDIA GPU simulator. | CUDA kernel analysis. | [GPGPU-Sim](https://github.com/gpgpu-sim/gpgpu-sim_distribution) |
| **Accel-Sim** | Validated GPU simulator for modern workloads. | Tensor cores and deep learning workloads. | [Accel-Sim](https://github.com/accel-sim/accel-sim-framework) |
| **Timeloop** | Deep learning accelerator modeling framework. | Energy/performance optimization. | [Timeloop](https://github.com/NVlabs/timeloop) |
| **SCALE-Sim** | Systolic array simulator for deep neural networks. | TPU-like architectures. | [SCALE-Sim](https://github.com/ARM-software/SCALE-Sim) |
| **STONNE** | Cycle-level simulation framework for DL inference. | Design-space exploration for DL accelerators. | [STONNE](https://github.com/stonne-sim/stonne) |

### Memory System Simulators  
| Simulator | Description | Use Case | Link |
|-----------|-------------|----------|------|
| **DRAMSim3** | Cycle-accurate DRAM simulator. | DDRx/LPDDRx modeling. | [DRAMSim3](https://github.com/umd-memsys/DRAMsim3) |
| **Ramulator** | Supports HBM, GDDR, and emerging memories. | Memory controller design. | [Ramulator](https://github.com/CMU-SAFARI/ramulator) |
| **Ramulator 2** | Redesigned Ramulator with cleaner, modular API. | Next-gen memory protocol research. | [Ramulator2](https://github.com/CMU-SAFARI/ramulator2) |
| **MQSim** | NVMe and SSD simulator. | Computational storage and near-data processing. | [MQSim](https://github.com/CMU-SAFARI/MQSim) |

### Full-System/Cloud Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **FireSim**     | FPGA-accelerated datacenter simulator.       | Cloud hardware research.          | [FireSim](https://fires.im/) |  
| **Simics**      | Commercial full-system simulator.            | Enterprise virtual prototyping.   | [Simics](https://www.windriver.com/simics) |  

### RTL/FPGA Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **Verilator**   | Fast RTL-to-C++ simulator.                   | Pre-silicon verification.         | [Verilator](https://www.veripool.org/verilator/) |  
| **VCS**         | Commercial RTL simulator (Synopsys).         | ASIC/FPGA validation.             | [VCS](https://www.synopsys.com/verification/simulation/vcs.html) |  

### Specialized/Historical Tools  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **Spike**       | RISC-V ISA reference simulator.              | RISC-V software dev.              | [Spike](https://github.com/riscv-software-src/riscv-isa-sim) |  
| **SimpleScalar**| Classic CPU simulator (deprecated).          | Teaching pipeline basics.         | [Archive](http://www.simplescalar.com/) |  

---

## Benchmarks

Benchmark suites crucial for evaluating computer system performance, selected based on their relevance and widespread use in academic research and industry.

| Benchmark | Description | Use Case | Link |
|-----------|-------------|----------|------|
| **SPEC CPU2017** | Standard benchmark suite for CPU performance. | CPU performance evaluation. | [SPEC CPU2017](https://www.spec.org/cpu2017) |
| **PARSEC 3.0** | Benchmark suite for shared-memory computers. | Multicore research. | [PARSEC 3.0](http://parsec.cs.princeton.edu) |
| **SPLASH-2** | Shared-memory parallel programs. | Cache coherence and multicore studies. | [SPLASH-2](https://github.com/SakalisC/Splash-2) |
| **Rodinia v3.1** | Heterogeneous computing benchmark suite. | GPU and heterogeneous architectures. | [Rodinia v3.1](https://rodinia.cs.virginia.edu) |
| **MLPerf** | Industry-standard ML hardware benchmark suite. | AI accelerator and GPU evaluation. | [MLPerf](https://mlcommons.org/en/inference-datacenter/) |
| **MiBench** | Benchmark suite for embedded systems. | Embedded systems performance. | [MiBench](https://vhosts.eecs.umich.edu/mibench) |
| **NAS Parallel Benchmark 3.4.2** | High-performance computing benchmarks. | Parallel systems performance. | [NAS NPB](https://www.nas.nasa.gov/publications/npb.html) |
| **STREAM** | Measures memory bandwidth. | Memory system evaluation. | [STREAM](https://www.cs.virginia.edu/~stream) |
| **Graph500** | Graph-based workload benchmark. | Memory-bound and graph analytics research. | [Graph500](https://graph500.org/) |
| **PolyBench/C 4.2** | Kernel benchmark suite for compilers. | Compiler and performance optimization. | [PolyBench/C](https://sourceforge.net/p/polybench/home/HOME) |

---

## Tools for Research

Essential tools categorized for performance analysis, power measurement, design, and visualization.

| Category | Tool | Description | Link |
|----------|------|-------------|------|
| **Performance Analysis** | **Linux perf** | Profiling tool for Linux systems. | [Linux perf](https://perf.wiki.kernel.org/index.php/Tutorial) |
| | **Intel VTune** | Detailed performance analysis for Intel architectures. | [Intel VTune](https://www.intel.com/content/www/en-us/products/tools/performance-tools/vtune.html) |
| | **ARM Development Studio** | Performance tools for ARM architectures. | [ARM Studio](https://developer.arm.com/tools-and-software/embedded/embedded-tools/development-tools) |
| | **Valgrind / Cachegrind** | Memory profiling and cache simulation. | [Valgrind](https://valgrind.org/) |
| | **Intel Pin** | Dynamic binary instrumentation framework. | [Intel Pin](https://www.intel.com/content/www/en-us/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html) |
| **Power & Energy** | **McPAT** | Power, area, and timing modeling framework. | [McPAT](https://github.com/HewlettPackard/mcpat) |
| | **CACTI** | DRAM/SRAM cache power/area model. | [CACTI](https://github.com/HewlettPackard/cacti) |
| | **Wattch** | Power modeling integrated with cycle-level simulators. | [Wattch](http://www.eecs.harvard.edu/~dbrooks/wattch-form.html) |
| | **Intel Power Gadget** | Energy measurement tool for Intel processors. | [Power Gadget](https://www.intel.com/content/www/en-us/products/docs/processors/intel-core/intel-power-gadget.html) |
| **Design Language** | **Chisel** | Hardware construction language for custom processors. | [Chisel](https://chisel-lang.org) |
| | **Bluespec SystemVerilog** | High-level language for hardware design. | [Bluespec](https://bluespec.com/products/bluespec-systemverilog) |
| | **LLVM** | Compiler infrastructure widely used in arch research. | [LLVM](https://llvm.org/) |
| **Visualization** | **Flame Graphs** | Performance visualization tool. | [Flame Graphs](https://github.com/brendangregg/FlameGraph) |
| | **SpeedScope** | Web-based profiling data analysis tool. | [SpeedScope](https://www.speedscope.dev) |

---

## ISA References & Specs

Official specifications and reference manuals for major instruction set architectures.

| ISA | Description | Link |
|-----|-------------|------|
| **RISC-V Spec** | Official unprivileged and privileged ISA specifications. | [RISC-V Specs](https://github.com/riscv/riscv-isa-manual/releases) |
| **ARM Architecture Reference Manual** | Complete ARMv8/v9 ISA reference. | [ARM ARM](https://developer.arm.com/documentation/ddi0487/latest) |
| **Intel x86 Software Developer Manuals** | Full x86-64 ISA and microarchitecture reference. | [Intel SDM](https://www.intel.com/content/www/en-us/developer/articles/technical/intel-sdm.html) |
| **AMD64 Architecture Programmer's Manual** | AMD's x86-64 ISA reference. | [AMD APM](https://www.amd.com/en/support/tech-docs/amd64-architecture-programmers-manual-volumes-1-5) |
| **MIPS Architecture** | Classic MIPS ISA reference, useful for teaching. | [MIPS Docs](https://www.mips.com/products/architectures/) |

---

## Compilers & Binary Analysis

Tools for compiler research, binary instrumentation, and code generation — tightly coupled to architecture research.

| Tool | Description | Use Case | Link |
|------|-------------|----------|------|
| **LLVM** | Modular compiler infrastructure and IR framework. | Custom backends, pass development, arch-aware optimization. | [LLVM](https://llvm.org/) |
| **GCC** | GNU Compiler Collection with broad architecture support. | Cross-compilation and ISA-level code generation. | [GCC](https://gcc.gnu.org/) |
| **Intel Pin** | Dynamic binary instrumentation framework. | Trace generation, profiling, microarch analysis. | [Intel Pin](https://www.intel.com/content/www/en-us/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html) |
| **DynamoRIO** | Runtime code manipulation framework. | Dynamic analysis and custom instrumentation. | [DynamoRIO](https://dynamorio.org/) |
| **Valgrind** | Instrumentation framework for dynamic analysis. | Memory error detection, cache profiling (Cachegrind). | [Valgrind](https://valgrind.org/) |
| **Capstone** | Lightweight multi-architecture disassembly framework. | Binary analysis and reverse engineering. | [Capstone](https://www.capstone-engine.org/) |

---

## Traces & Datasets

Memory, branch, and instruction traces used as inputs for simulators and predictor research.

| Dataset | Description | Use Case | Link |
|---------|-------------|----------|------|
| **CVP-1 Traces** | Branch predictor traces from the Championship Value Prediction competition. | Branch prediction and value prediction research. | [CVP-1](https://www.microarch.org/cvp1/) |
| **CRC2 Traces** | Traces from the Cache Replacement Championship. | Cache replacement policy research. | [CRC2](https://crc2.ece.tamu.edu/) |
| **SPEC CPU Traces** | Instruction and memory traces derived from SPEC workloads. | Simulator input for cache/branch studies. | [Scarab Traces](https://github.com/hpsresearchgroup/scarab) |
| **DPC-3 Traces** | Traces from the Data Prefetching Championship. | Prefetcher design and evaluation. | [DPC-3](https://dpc3.compas.cs.stonybrook.edu/) |
| **ML Perf Inference Traces** | Inference workload traces for AI accelerator research. | LLM and DNN hardware evaluation. | [MLCommons](https://mlcommons.org/) |

---

## Tutorials

Online courses and specific guides for learning computer architecture, catering to both beginners and graduate researchers.

| Tutorial | Description | Link |
|----------|-------------|------|
| **Princeton Computer Architecture** | Comprehensive architecture course for graduate students (Coursera). | [Princeton Course](https://www.coursera.org/learn/comparch) |
| **Georgia Tech HPCA** | Advanced course on high-performance computer architecture (YouTube). | [Georgia Tech HPCA](https://www.youtube.com/playlist?list=PLAwxTw4SYaPmqpjgrmf4-DGlaeV0om4iP) |
| **MIT 6.004 Computation Structures** | Foundational digital design and architecture course (MIT OCW). | [MIT OCW](https://ocw.mit.edu/courses/6-004-computation-structures-spring-2017/) |
| **gem5 Tutorials** | Official tutorials for hands-on learning with the gem5 simulator. | [gem5 Learning](https://www.gem5.org/documentation/learning_gem5/introduction/) |
| **gem5 Bootcamp** | Recorded sessions from the official gem5 bootcamp. | [gem5 Bootcamp](https://www.youtube.com/@gem5simulator) |
| **RISC-V Tutorials** | Official learning resources for the open standard RISC-V ISA. | [RISC-V Learn](https://github.com/riscv/learn) |
| **David Patterson RISC-V Lectures** | Lectures by the co-inventor of RISC-V on modern ISA design. | [YouTube](https://www.youtube.com/results?search_query=david+patterson+risc-v) |
| **GPU Architecture Tutorial** | Detailed explanation of GPU architecture internals. | [GPU Tutorial](https://medium.com/codex/understanding-the-architecture-of-a-gpu-d5d2d2e8978b) |

---

## Cutting-Edge Research & Emerging Architectures

This section tracks tools and frameworks actively used in recent top-tier publications (ISCA, MICRO, HPCA, ASPLOS) to evaluate next-generation computing paradigms.

### AI & Large Language Model (LLM) Hardware
With the scaling of AI, research heavily focuses on spatial architectures, sparsity, and Transformer-specific optimizations.

| Framework/Tool | Description | Research Application | Link |
| :--- | :--- | :--- | :--- |
| **Accel-Sim** | Validated GPU simulator for modern workloads. | Evaluating tensor cores and deep learning workloads. | [Accel-Sim](https://github.com/accel-sim/accel-sim-framework) |
| **ASTRA-sim** | Distributed deep learning training simulator. | Modeling multi-GPU communication and network endpoints. | [ASTRA-sim](https://github.com/astra-sim/astra-sim) |
| **Sparseloop** | Analytical modeling for sparse tensor accelerators. | Exploring hardware exploitation of un-structured/structured sparsity. | [Sparseloop](https://github.com/mit-emesh/sparseloop) |
| **Timeloop + Accelergy**| Joint performance and energy modeling. | Full design-space exploration for AI chips and DNN accelerators. | [Accelergy](https://github.com/HewlettPackard/accelergy) |

### Advanced Packaging & Chiplets (2.5D/3D Integration)
As Moore's Law slows, multi-die systems connected via advanced packaging (e.g., UCIe) are dominating research.

| Tool | Description | Research Application | Link |
| :--- | :--- | :--- | :--- |
| **Booksim2** | Cycle-accurate network-on-chip (NoC) simulator. | Modeling Network-on-Interposer (NoI) and chiplet routing. | [Booksim2](https://github.com/booksim/booksim2) |
| **Garnet (gem5)** | Detailed NoC model integrated into gem5. | On-chip network design and evaluation. | [Garnet](https://www.gem5.org/documentation/general_docs/ruby/garnet-2/) |

### Memory Disaggregation & Processing-in-Memory (PIM)
Compute Express Link (CXL) and in-memory computing are reshaping the memory hierarchy.

| Tool/Standard | Description | Research Application | Link |
| :--- | :--- | :--- | :--- |
| **MQSim** | NVMe and SSD simulator. | Computational storage and near-data processing. | [MQSim](https://github.com/CMU-SAFARI/MQSim) |
| **Ramulator 2** | Modular DRAM simulator with CXL support. | Evaluating latency and bandwidth of tiered memory systems. | [Ramulator2](https://github.com/CMU-SAFARI/ramulator2) |
| **CXL Consortium** | Official CXL specification and resources. | Understanding CXL memory pooling and coherency protocols. | [CXL Consortium](https://www.computeexpresslink.org/) |
| **PIMulator** | Simulation framework for PIM architectures. | Near-data processing and PIM design exploration. | [PIMulator](https://github.com/CMU-SAFARI/pimulator) |

### Hardware Security & Confidential Computing
Protecting microarchitectures against transient execution attacks and side-channels.

| Tool | Description | Research Application | Link |
| :--- | :--- | :--- | :--- |
| **Revizor** | Microarchitectural fuzzing tool. | Detecting automated hardware information leaks (e.g., Spectre variants). | [Revizor](https://github.com/microsoft/revizor) |
| **SoftMC** | FPGA-based DRAM testing framework. | Discovering and mitigating Rowhammer vulnerabilities in DDR4/DDR5. | [SoftMC](https://github.com/CMU-SAFARI/SoftMC) |

---

## Elite Research Labs in Computer Architecture & Systems
Below is a non-exhaustive list of 20 highly influential research groups in computer architecture and closely related systems areas (e.g., accelerators, memory systems, datacenters, HW/SW co-design). These labs are well known for sustained, high-impact contributions in venues such as ISCA, MICRO, HPCA, and ASPLOS.

| University / Institution | Lab / Group Name | Key Focus Areas & Notes | Link |
| :--- | :--- | :--- | :--- |
| **ETH Zurich** | **SAFARI Research Group** | Processing-in-Memory (PIM), DRAM and NVM architectures, Rowhammer, memory controllers, storage systems, and bioinformatics acceleration. Highly influential across all major architecture venues. | [SAFARI](https://safari.ethz.ch/) |
| **Georgia Tech** | **Synergy Lab** | Deep learning accelerators, Networks-on-Chip (NoC), spatial architectures, HW/SW co-design, and performance modeling (e.g., MAESTRO, ASTRO-sim). | [Synergy](http://synergy.ece.gatech.edu/) |
| **UC Berkeley** | **ADEPT Lab** | RISC‑V ecosystem, agile hardware design, warehouse-scale computing, and open-source silicon tools such as Chisel and FireSim. | [ADEPT](https://adept.cs.berkeley.edu/) |
| **MIT** | **CSAIL – Computer Systems Group (CSG)** | Parallel architectures, spatial accelerators (Timeloop/Accelergy), cache coherence, secure hardware, and programmable architectures for ML and data analytics. | [MIT CSG](http://csg.csail.mit.edu/) |
| **UT Austin** | **HPS / LCA** | Core microarchitecture, branch prediction, cache and memory hierarchies, GPU memory systems, reliability, and performance modeling. | [UT Austin Arch](https://www.ece.utexas.edu/research/computer-architecture-and-embedded-systems) |
| **Univ. of Washington** | **Sampa** | Large-scale systems, approximate computing, DNA data storage, machine learning systems, and new computing substrates. | [Sampa](https://sampa.cs.washington.edu/) |
| **Univ. of Michigan** | **Computer Engineering (CE) Lab** | Secure and trustworthy hardware, in-memory computing (e.g., compute caches), energy-efficient architectures, and low-power embedded systems. | [UMich CE](https://ce.eecs.umich.edu/) |
| **UIUC** | **Computer Architecture Group** | Memory consistency models, high-performance and manycore architectures, hardware security, and parallel programming models. | [UIUC Arch](https://cs.illinois.edu/research/areas/architecture-compilers-and-parallel-computing) |
| **Cornell University** | **Computer Systems Laboratory (CSL)** | Hardware–software co-design, datacenter networking microarchitecture, secure enclaves, and scalable server architectures. | [Cornell CSL](https://csl.cornell.edu/) |
| **Stanford University** | **AHA (Agile Hardware) / MAST** | Domain-specific accelerators, CGRAs and reconfigurable fabrics, memory systems, and agile hardware design methodologies. | [Stanford AHA](https://aha.stanford.edu/) |
| **Univ. of Wisconsin–Madison** | **Vertical / Multifacet** | Classic and modern CPU microarchitecture, multiprocessors, memory systems, heterogeneous and GPU architectures. | [UW Arch](https://www.cs.wisc.edu/research/computer-architecture/) |
| **Princeton University** | **Princeton Parallel Group** | Manycore processor architectures (OpenPiton), scalable memory systems, datacenter and cloud architectures, and HW/SW co-design. | [Princeton Parallel](https://parallel.princeton.edu/) |
| **Univ. of Toronto** | **EcoSystem / CSNA** | Energy-efficient ML systems, neural accelerators, compression, GPU microarchitecture, and memory systems for AI workloads. | [EcoSystem](https://ecosystem.cs.toronto.edu/) |
| **EPFL** | **PARSA / EcoCloud** | Datacenter and cloud server architectures, rack-scale computing, energy-efficient computing, and hardware support for big data. | [EcoCloud](https://www.epfl.ch/research/domains/ecocloud/) |
| **UCLA** | **VAST Lab / CDSC** | Domain-specific computing, FPGA and heterogeneous acceleration, high-level synthesis, and automated design tools for ML hardware. | [VAST Lab](https://vast.cs.ucla.edu/) |
| **Carnegie Mellon University** | **Computer Architecture & Systems (various groups)** | Storage systems, non-volatile memories, accelerators, parallel systems, and operating systems/hardware co-design. | [CMU ECE Systems](https://www.ece.cmu.edu/research/computer-systems/index.html) |
| **University of Cambridge** | **Computer Architecture Group** | Manycore and interconnect architectures, memory systems, on-chip networks, and secure/low-power processor design. | [Cambridge Arch](https://www.cst.cam.ac.uk/research/themes/computer-architecture) |
| **Tsinghua University** | **Computer Architecture & Systems Groups** | High-performance processors, accelerators for AI and HPC, memory systems, and heterogeneous computing platforms. | [Tsinghua CS](https://www.cs.tsinghua.edu.cn/en/) |
| **University of Illinois (UIUC) – CSL** | **iCAN / IMPACT lineage** | Compiler–architecture co-design, vector/SIMD and accelerator architectures, domain-specific processors, and performance optimization. | [UIUC CSL](https://csl.illinois.edu/) |
| **University of Texas at Austin** | **Texas Systems Research Consortium (UT + partners)** | Large-scale systems, datacenter architecture, storage, and cloud-scale performance engineering, often in close collaboration with architecture groups. | [Texas Systems](https://www.cs.utexas.edu/research/computer-systems) |

> **Note:** This list is illustrative rather than exhaustive. It focuses on groups broadly recognized for sustained, high-impact work in computer architecture and closely related systems/accelerator research.

---

## Hall of Fame

To find the most influential researchers in the field, refer to the official Hall of Fame registries maintained by the top-tier conferences based on paper publication counts.

*   **[ISCA Hall of Fame](https://pages.cs.wisc.edu/~arch/www/iscahof.html)**: Recognizes authors with $8$ or more papers in the International Symposium on Computer Architecture.
*   **[MICRO Hall of Fame](https://www.microarch.org/hof/)**: Recognizes authors with $8$ or more papers in the International Symposium on Microarchitecture.
*   **[HPCA Hall of Fame](https://www.computer.org/communities/technical-committees/tcca/awards/hpca-hall-of-fame)**: Recognizes authors who have made significant contributions to HPCA over the years.

---

## How to Contribute

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to add new tools, benchmarks, or tutorials to this list.

## License
[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [aliyasoubi](https://github.com/aliyasoubi) has waived all copyright and related or neighboring rights to this work.
