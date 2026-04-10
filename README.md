# Awesome Computer Architecture [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Computer architecture resources, including simulators, benchmarks, tools, and tutorials for researchers, graduate students, and hardware engineers.

## Contents

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
  - [Performance Analysis](#performance-analysis)
  - [Power & Energy](#power--energy)
  - [Design Language](#design-language)
  - [Visualization](#visualization)
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

---

## Books

Essential reading materials for computer architecture, ranging from foundational concepts to advanced quantitative analysis.

- [CMOS VLSI Design: A Circuits & Systems Perspective](https://www.pearson.com/en-us/subject-catalog/p/cmos-vlsi-design-a-circuits-and-systems-perspective/P200000009477/9780321547743) - Fundamentals of CMOS technology, circuits, and VLSI chip design by Weste & Harris.
- [Computer Architecture: A Quantitative Approach](https://shop.elsevier.com/books/computer-architecture/hennessy/978-0-443-15406-5) - The definitive guide for graduate-level architecture by Hennessy & Patterson.
- [Computer Organization and Design (RISC-V Edition)](https://shop.elsevier.com/books/computer-organization-and-design-risc-v-edition/patterson/978-0-12-820331-6) - Best for undergraduate basics and RISC-V fundamentals by Patterson & Hennessy.
- [Digital Design and Computer Architecture](https://shop.elsevier.com/books/digital-design-and-computer-architecture/harris/978-0-12-394424-5) - Connecting logic gates to processor design by Harris & Harris.
- [Parallel Computer Architecture: A Hardware/Software Approach](https://shop.elsevier.com/books/parallel-computer-architecture/culler/978-1-55860-343-1) - The classic text on parallel computing and high-performance architecture by Culler, Singh, & Gupta.
- [Principles and Practices of Interconnection Networks](https://shop.elsevier.com/books/principles-and-practices-of-interconnection-networks/dally/978-0-12-200751-4) - Definitive guide on router architecture, topology, and routing by Dally & Towles.

## Conferences

The top-tier (Tier-1) academic conferences where the latest computer architecture research is published.

- [ASPLOS](https://www.asplos-conference.org) - Architectural Support for Programming Languages and OS; the intersection of hardware, OS, and compilers.
- [HPCA](https://hpca-conf.org) - International Symposium on High-Performance Computer Architecture; high-performance system design and analysis.
- [ISCA](https://iscaconf.org/) - International Symposium on Computer Architecture; the premier forum for new ideas in computer architecture.
- [MICRO](https://www.microarch.org/) - International Symposium on Microarchitecture; advanced microarchitecture and compiler techniques.

## Simulators

### CPU Simulators

- [ChampSim](https://github.com/ChampSim/ChampSim) - Trace-driven simulator for branch prediction and prefetching, considered a de-facto standard for ISCA/MICRO research.
- [gem5](https://www.gem5.org/) - Modular, open-source CPU/SoC simulator used for studying cache, branch prediction, and out-of-order CPUs.
- [MARSSx86](https://github.com/donggyukim/Marssx86) - Cycle-accurate x86 simulator for x86 microarchitecture analysis.
- [QEMU](https://www.qemu.org/) - Fast full-system emulator heavily used for OS and software prototyping.
- [Sniper](https://snipersim.org/) - Interval-based multicore simulator for large-scale CMP performance studies.
- [SST](https://sst-simulator.org/) - Parallel simulator for large-scale systems focusing on HPC/SoC co-design.
- [ZSim](https://github.com/s5z/zsim) - Fast, scalable x86-64 multicore simulator for cache hierarchy and NUCA research.

### GPU/Accelerator Simulators

- [Accel-Sim](https://github.com/accel-sim/accel-sim-framework) - Validated GPU simulator for modern workloads like tensor cores and deep learning workloads.
- [GPGPU-Sim](https://github.com/gpgpu-sim/gpgpu-sim_distribution) - Cycle-accurate NVIDIA GPU simulator for CUDA kernel analysis.
- [SCALE-Sim](https://github.com/ARM-software/SCALE-Sim) - Systolic array simulator for deep neural networks and TPU-like architectures.
- [STONNE](https://stonne-simulator.github.io) - is a cycle-level microarchitectural simulator for flexible DNN inference accelerators.
- [Timeloop](https://github.com/NVlabs/timeloop) - Deep learning accelerator modeling framework for energy and performance optimization.

### Memory System Simulators

- [DRAMSim3](https://github.com/umd-memsys/DRAMsim3) - Cycle-accurate DRAM simulator for DDRx and LPDDRx modeling.
- [MQSim](https://github.com/CMU-SAFARI/MQSim) - NVMe and SSD simulator for computational storage and near-data processing.
- [Ramulator](https://github.com/CMU-SAFARI/ramulator) - Supports HBM, GDDR, and emerging memories for memory controller design.
- [Ramulator 2](https://github.com/CMU-SAFARI/ramulator2) - Redesigned Ramulator with a cleaner, modular API for next-generation memory protocol research.

### Full-System/Cloud Simulators

- [FireSim](https://fires.im/) - FPGA-accelerated datacenter simulator for cloud hardware research.
- [Simics](https://www.intel.com/content/www/us/en/developer/articles/tool/simics-simulator.html) - Commercial full-system simulator for enterprise virtual prototyping.

### RTL/FPGA Simulators

- [VCS](https://www.synopsys.com/verification/simulation/vcs.html) - Commercial RTL simulator by Synopsys for ASIC/FPGA validation.
- [Verilator](https://www.veripool.org/verilator/) - Fast RTL-to-C++ simulator for pre-silicon verification.

### Specialized/Historical Tools

- [SimpleScalar](https://github.com/toddmaustin/simplesim-3.0) - Classic CPU simulator generally used for teaching pipeline basics.
- [Spike](https://github.com/riscv-software-src/riscv-isa-sim) - RISC-V ISA reference simulator for RISC-V software development.

## Benchmarks

Benchmark suites crucial for evaluating computer system performance, selected based on their relevance and widespread use in academic research and industry.

- [Graph500](https://graph500.org/) - Graph-based workload benchmark for memory-bound and graph analytics research.
- [MiBench](https://vhosts.eecs.umich.edu/mibench) - Benchmark suite for evaluating embedded systems performance.
- [MLPerf](https://mlcommons.org/en/inference-datacenter/) - Industry-standard ML hardware benchmark suite for AI accelerator and GPU evaluation.
- [NAS Parallel Benchmark 3.4.2](https://www.nas.nasa.gov/publications/npb.html) - High-performance computing benchmarks for parallel systems performance.
- [PARSEC 3.0](https://github.com/connorimes/parsec-3.0) - Benchmark suite for shared-memory computers, heavily used in multicore research.
- [PolyBench/C 4.2](https://sourceforge.net/p/polybench/home/HOME) - Kernel benchmark suite for compilers and performance optimization.
- [Rodinia v3.1](https://rodinia.cs.virginia.edu) - Heterogeneous computing benchmark suite for GPU and heterogeneous architectures.
- [SPEC CPU2017](https://www.spec.org/cpu2017) - Standard benchmark suite for comprehensive CPU performance evaluation.
- [SPLASH-3](https://github.com/SakalisC/Splash-3) - Shared-memory parallel programs for cache coherence and multicore studies.
- [STREAM](https://www.cs.virginia.edu/stream/) - Synthetic benchmark program that measures sustainable memory bandwidth.

## Tools for Research

Essential tools categorized for performance analysis, power measurement, design, and visualization.

### Performance Analysis

- [ARM Development Studio](https://www.arm.com/products/development-tools/embedded-and-software/arm-development-studio) - Performance tools for ARM architectures.
- [Intel VTune](https://www.intel.com/content/www/us/en/developer/tools/oneapi/vtune-profiler.html) - Detailed performance analysis for Intel architectures.
- [Linux perf](https://perfwiki.github.io/main/) - Profiling tool for Linux systems.

### Power & Energy

- [CACTI](https://github.com/HewlettPackard/cacti) - DRAM and SRAM cache power and area model.
- [ntel® PCM](https://github.com/intel/pcm) - Energy measurement tool for Intel processors.
- [McPAT](https://github.com/HewlettPackard/mcpat) - Power, area, and timing modeling framework.
- [Wattch](https://www.seas.upenn.edu/~leebcc/teachdir/ece299_fall10/Brooks00_Wattch.pdf) - Power modeling integrated with cycle-level simulators.

### Design Language

- [Bluespec SystemVerilog](https://github.com/mchanphilly/vscode-bsv) - High-level language for hardware design.
- [Chisel](https://chisel-lang.org) - Hardware construction language for custom processors.

### Visualization

- [Flame Graphs](https://github.com/brendangregg/FlameGraph) - Performance visualization tool.
- [SpeedScope](https://www.speedscope.app/) - Web-based profiling data analysis tool.

## ISA References & Specs

Official specifications and reference manuals for major instruction set architectures.

- [AMD64 Architecture Programmer's Manual](https://www.amd.com/en/support/tech-docs/amd64-architecture-programmers-manual-volumes-1-5) - AMD's x86-64 ISA reference.
- [ARM Architecture Reference Manual](https://developer.arm.com/documentation/ddi0487/latest) - Complete ARMv8/v9 ISA reference.
- [Intel x86 Software Developer Manuals](https://www.intel.com/content/www/en-us/developer/articles/technical/intel-sdm.html) - Full x86-64 ISA and microarchitecture reference.
- [MIPS Architecture](https://www.mips.com/products/architectures/) - Classic MIPS ISA reference, useful for teaching.
- [RISC-V Spec](https://github.com/riscv/riscv-isa-manual/releases) - Official unprivileged and privileged ISA specifications.

## Compilers & Binary Analysis

Tools for compiler research, binary instrumentation, and code generation.

- [Capstone](https://www.capstone-engine.org/) - Lightweight multi-architecture disassembly framework for binary analysis and reverse engineering.
- [DynamoRIO](https://dynamorio.org/) - Runtime code manipulation framework for dynamic analysis and custom instrumentation.
- [GCC](https://gcc.gnu.org/) - GNU Compiler Collection with broad architecture support for cross-compilation and ISA-level code generation.
- [Intel Pin](https://www.intel.com/content/www/us/en/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html) - Dynamic binary instrumentation framework for trace generation, profiling, and microarch analysis.
- [LLVM](https://llvm.org/) - Modular compiler infrastructure and IR framework for custom backends, pass development, and arch-aware optimization.
- [Valgrind](https://valgrind.org/) - Instrumentation framework for dynamic analysis, memory error detection, and cache profiling.

## Traces & Datasets

Memory, branch, and instruction traces used as inputs for simulators and predictor research.

- [CRC2 Traces](https://crc2.ece.tamu.edu/) - Traces from the Cache Replacement Championship for replacement policy research.
- [CVP-1 Traces](https://www.microarch.org/cvp1/) - Branch predictor traces from the Championship Value Prediction.
- [DPC-3 Traces](https://dpc3.compas.cs.stonybrook.edu/) - Traces from the Data Prefetching Championship for prefetcher design and evaluation.
- [MLPerf Inference Traces](https://mlcommons.org/) - Inference workload traces for AI accelerator research and LLM hardware evaluation.
- [SPEC CPU Traces](https://github.com/hpsresearchgroup/scarab) - Instruction and memory traces derived from SPEC workloads for simulator input.

## Tutorials

Online courses and specific guides for learning computer architecture, catering to both beginners and graduate researchers.

- [David Patterson RISC-V Lectures](https://www.youtube.com/results?search_query=david+patterson+risc-v) - Lectures by the co-inventor of RISC-V on modern ISA design.
- [gem5 Bootcamp](https://www.youtube.com/@gem5simulator) - Recorded sessions from the official gem5 bootcamp.
- [gem5 Tutorials](https://www.gem5.org/documentation/learning_gem5/introduction/) - Official tutorials for hands-on learning with the gem5 simulator.
- [Georgia Tech HPCA](https://www.youtube.com/playlist?list=PLAwxTw4SYaPmqpjgrmf4-DGlaeV0om4iP) - Advanced course on high-performance computer architecture.
- [GPU Architecture Tutorial](https://medium.com/codex/understanding-the-architecture-of-a-gpu-d5d2d2e8978b) - Detailed explanation of GPU architecture internals.
- [MIT 6.004 Computation Structures](https://ocw.mit.edu/courses/6-004-computation-structures-spring-2017/) - Foundational digital design and architecture course.
- [Princeton Computer Architecture](https://www.coursera.org/learn/comparch) - Comprehensive architecture course for graduate students.
- [RISC-V Tutorials](https://github.com/riscv/learn) - Official learning resources for the open standard RISC-V ISA.

## Cutting-Edge Research & Emerging Architectures

Tools and frameworks actively used in recent top-tier publications (ISCA, MICRO, HPCA, ASPLOS) to evaluate next-generation computing paradigms.

### AI & Large Language Model (LLM) Hardware

- [ASTRA-sim](https://github.com/astra-sim/astra-sim) - Distributed deep learning training simulator for modeling multi-GPU communication and network endpoints.
- [Sparseloop](https://github.com/Accelergy-Project/micro22-sparseloop-artifact) - Analytical modeling for sparse tensor accelerators exploring hardware exploitation of un-structured/structured sparsity.
- [Timeloop + Accelergy](https://github.com/Accelergy-Project/accelergy-timeloop-infrastructure) - Joint performance and energy modeling for full design-space exploration of AI chips and DNN accelerators.

### Advanced Packaging & Chiplets (2.5D/3D Integration)

- [Booksim2](https://github.com/booksim/booksim2) - Cycle-accurate network-on-chip (NoC) simulator for modeling Network-on-Interposer (NoI) and chiplet routing.
- [Garnet (gem5)](https://www.gem5.org/documentation/general_docs/ruby/garnet-2/) - Detailed NoC model integrated into gem5 for on-chip network design and evaluation.

### Memory Disaggregation & Processing-in-Memory (PIM)

- [CXL Consortium](https://www.computeexpresslink.org/) - Official CXL specification and resources for understanding CXL memory pooling and coherency protocols.
- [ZSim+Ramulator](https://github.com/CMU-SAFARI/ramulator-pim) -  Processing-in-Memory Simulation Framework.

### Hardware Security & Confidential Computing

- [Revizor](https://github.com/hw-sw-contracts/revizor) - Microarchitectural fuzzing tool for detecting automated hardware information leaks like Spectre variants.
- [SoftMC](https://github.com/CMU-SAFARI/SoftMC) - FPGA-based DRAM testing framework for discovering and mitigating Rowhammer vulnerabilities in DDR4/DDR5.

## Elite Research Labs in Computer Architecture & Systems

Below is a curated list of research groups with sustained, high-impact contributions in top-tier computer architecture and systems venues such as ISCA, MICRO, HPCA, and ASPLOS.

### Notable & Highly Influential Labs

- **[CMU CALCM – Computer Architecture Lab at Carnegie Mellon](https://calcm.ece.cmu.edu/)** - The primary architecture hub at CMU. Historically and currently elite in storage systems, non-volatile memories, accelerators, parallel processing, and HW/SW co-design.
- **[Georgia Tech MSL – Memory Systems Lab](https://msl.ece.gatech.edu/)** - *Led by Moinuddin Qureshi.* World-class research focusing on cache/memory hierarchies, scalable memory systems, secure architecture, and quantum computing architecture.
- **[UC Berkeley SLICE Lab](https://slice.eecs.berkeley.edu/)** - *Successor to the ADEPT Lab.* Focuses on open-source silicon ecosystems (RISC-V), agile hardware design methodologies, ML accelerators, and warehouse-scale computing.
- **[UIUC I-ACOMA Lab](http://iacoma.cs.uiuc.edu/)** - *Led by Josep Torrellas.* Renowned for work on extreme-scale architectures, parallel architectures, memory consistency models, and secure hardware.

### Core Elite Labs

- **[Cambridge Computer Architecture Group (CAG)](https://www.cst.cam.ac.uk/research/comparch)** - Specializes in manycore and interconnect architectures, memory systems, on-chip networks, and secure, low-power design.
- **[Cornell Computer Systems Laboratory (CSL)](https://www.csl.cornell.edu/)** - A powerhouse for HW/SW co-design, datacenter networking microarchitecture, secure enclaves, scalable servers, and agile hardware.
- **[EPFL PARSA / EcoCloud](https://parsa.epfl.ch/)** - Focuses on datacenter and cloud server architectures, rack-scale computing, energy-efficient computing, and hardware for big data.
- **[ETH Zürich SAFARI Research Group](https://safari.ethz.ch/)** - *Led by Onur Mutlu.* A highly prolific lab pioneering Processing-in-Memory (PIM), DRAM/NVM architectures, Rowhammer/hardware security, and bioinformatics acceleration.
- **[Georgia Tech Synergy Lab](http://synergy.ece.gatech.edu/)** - *Led by Tushar Krishna.* Leading research in deep learning accelerators, Network-on-Chip (NoC), spatial architectures, and AI performance modeling.
- **[MIT CSG – Computer Systems Group](http://csg.csail.mit.edu/)** - Highly influential in parallel architectures, spatial accelerators, cache coherence, secure hardware, and programmable ML hardware.
- **[Princeton Parallel Group](https://parallel.princeton.edu/)** - *Led by David Wentzlaff.* Known for manycore processors, scalable memory systems, datacenter/cloud architectures, and open-source hardware (e.g., OpenPiton).
- **[Stanford AHA – Agile Hardware Project](https://aha.stanford.edu/)** - Pushing the boundaries of domain-specific accelerators, CGRAs, reconfigurable fabrics, memory systems, and agile hardware design tooling.
- **[Tsinghua PACMAN Group](http://pacman.cs.tsinghua.edu.cn/)** - Focuses on high-performance processors, accelerators for AI and HPC, memory systems, and heterogeneous systems design.
- **[UCLA VAST Lab](https://vast.cs.ucla.edu/)** - *Led by Jason Cong.* Pioneers in domain-specific computing, FPGA/heterogeneous acceleration, High-Level Synthesis (HLS), and automated ML hardware design tools.
- **[University of Michigan – Computer Engineering Lab (CE)](https://ce.engin.umich.edu/)** - Home to multiple top PIs researching secure/trustworthy hardware, in-memory computing, energy-efficient architectures, and robust system design.
- **[University of Toronto – EECG](https://www.eecg.utoronto.ca/)** - Contains multiple elite sub-groups. Globally recognized for energy-efficient ML systems, GPU microarchitecture, FPGA design, and memory for AI.
- **[UT Austin LCA – Laboratory for Computer Architecture](https://lca.ece.utexas.edu/)** - Elite research in core CPU microarchitecture, branch prediction, cache/memory hierarchies, GPU memory systems, and hardware reliability.
- **[University of Washington – Sampa Lab](https://sampa.cs.washington.edu/)** - Cutting-edge work in large-scale systems, approximate computing, DNA data storage, ML systems, and novel hardware substrates.
- **[UW–Madison Computer Architecture](https://www.cs.wisc.edu/research/computer-architecture/)** - A historically legendary hub for architecture. Focuses on classic and modern CPU microarchitecture, memory consistency models, heterogeneous computing, and tool development (e.g., gem5).
- **[Harvard Architecture, Circuits, and Compilers Group](https://vlsiarch.eecs.harvard.edu)** - Renowned for pioneering work in power/thermal-efficient architectures, edge AI hardware accelerators, autonomous systems, and HW/SW co-design.
- **[Universitat Politècnica de Catalunya (UPC) DAC](https://www.ac.upc.edu/en)** - Deeply integrated with the Barcelona Supercomputing Center (BSC), conducting world-leading research in HPC, superscalar microarchitecture, vector processors, and memory systems.
- 
### Additional Elite Architecture & Systems Labs

- **[UC Berkeley BAR – Berkeley Architecture Research Group](https://bar.eecs.berkeley.edu/)** - Deeply influential in the RISC-V movement, vector architectures, out-of-order processor generators (BOOM), and SoC design tools.
- **[University of Edinburgh – ICSA](https://web.inf.ed.ac.uk/icsa)** - A leading European institute known for high-performance compilers, heterogeneous computing, low-power systems, and advanced microarchitecture.
- **[University of Manchester – APT Group](https://apt.cs.manchester.ac.uk/)** - Famous for the SpiNNaker project, neuromorphic computing, and massive-scale many-core systems.
- **[TU Delft – Computer Engineering Lab](https://ce.ewi.tudelft.nl/)** - Leading European research in quantum computing control microarchitecture, memristor-based computing, and edge AI accelerators.
- **[KAIST – Computer Architecture & Systems](https://cs.kaist.ac.kr/)** *(Navigate to Systems/Arch labs)* - A dominant force in Asia producing highly influential papers in NVM, SSD architectures, AI accelerators, and main memory systems.
- **[Seoul National University – Computer Architecture & Embedded Systems](https://cse.snu.ac.kr/)** *(Navigate to labs)* - World-class output in deep learning accelerators, GPU architectures, advanced memory structures, and hardware-software co-design.

## Hall of Fame

Official Hall of Fame registries maintained by the top-tier conferences based on paper publication counts.

- [HPCA Hall of Fame](https://ieeetcca.org/awards/hpca-hall-of-fame/) - Recognizes authors who have made significant contributions to HPCA over the years.
- [ISCA Hall of Fame](https://pages.cs.wisc.edu/~arch/www/iscabibhall.html) - Recognizes authors with 8 or more papers in the International Symposium on Computer Architecture.
- [MICRO Hall of Fame](https://www.sigmicro.org/awards/microhof.php) - Recognizes authors with 8 or more papers in the International Symposium on Microarchitecture.

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to add new tools, benchmarks, or tutorials to this list.
