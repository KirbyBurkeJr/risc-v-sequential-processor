
# RISC-V 32-Bit Sequential Processor

## Overview

![Processor diagram](https://github.com/KirbyBurkeJr/risc-v-sequential-processor/blob/main/doc/processor-diagram.png)

This repository contains the Verilog design source and simulation files for a 32-bit sequential RISC-V processor. For more information about this project, visit the [RISC-V Sequential Processor](https://kirbyburkejr.com/projects/risc-v-sequential-processor) page on my portfolio site.

## Features

This design includes a five-stage datapath and two additional control units that process a selection of RISC-V instructions.

### Five-Stage Datapath

![Datapath diagram](https://github.com/KirbyBurkeJr/risc-v-sequential-processor/blob/main/doc/datapath-diagram.png)

- Instruction Fetch (IF)
- Instruction Decode (ID)
- Execution (EX)
- Memory Access (MEM)
- Write Back (WB)

### Control Units

The Controller module manages memory and register read/write permissions and supports the ALU Controller module in selecting the appropriate ALU operation.

### RISC-V Instruction Set Architecture

This design supports the following 13 RISC-V instructions.

**R-Type (7)**
- Arithmetic: ADD & SUB
- Logical: AND, OR, & NOR
- Compare: SEQ & SLT

**I-Type (5)**
- ADDI
- ANDI
- ORI
- SLTI
- LW

**S-Type (1)**
- SW

## Directories

**docs/**
- datapath-diagram.png
- processor-diagram.png
- instruction-specifications.png

**src/design/**

- Processor.v
- 11 design files (dependencies)

**src/testbench/**

- tb_Processor.v

**sim/**
- example-tcl-output.txt
- tb_Processor_behav.png
- tb_Processor_behav.wcfg

## Instructions

### Cloning the Repository
```bash
git clone https://github.com/KirbyBurkeJr/risc-v-sequential-processor
cd risc-v-sequential-processor
```

### Running the Simulation

The simulation includes a sequence of tests for 20 instructions.

1. Open Vivado and create a new project.
2. Add the files in the `src/design/` and `src/testbench/` directories.
3. Run the simulation using the `tb_Processor.v` test bench file.

Simulation output includes a waveform diagram and Tcl output, including conditional alerts for specific instruction failures and a summary with the count of successful instructions.

## Documentation

Detailed block diagrams, including internal bus signals and port mapping:
- Processor (i.e., the parent container)
- Datapath, including stages and submodules

Tables with bit allocation for each instruction type.

### Tools Used

- [Vivado v2023.2 (64-bit)](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/2023-2.html) for Verilog module design and waveform generation.

## License
This project is licensed under the [MIT License](LICENSE).

## Contributing
Feel free to submit issues or pull requests to improve this project.
