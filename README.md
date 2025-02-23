# [Awesome Computer Architecture](https://github.com/yourusername/awesome-computer-architecture) 
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

The open-source "Awesome Computer Architecture" repository has been enhanced by filling in the benchmarks, tools, and tutorials sections, ensuring it serves as a robust resource for researchers and graduate students. The updates include widely recognized benchmark suites, essential tools for performance analysis and design, and high-quality tutorials for learning computer architecture concepts.

## Table of Contents
- [Introduction](#introduction)
- [Simulators](#cpu-simulators)
- [Benchmarks](#benchmarks)
- [Tools](#tools-for-computer-architecture-research)
- [Tutorials](#tutorials)
- [How to Contribute](#how-to-contribute)
- [License](#license)

## Introduction

This repository provides a comprehensive list of resources related to computer architecture. It is intended for researchers and graduate students looking for simulators, benchmarks, tools, and tutorials in the field.

## CPU Simulators
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **gem5**        | Modular, open-source CPU/SoC simulator.      | Cache, branch prediction, OoO CPUs. | [gem5.org](https://www.gem5.org/) |  
| **QEMU**        | Fast full-system emulator.                   | OS/software prototyping.          | [qemu.org](https://www.qemu.org/) |  
| **SST**         | Parallel simulator for large-scale systems.  | HPC/SoC co-design.                | [sst-simulator.org](https://sst-simulator.org/) |  
| **MARSSx86**    | Cycle-accurate x86 simulator.                | x86 microarchitecture analysis.   | [marss86.org](https://marss86.org/) |  

---

## GPU/Accelerator Simulators

| Simulator  | Description | Use Case | Link |
|------------|------------|----------|------|
| **GPGPU-Sim**  | Cycle-accurate NVIDIA GPU simulator | CUDA kernel analysis | [GPGPU-Sim](https://github.com/gpgpu-sim/gpgpu-sim_distribution) |
| **Timeloop**   | Deep learning accelerator modeling framework | Energy/performance optimization | [Timeloop](https://github.com/NVlabs/timeloop) |
| **SCALE-Sim**  | Systolic array simulator for deep neural networks | TPU-like architectures | [SCALE-Sim](https://github.com/ARM-software/SCALE-Sim) |
| **STONNE**     | Cycle-level simulation framework for flexible deep learning inference accelerators | Design-space exploration for DL accelerators | [STONNE](https://github.com/CBL-ORNL/STONNE) |

---

## Memory System Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **DRAMSim3**    | Cycle-accurate DRAM simulator.               | DDRx/LPDDRx modeling.             | [DRAMSim3](https://github.com/umd-memsys/DRAMsim3) |  
| **Ramulator**   | Supports HBM, GDDR, and emerging memories.   | Memory controller design.         | [Ramulator](https://github.com/CMU-SAFARI/ramulator) |  

---

## Full-System/Cloud Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **FireSim**     | FPGA-accelerated datacenter simulator.       | Cloud hardware research.          | [FireSim](https://fires.im/) |  
| **Simics**      | Commercial full-system simulator.            | Enterprise virtual prototyping.   | [Simics](https://www.windriver.com/simics) |  

---

## Power/Energy Modeling  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **McPAT**       | Power/area/timing modeling framework.        | CPU/GPU power estimation.         | [McPAT](https://github.com/HewlettPackard/mcpat) |  
| **CACTI**       | DRAM/SRAM cache power/area model.            | Memory hierarchy optimization.    | [CACTI](https://github.com/HewlettPackard/cacti) |  

---

## RTL/FPGA Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **Verilator**   | Fast RTL-to-C++ simulator.                   | Pre-silicon verification.         | [Verilator](https://www.veripool.org/verilator/) |  
| **VCS**         | Commercial RTL simulator (Synopsys).         | ASIC/FPGA validation.             | [VCS](https://www.synopsys.com/verification/simulation/vcs.html) |  

---

## Specialized/Historical Tools  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **Spike**       | RISC-V ISA reference simulator.              | RISC-V software dev.              | [Spike](https://github.com/riscv-software-src/riscv-isa-sim) |  
| **SimpleScalar**| Classic CPU simulator (deprecated).          | Teaching pipeline basics.         | [Archive](http://www.simplescalar.com/) |  


---

## Benchmarks

This section lists benchmark suites crucial for evaluating computer system performance, particularly in architecture research. These are selected based on their relevance and widespread use in the field.

| Benchmark                      | Description                                      | Use Case                          | Link |
|--------------------------------|--------------------------------------------------|-----------------------------------|------|
| **SPEC CPU2017**               | Standard benchmark suite for CPU performance     | CPU performance evaluation        | [SPEC CPU2017](https://www.spec.org/cpu2017) |
| **PARSEC 3.0**                 | Benchmark suite for shared-memory computers      | Multicore research                | [PARSEC 3.0](http://parsec.cs.princeton.edu) |
| **Rodinia v3.1**               | Heterogeneous computing benchmark suite          | GPU and heterogeneous architectures | [Rodinia v3.1](https://rodinia.cs.virginia.edu) |
| **MiBench**                    | Benchmark suite for embedded systems             | Embedded systems performance      | [MiBench](https://vhosts.eecs.umich.edu/mibench) |
| **NAS Parallel Benchmark 3.4.2** | High-performance computing benchmarks            | Parallel systems performance      | [NAS Parallel Benchmark](https://www.nas.nasa.gov/publications/npb.html) |
| **STREAM**                     | Measures memory bandwidth                        | Memory system evaluation          | [STREAM](https://www.cs.virginia.edu/~stream) |
| **PolyBench/C 4.2**            | Kernel benchmark suite for performance and compiler optimization analysis | Compiler and performance optimization | [PolyBench/C 4.2](https://sourceforge.net/p/polybench/home/HOME) |

---

## Tools for Computer Architecture Research

This section includes essential tools categorized for **performance analysis, power measurement, design, and visualization**, ensuring clarity and ease of use.   
This process identified a survey paper from **IEEE Xplore** and a **GitHub repository** listing relevant resources.

### Tool Categories

| **Category**              | **Tool**                      | **Description**                                      | **Link**  |
|--------------------------|-----------------------------|------------------------------------------------------|-----------|
| **Performance Analysis**  | **Linux perf**              | Profiling tool for Linux systems                     | [Linux perf](https://perf.wiki.kernel.org/index.php/Tutorial) |
|                          | **Intel VTune**             | Detailed performance analysis for Intel architectures | [Intel VTune](https://www.intel.com/content/www/en-us/products/tools/performance-tools/vtune.html) |
|                          | **ARM Development Studio**  | Performance tools for ARM architectures              | [ARM Development Studio](https://developer.arm.com/tools-and-software/embedded/embedded-tools/development-tools) |
| **Power & Energy**        | **McPAT**                   | Power, area, and timing modeling framework           | [McPAT](http://www.hpl.hp.com/research/mcpat) |
|                          | **CACTI**                   | DRAM/SRAM cache power/area model                     | [CACTI](https://github.com/nvdimm/CACTI) |
|                          | **Intel Power Gadget**      | Energy measurement tool for Intel processors         | [Intel Power Gadget](https://www.intel.com/content/www/en-us/products/docs/processors/intel-core/intel-power-gadget.html) |
| **Design & Simulation**   | **Chisel**                  | Hardware construction language for custom processors | [Chisel](https://chisel-lang.org) |
|                          | **Bluespec SystemVerilog**  | Language for hardware design                         | [Bluespec SystemVerilog](https://bluespec.com/products/bluespec-systemverilog) |
|                          | **Verilator**               | Fast RTL-to-C++ simulator for verification          | [Verilator](https://www.verilator.org) |
| **Visualization**         | **Flame Graphs**            | Performance visualization tool                       | [Flame Graphs](https://github.com/brendangregg/FlameGraph) |
|                          | **SpeedScope**              | Profiling data analysis tool                         | [SpeedScope](https://www.speedscope.dev) |


## Tutorials

This section provides links to online courses and specific guides for learning computer architecture, catering to researchers and graduate students.

| Tutorial                            | Description                                                          | Link |
|-------------------------------------|----------------------------------------------------------------------|------|
| **Princeton Computer Architecture** | Comprehensive course on computer architecture for researchers and graduate students | [Princeton Computer Architecture](https://www.coursera.org/learn/comparch) |
| **Georgia Tech High Performance**   | Advanced course on high-performance computer architecture for researchers | [Georgia Tech High Performance](https://www.youtube.com/playlist?list=PLAwxTw4SYaPmqpjgrmf4-DGlaeV0om4iP) |
| **gem5 Tutorials**                  | Official tutorials for hands-on learning with the gem5 simulator    | [gem5 Tutorials](https://www.gem5.org/documentation/learning_gem5/introduction/) |
| **RISC-V Tutorials**                | Official learning resources for RISC-V architecture                 | [RISC-V Tutorials](https://github.com/riscv/learn) |
| **GPU Architecture Tutorial**       | Detailed explanation of GPU architecture for computer architecture students | [GPU Architecture Tutorial](https://medium.com/codex/understanding-the-architecture-of-a-gpu-d5d2d2e8978b) |



## How to Contribute

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.