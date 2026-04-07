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
- [Computer Architecture: A Quantitative Approach](https://store.elsevier.com/eu/book/9780128119051/computer-architecture) - The definitive guide for graduate-level architecture by Hennessy & Patterson.
- [Computer Organization and Design (RISC-V Edition)](https://store.elsevier.com/eu/book/9780128203316/computer-organization-and-design-risc-v-edition) - Best for undergraduate basics and RISC-V fundamentals by Patterson & Hennessy.
- [Digital Design and Computer Architecture](https://store.elsevier.com/eu/book/9780123944245/digital-design-and-computer-architecture) - Connecting logic gates to processor design by Harris & Harris.
- [Modern Processor Design](https://www.waveland.com/browse.php?t=384) - Deep dive into superscalar processor microarchitecture by Shen & Lipasti.
- [Parallel Computer Architecture: A Hardware/Software Approach](https://store.elsevier.com/eu/book/9781558603431/parallel-computer-architecture) - The classic text on parallel computing and high-performance architecture by Culler, Singh, & Gupta.
- [Principles and Practices of Interconnection Networks](https://store.elsevier.com/eu/book/9780122007514/principles-and-practices-of-interconnection-networks) - Definitive guide on router architecture, topology, and routing by Dally & Towles.

## Conferences

The top-tier (Tier-1) academic conferences where the latest computer architecture research is published.

- [ASPLOS](https://www.sigarch.org/events/asplos/) - Architectural Support for Programming Languages and OS; the intersection of hardware, OS, and compilers.
- [HPCA](https://www.computer.org/communities/technical-committees/tcca) - International Symposium on High-Performance Computer Architecture; high-performance system design and analysis.
- [ISCA](https://www.sigarch.org/events/isca/) - International Symposium on Computer Architecture; the premier forum for new ideas in computer architecture.
- [MICRO](https://www.microarch.org/) - International Symposium on Microarchitecture; advanced microarchitecture and compiler techniques.

## Simulators

### CPU Simulators

- [ChampSim](https://github.com/ChampSim/ChampSim) - Trace-driven simulator for branch prediction and prefetching, considered a de-facto standard for ISCA/MICRO research.
- [gem5](https://www.gem5.org/) - Modular, open-source CPU/SoC simulator used for studying cache, branch prediction, and out-of-order CPUs.
- [MARSSx86](https://marss86.org/) - Cycle-accurate x86 simulator for x86 microarchitecture analysis.
- [QEMU](https://www.qemu.org/) - Fast full-system emulator heavily used for OS and software prototyping.
- [Sniper](https://snipersim.org/) - Interval-based multicore simulator for large-scale CMP performance studies.
- [SST](https://sst-simulator.org/) - Parallel simulator for large-scale systems focusing on HPC/SoC co-design.
- [ZSim](https://github.com/s5z/zsim) - Fast, scalable x86-64 multicore simulator for cache hierarchy and NUCA research.

### GPU/Accelerator Simulators

- [Accel-Sim](https://github.com/accel-sim/accel-sim-framework) - Validated GPU simulator for modern workloads like tensor cores and deep learning workloads.
- [GPGPU-Sim](https://github.com/gpgpu-sim/gpgpu-sim_distribution) - Cycle-accurate NVIDIA GPU simulator for CUDA kernel analysis.
- [SCALE-Sim](https://github.com/ARM-software/SCALE-Sim) - Systolic array simulator for deep neural networks and TPU-like architectures.
- [STONNE](https://github.com/stonne-sim/stonne) - Cycle-level simulation framework for DL inference and design-space exploration for DL accelerators.
- [Timeloop](https://github.com/NVlabs/timeloop) - Deep learning accelerator modeling framework for energy and performance optimization.

### Memory System Simulators

- [DRAMSim3](https://github.com/umd-memsys/DRAMsim3) - Cycle-accurate DRAM simulator for DDRx and LPDDRx modeling.
- [MQSim](https://github.com/CMU-SAFARI/MQSim) - NVMe and SSD simulator for computational storage and near-data processing.
- [Ramulator](https://github.com/CMU-SAFARI/ramulator) - Supports HBM, GDDR, and emerging memories for memory controller design.
- [Ramulator 2](https://github.com/CMU-SAFARI/ramulator2) - Redesigned Ramulator with a cleaner, modular API for next-generation memory protocol research.

### Full-System/Cloud Simulators

- [FireSim](https://fires.im/) - FPGA-accelerated datacenter simulator for cloud hardware research.
- [Simics](https://www.windriver.com/simics) - Commercial full-system simulator for enterprise virtual prototyping.

### RTL/FPGA Simulators

- [VCS](https://www.synopsys.com/verification/simulation/vcs.html) - Commercial RTL simulator by Synopsys for ASIC/FPGA validation.
- [Verilator](https://www.veripool.org/verilator/) - Fast RTL-to-C++ simulator for pre-silicon verification.

### Specialized/Historical Tools

- [SimpleScalar](http://www.simplescalar.com/) - Classic CPU simulator generally used for teaching pipeline basics.
- [Spike](https://github.com/riscv-software-src/riscv-isa-sim) - RISC-V ISA reference simulator for RISC-V software development.

## Benchmarks

Benchmark suites crucial for evaluating computer system performance, selected based on their relevance and widespread use in academic research and industry.

- [Graph500](https://graph500.org/) - Graph-based workload benchmark for memory-bound and graph analytics research.
- [MiBench](https://vhosts.eecs.umich.edu/mibench) - Benchmark suite for evaluating embedded systems performance.
- [MLPerf](https://mlcommons.org/en/inference-datacenter/) - Industry-standard ML hardware benchmark suite for AI accelerator and GPU evaluation.
- [NAS Parallel Benchmark 3.4.2](https://www.nas.nasa.gov/publications/npb.html) - High-performance computing benchmarks for parallel systems performance.
- [PARSEC 3.0](http://parsec.cs.princeton.edu) - Benchmark suite for shared-memory computers, heavily used in multicore research.
- [PolyBench/C 4.2](https://sourceforge.net/p/polybench/home/HOME) - Kernel benchmark suite for compilers and performance optimization.
- [Rodinia v3.1](https://rodinia.cs.virginia.edu) - Heterogeneous computing benchmark suite for GPU and heterogeneous architectures.
- [SPEC CPU2017](https://www.spec.org/cpu2017) - Standard benchmark suite for comprehensive CPU performance evaluation.
- [SPLASH-2](https://github.com/SakalisC/Splash-2) - Shared-memory parallel programs for cache coherence and multicore studies.
- [STREAM](https://www.cs.virginia.edu/~stream) - Synthetic benchmark program that measures sustainable memory bandwidth.

## Tools for Research

Essential tools categorized for performance analysis, power measurement, design, and visualization.

### Performance Analysis

- [ARM Development Studio](https://developer.arm.com/tools-and-software/embedded/embedded-tools/development-tools) - Performance tools for ARM architectures.
- [Intel VTune](https://www.intel.com/content/www/en-us/products/tools/performance-tools/vtune.html) - Detailed performance analysis for Intel architectures.
- [Linux perf](https://perf.wiki.kernel.org/index.php/Tutorial) - Profiling tool for Linux systems.

### Power & Energy

- [CACTI](https://github.com/HewlettPackard/cacti) - DRAM and SRAM cache power and area model.
- [Intel Power Gadget](https://www.intel.com/content/www/en-us/products/docs/processors/intel-core/intel-power-gadget.html) - Energy measurement tool for Intel processors.
- [McPAT](https://github.com/HewlettPackard/mcpat) - Power, area, and timing modeling framework.
- [Wattch](http://www.eecs.harvard.edu/~dbrooks/wattch-form.html) - Power modeling integrated with cycle-level simulators.

### Design Language

- [Bluespec SystemVerilog](https://bluespec.com/products/bluespec-systemverilog) - High-level language for hardware design.
- [Chisel](https://chisel-lang.org) - Hardware construction language for custom processors.

### Visualization

- [Flame Graphs](https://github.com/brendangregg/FlameGraph) - Performance visualization tool.
- [SpeedScope](https://www.speedscope.dev) - Web-based profiling data analysis tool.

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
- [Intel Pin](https://www.intel.com/content/www/en-us/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html) - Dynamic binary instrumentation framework for trace generation, profiling, and microarch analysis.
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
- [Sparseloop](https://github.com/mit-emesh/sparseloop) - Analytical modeling for sparse tensor accelerators exploring hardware exploitation of un-structured/structured sparsity.
- [Timeloop + Accelergy](https://github.com/HewlettPackard/accelergy) - Joint performance and energy modeling for full design-space exploration of AI chips and DNN accelerators.

### Advanced Packaging & Chiplets (2.5D/3D Integration)

- [Booksim2](https://github.com/booksim/booksim2) - Cycle-accurate network-on-chip (NoC) simulator for modeling Network-on-Interposer (NoI) and chiplet routing.
- [Garnet (gem5)](https://www.gem5.org/documentation/general_docs/ruby/garnet-2/) - Detailed NoC model integrated into gem5 for on-chip network design and evaluation.

### Memory Disaggregation & Processing-in-Memory (PIM)

- [CXL Consortium](https://www.computeexpresslink.org/) - Official CXL specification and resources for understanding CXL memory pooling and coherency protocols.
- [PIMulator](https://github.com/CMU-SAFARI/pimulator) - Simulation framework for near-data processing and PIM design exploration.

### Hardware Security & Confidential Computing

- [Revizor](https://github.com/microsoft/revizor) - Microarchitectural fuzzing tool for detecting automated hardware information leaks like Spectre variants.
- [SoftMC](https://github.com/CMU-SAFARI/SoftMC) - FPGA-based DRAM testing framework for discovering and mitigating Rowhammer vulnerabilities in DDR4/DDR5.

## Elite Research Labs in Computer Architecture & Systems

Highly influential research groups well known for sustained, high-impact contributions in venues such as ISCA, MICRO, HPCA, and ASPLOS.

- [Cambridge Arch Group](https://www.cst.cam.ac.uk/research/themes/computer-architecture) - Manycore/interconnect architectures, memory systems, on-chip networks, secure/low-power design.
- [CMU ECE Systems](https://www.ece.cmu.edu/research/computer-systems/index.html) - Storage systems, non-volatile memories, accelerators, parallel systems, and operating systems/hardware co-design.
- [Cornell CSL](https://csl.cornell.edu/) - HW/SW co-design, datacenter networking microarchitecture, secure enclaves, scalable servers.
- [EPFL EcoCloud](https://www.epfl.ch/research/domains/ecocloud/) - Datacenter/cloud servers, rack-scale computing, energy-efficient computing, big data HW.
- [ETH Zurich SAFARI](https://safari.ethz.ch/) - PIM, DRAM/NVM architectures, Rowhammer, memory controllers, storage systems, bioinformatics.
- [Georgia Tech Synergy Lab](http://synergy.ece.gatech.edu/) - Deep learning accelerators, NoC, spatial architectures, HW/SW co-design, performance modeling.
- [MIT CSG](http://csg.csail.mit.edu/) - Parallel architectures, spatial accelerators, cache coherence, secure HW, programmable ML HW.
- [Princeton Parallel Group](https://parallel.princeton.edu/) - Manycore processors, scalable memory systems, datacenter/cloud architectures, HW/SW co-design.
- [Stanford AHA](https://aha.stanford.edu/) - Domain-specific accelerators, CGRAs, reconfigurable fabrics, memory systems, agile HW design.
- [Tsinghua CS](https://www.cs.tsinghua.edu.cn/en/) - High-performance processors, accelerators for AI and HPC, memory systems, heterogeneous systems.
- [UC Berkeley ADEPT Lab](https://adept.cs.berkeley.edu/) - RISC-V ecosystem, agile HW design, warehouse-scale computing, open-source silicon tools.
- [UCLA VAST Lab](https://vast.cs.ucla.edu/) - Domain-specific computing, FPGA/heterogeneous acceleration, HLS, automated ML HW design tools.
- [UIUC Architecture](https://cs.illinois.edu/research/areas/architecture-compilers-and-parallel-computing) - Memory consistency, high-performance/manycore architectures, HW security, parallel programming.
- [UMich CE Lab](https://ce.eecs.umich.edu/) - Secure/trustworthy HW, in-memory computing, energy-efficient architectures, embedded systems.
- [Univ. of Toronto EcoSystem](https://ecosystem.cs.toronto.edu/) - Energy-efficient ML systems, neural accelerators, compression, GPU microarch, memory for AI.
- [UT Austin Arch](https://www.ece.utexas.edu/research/computer-architecture-and-embedded-systems) - Core microarch, branch prediction, cache/memory hierarchies, GPU memory systems, reliability.
- [UW Sampa](https://sampa.cs.washington.edu/) - Large-scale systems, approximate computing, DNA data storage, ML systems, new HW substrates.
- [UW-Madison Arch](https://www.cs.wisc.edu/research/computer-architecture/) - Classic/modern CPU microarch, multiprocessors, memory systems, heterogeneous/GPU architectures.

## Hall of Fame

Official Hall of Fame registries maintained by the top-tier conferences based on paper publication counts.

- [HPCA Hall of Fame](https://www.computer.org/communities/technical-committees/tcca/awards/hpca-hall-of-fame) - Recognizes authors who have made significant contributions to HPCA over the years.
- [ISCA Hall of Fame](https://pages.cs.wisc.edu/~arch/www/iscahof.html) - Recognizes authors with 8 or more papers in the International Symposium on Computer Architecture.
- [MICRO Hall of Fame](https://www.microarch.org/hof/) - Recognizes authors with 8 or more papers in the International Symposium on Microarchitecture.

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to add new tools, benchmarks, or tutorials to this list.
