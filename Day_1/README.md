# Day 1: Verilog RTL Design and Simulation

## Overview

Welcome to **Day 1 of my RTL Design and Synthesis learning journey**.

In this session, I explored the fundamentals of **Verilog HDL, digital circuit simulation, RTL verification, waveform analysis, and synthesis**.

The main objective was to understand how a digital circuit can be described using Verilog, verified through simulation and waveform analysis, and synthesized into a gate-level representation.

---

## Table of Contents

1. [Simulator, Design, and Testbench](#1-simulator-design-and-testbench)
2. [Getting Started with Icarus Verilog](#2-getting-started-with-icarus-verilog)
3. [Lab: 2-to-1 Multiplexer Simulation](#3-lab-2-to-1-multiplexer-simulation)
4. [Verilog Code Analysis](#4-verilog-code-analysis)
5. [Simulation and Waveform Verification](#5-simulation-and-waveform-verification)
6. [Introduction to Yosys and RTL Synthesis](#6-introduction-to-yosys-and-rtl-synthesis)
7. [Sky130 Standard Cell Library](#7-sky130-standard-cell-library)
8. [Technology Mapping](#8-technology-mapping)
9. [Results](#9-results)
10. [Summary](#10-summary)

---

# 1. Simulator, Design, and Testbench

## Simulator

A **simulator** is a software tool used to execute Verilog HDL code and verify the behavior of a digital circuit before implementing it on actual hardware.

Simulation helps identify functional errors at an early stage and verifies whether the circuit produces the expected output for different input conditions.

### Main Functions of a Simulator

- Executes Verilog HDL code
- Verifies circuit functionality
- Detects design errors
- Analyzes signal behavior
- Generates waveform files

---

## Design

The **design** is the Verilog module that represents the required digital circuit.

It defines:

- Input signals
- Output signals
- Internal logic
- Functional behavior of the circuit

For this experiment, the design is a **2-to-1 multiplexer**.

### Design Flow

```mermaid
flowchart LR
    A[Verilog RTL Design] --> B[Design Module]
    B --> C[Digital Circuit]
