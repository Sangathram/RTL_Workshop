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

## Testbench

A testbench is a separate Verilog module used to provide different input combinations to the design and observe the outputs.

---

# 2. Icarus Verilog

Icarus Verilog is an open-source Verilog compiler and simulator. It is used to compile Verilog designs, execute simulations, and generate waveform files.

The basic simulation flow is:

**Verilog Design → Testbench → Compilation → Simulation → Waveform Analysis**

---

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

```verilog
module good_mux(
    input i0,
    input i1,
    input sel,
    output y
);

assign y = sel ? i1 : i0;

endmodule
