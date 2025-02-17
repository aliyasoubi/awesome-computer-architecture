# [Awesome Computer Architecture](https://github.com/yourusername/awesome-computer-architecture) 
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

An open-source Computer Architecture repository designed for researchers and graduate students to learn, explore, and apply cutting-edge concepts in computer system design.

## Table of Contents
- [Introduction](#introduction)
- [Simulators](#simulators)
- [Benchmarks](#benchmarks)
- [Tools](#tools)
- [Tutorials](#tutorials)
- [How to Contribute](#how-to-contribute)
- [License](#license)

## Introduction

This repository provides a comprehensive list of resources related to computer architecture. It is intended for researchers and graduate students looking for simulators, benchmarks, tools, and tutorials in the field.

## CPU/SoC Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **gem5**        | Modular, open-source CPU/SoC simulator.      | Cache, branch prediction, OoO CPUs. | [gem5.org](https://www.gem5.org/) |  
| **QEMU**        | Fast full-system emulator.                   | OS/software prototyping.          | [qemu.org](https://www.qemu.org/) |  
| **SST**         | Parallel simulator for large-scale systems.  | HPC/SoC co-design.                | [sst-simulator.org](https://sst-simulator.org/) |  
| **MARSSx86**    | Cycle-accurate x86 simulator.                | x86 microarchitecture analysis.   | [marss86.org](https://marss86.org/) |  

---

## GPU/Accelerator Simulators  
| Simulator       | Description                                  | Use Case                          | Link |  
|-----------------|----------------------------------------------|-----------------------------------|------|  
| **GPGPU-Sim**   | Cycle-accurate NVIDIA GPU simulator.         | CUDA kernel analysis.             | [GPGPU-Sim](http://www.gpgpu-sim.org/) |  
| **Timeloop**    | DNN accelerator modeling framework.          | Energy/performance optimization.  | [Timeloop](https://github.com/NVlabs/timeloop) |  
| **SCALE-Sim**   | Systolic array simulator for DNNs.           | TPU-like architectures.           | [SCALE-Sim](https://github.com/ARM-software/SCALE-Sim) |  

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

*(Content to be added)*

## Tools

*(Content to be added)*

## Tutorials

*(Content to be added)*

## How to Contribute

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.