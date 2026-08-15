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




# 3. Lab: 2-to-1 Multiplexer Simulation

A 2-to-1 multiplexer has:

- Two inputs: `i0` and `i1`
- One select signal: `sel`
- One output: `y`

The output is selected according to the select signal.

| Select | Output |
|--------|--------|
| 0 | i0 |
| 1 | i1 |

## Verilog Design

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
