# Day 1: Verilog RTL Design and Simulation

## Overview

Welcome to Day 1 of my RTL Design and Synthesis learning journey. In this session, I explored the fundamentals of Verilog HDL, digital circuit simulation, RTL verification, and synthesis.

The main objective was to understand how a digital circuit can be described using Verilog, verified using simulation and waveform analysis, and synthesized into a gate-level representation.

---

## Table of Contents

1. Simulator, Design and Testbench
2. Icarus Verilog
3. 2-to-1 Multiplexer Simulation
4. Verilog Code Analysis
5. Yosys and Synthesis
6. Sky130 Standard Cell Library
7. Results
8. Summary

---

# 1. Simulator, Design and Testbench

## Simulator

A simulator is a software tool used to execute Verilog code and verify the behavior of a digital circuit before hardware implementation.

## Design

The design is the Verilog module that represents the required digital circuit. It contains the inputs, outputs, and logic required for the circuit operation.
<img width="534" height="264" alt="image" src="https://github.com/user-attachments/assets/d9f1778c-bcbb-45b6-b045-c9ff882f0dc8" />


## Testbench

A testbench is a separate Verilog module used to provide different input combinations to the design and observe the outputs.

---<img width="1122" height="608" alt="image" src="https://github.com/user-attachments/assets/0f1fc68b-9038-4cd0-9730-e936dd03f71b" />

# 2 Getting Started with Icarus Verilog
What is Icarus Verilog?
Icarus Verilog is a free and open-source Verilog compiler and simulator. It allows users to compile Verilog source files, execute simulations, and generate waveform files for analyzing the behavior of digital circuits.

Basic Simulation Flow
<img width="1854" height="956" alt="image" src="https://github.com/user-attachments/assets/ef4b5969-0972-4d7a-a550-5c816ccc05fa" />

# 3 Lab: 2-to-1 Multiplexer Simulation
Installing the Required Tools
Install Icarus Verilog:

sudo apt install iverilog
Install GTKWave:

sudo apt install gtkwave
Compiling the Design
Compile the Verilog design and testbench:

iverilog good_mux.v tb_good_mux.v
Running the Simulation
Execute the compiled output file:

./a.out
Viewing the Waveform
Open the generated waveform using GTKWave:

gtkwave tb_good_mux.vcd
Simulation Result
The generated waveform verifies that the 2-to-1 multiplexer functions correctly. The output changes according to the select signal and follows the selected input.
<img width="1841" height="904" alt="image" src="https://github.com/user-attachments/assets/a2dc3159-ed40-4ac5-9b90-40f2159c6c8b" />

| Select | Output |
|--------|--------|
| 0 | i0 |
| 1 | i1 |

# 4 Verilog Design

A 2-to-1 multiplexer was designed using Verilog HDL.

- `i0` and `i1` are the two input signals.
- `sel` is the select signal.
- `y` is the output.
- When `sel = 0`, output `y` follows `i0`.
- When `sel = 1`, output `y` follows `i1`.

```verilog
module good_mux(
    input i0,
    input i1,
    input sel,
    output y
);

assign y = sel ? i1 : i0;

endmodule
```
# 5. Introduction to Yosys and Gate Libraries Theory
Yosys is an open-source synthesis tool that converts Verilog RTL descriptions into gate-level netlists. It analyzes and optimizes the design before mapping the logic to cells from a selected technology library.

A Liberty (.lib) file describes the characteristics of standard cells used by the technology. It contains information such as cell functionality, timing, area, power, and drive strength. Yosys uses this information during technology mapping to select suitable standard cells.

In this experiment, the good_mux design was synthesized using the Sky130 standard cell library. The RTL was processed, optimized, technology-mapped, and represented as a gate-level netlist.
# Synthesis Lab with Yosys
Step 1: Start Yosys
yosys
Step 2: Load the Liberty Library
read_liberty -lib /home/vsduser/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
Step 3: Load the Verilog Design
read_verilog /home/vsduser/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files/good_mux.v
Step 4: Run RTL Synthesis
synth -top good_mux
Step 5: Perform Technology Mapping
abc -liberty /home/vsduser/VLSI/sky130RTLDesignAndSynthesisWorkshop/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
Step 6: Display the Synthesized Design
show
<img width="1117" height="629" alt="image" src="https://github.com/user-attachments/assets/e7bf3450-d394-4b4e-bd06-b4a1d91f3a1d" />
# 6 Result
The good_mux Verilog design was synthesized successfully.
The Sky130 Liberty library was loaded for technology mapping.
The RTL logic was optimized during synthesis.
Technology mapping was performed using the selected Sky130 standard cells.
The resulting gate-level representation was generated and viewed using Yosys.

