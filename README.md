# 8-Bit CPU Design on FPGA 🖥️🔧
*A custom 8-bit CPU datapath and controller implemented in VHDL and deployed to an FPGA board.*

## Overview
This project implements a simple **8-bit CPU** using VHDL (with some Verilog testbenches), integrating datapath components, an ALU, and a finite-state machine (FSM) controller.  
The design was developed and simulated in **ModelSim**, synthesized in **Altera Quartus**, and deployed to an FPGA development board.  
Outputs are displayed on **7-segment displays** for validation.

## Features
- **Datapath design:** ALU, registers, instruction decoder, program counter, and memory interface (see `individual_files/`)
- **FSM controller:** sequences instruction fetch, decode, and execution cycles (see `machine.vhd`)
- **VHDL modules:** modular design for ALU, registers, decoder, and display
- **Simulation:** ModelSim testbenches and waveform files (`*.vwf`) for functional and timing verification
- **FPGA deployment:** synthesized with Altera Quartus and validated on hardware
- **7-segment output:** results and instructions displayed for live demo
- **Debug-first workflow:** iterative simulation and waveform inspection before hardware synthesis

## Tech Stack
- **Languages:** VHDL (primary), Verilog (testbenches)
- **Simulation:** ModelSim
- **Synthesis:** Altera Quartus
- **Hardware:** Intel/Altera FPGA board with 7-segment displays
- **Tools:** Quartus project files (`Lab6.qpf`, `Lab6.qsf`), ModelSim testbenches, waveform debugging

## Repository Contents
- `individual_files/` — All VHDL source files, block symbol files, and waveform files
- `output_files/` — Quartus build outputs, reports, and programming files
- `simulation/` — ModelSim and Quartus simulation outputs
- `db/`, `incremental_db/` — Quartus project and incremental compilation data
- `README.md` — Project overview and instructions

## How It Works
1. Instructions are fetched from memory and decoded by the FSM controller (`machine.vhd`).
2. The datapath executes instructions using the ALU (`ALU_unit*.vhd`), registers (`reg*.vhd`), and control signals.
3. Simulation in ModelSim validates logic and timing with waveform files (`*.vwf`).
4. Design is synthesized in Quartus and deployed to FPGA.
5. CPU results are shown on the board’s **7-segment displays** (`sseg.vhd`, `ssegALU3.vhd`).

## Images & Diagrams
<img width="1390" height="434" alt="image" src="https://github.com/user-attachments/assets/497badae-dcdd-4177-bf4c-72ba57e6e80e" />
<img width="1353" height="408" alt="image" src="https://github.com/user-attachments/assets/850f6973-3ebe-48b3-8848-53b52e87c24e" />


## Results
- Successfully integrated CPU datapath and FSM controller in VHDL
- Verified with **self-checking testbenches** and waveform debugging
- Deployed to FPGA with functioning **7-segment outputs**
- Demonstrated system-level integration of multiple RTL blocks

---
