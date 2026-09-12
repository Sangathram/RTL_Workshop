# Physical Design (PD) — VLSI / OpenLANE Workshop

## Overview

This repository contains the practical work, figures, and notes completed across all **five modules** of the Physical Design workshop. The workshop progresses from open-source EDA and the Sky130 PDK through synthesis, floorplanning, standard-cell design and characterization, timing analysis, clock-tree synthesis, power distribution, routing, and physical verification.

The repository preserves the supplied workshop terminology and organizes the work module-by-module. Each module contains its own `README.md` and `Images` directory.

## Modules Covered

### Module 1 — Inception of Open-Source EDA, OpenLANE and Sky130 PDK

Covers how computers communicate with hardware, SoC design, OpenLANE, the Sky130 PDK, open-source EDA tools, technology-specific and tool-specific concepts, the OpenLANE directory structure, RTL-to-GDS flow, design preparation, synthesis, gate-level netlist generation, synthesis-result review, and basic timing/clock parameters.

[Open Module 1 →](./Module%201/README.md)

### Module 2 — Good Floorplan vs Bad Floorplan and Introduction to Library Cells

Covers chip floorplanning considerations, utilization factor, aspect ratio, pre-placed cells, decoupling capacitors, power planning, pin placement, Magic floorplan inspection, library binding, placement optimization, RePlAce congestion-aware placement, standard-cell libraries, metal layers, cell-design/characterization flow, and general timing-characterization parameters.

[Open Module 2 →](./Module%202/README.md)

### Module 3 — Design Library Cell Using Magic Layout and ngspice Characterization

Covers CMOS inverter simulation and threshold analysis, SPICE deck creation, static and dynamic behavior, CMOS fabrication steps, Sky130 layers, standard-cell layout using Magic, pin configuration, SPICE extraction, model-file characterization, connectivity, and DRC-rule work.

[Open Module 3 →](./Module%203/README.md)

### Module 4 — Pre-Layout Timing Analysis and Importance of Good Clock Tree

Covers delay-table timing modelling, grid-to-track conversion, layout-to-LEF preparation, timing libraries, OpenSTA pre-layout analysis, SDC and clock creation, setup analysis, jitter and uncertainty, synthesis optimization, TritonCTS clock-tree synthesis, buffering/H-Tree concepts, crosstalk, shielding, and real-clock setup/hold analysis.

[Open Module 4 →](./Module%204/README.md)

### Module 5 — Final Steps for RTL2GDS Using TritonRoute and OpenSTA

Covers maze routing, DRC, power-distribution construction, power straps, global and detailed routing, TritonRoute configuration and features, route guides, inter-guide connectivity, intra-/inter-layer routing, routing topology, connectivity handling, post-route statistics/files, and final DRC-clean verification.

[Open Module 5 →](./Module%205/README.md)

## Overall Workshop Flow

```text
Open-Source EDA / Sky130 PDK
          ↓
     OpenLANE / RTL2GDS
          ↓
        Synthesis
          ↓
      Floorplanning
          ↓
Library Binding & Placement
          ↓
Standard-Cell Design / Characterization
          ↓
   Timing Modelling / OpenSTA
          ↓
Clock Tree Synthesis / TritonCTS
          ↓
 Real-Clock Setup & Hold Analysis
          ↓
   Power Distribution Network
          ↓
 Global Routing / Detailed Routing
          ↓
       TritonRoute
          ↓
       DRC / Verification
          ↓
      Post-Route Files
```

## Repository Structure

```text
Physical_Design_PD/
├── README.md
├── Module 1/
│   ├── README.md
│   └── Images/
├── Module 2/
│   ├── README.md
│   └── Images/
├── Module 3/
│   ├── README.md
│   └── Images/
├── Module 4/
│   ├── README.md
│   └── Images/
└── Module 5/
    ├── README.md
    └── Images/
```

## Tools and Technologies

- **OpenLANE / OpenLane** — RTL-to-GDS implementation flow
- **Sky130 PDK** — open-source process design kit and technology files
- **Magic** — layout viewing, extraction, and DRC-related work
- **ngspice** — SPICE simulation and inverter characterization
- **OpenSTA** — static timing analysis
- **TritonCTS** — clock-tree synthesis
- **TritonRoute** — routing
- **RePlAce** — congestion-aware placement
- **Linux / Ubuntu** — workshop environment
- **Standard-cell libraries** — library and physical-design views

## Overall Learning Outcomes

After completing the five modules, the practical work provides exposure to:

1. Open-source EDA and the role of a PDK in digital ASIC implementation.
2. The OpenLANE RTL-to-GDS flow and its major stages.
3. Synthesis and gate-level netlist generation.
4. Chip floorplanning, utilization, aspect ratio, power planning, and pin placement.
5. Library binding, standard-cell placement, placement optimization, and congestion awareness.
6. CMOS inverter SPICE simulation and standard-cell characterization.
7. CMOS fabrication concepts and Sky130 layout layers.
8. Magic layout, extraction, connectivity, and DRC.
9. Timing libraries, delay tables, setup/hold analysis, jitter, and uncertainty.
10. Clock-tree synthesis, buffering, H-Tree concepts, crosstalk, and shielding.
11. Power distribution, global/detail routing, TritonRoute, route guides, and connectivity.
12. Final physical verification, DRC-clean checking, and post-route outputs.

## Practical Evidence

Each module has a dedicated `Images` directory. The supplied Module 3, Module 4, and Module 5 figures have been placed into their respective directories.

The uploaded source package did **not** contain the binary image files for Modules 1 and 2; only their expected image names were available from the previous README. Therefore, the Module 1 and Module 2 `Images` directories are created and documented, but their missing source images have not been fabricated or replaced with unrelated figures.

## Source and Organization

The overall README uses the second uploaded README as the reference structure and expands it to represent the complete five-module workshop. The first uploaded README was used as the previous-work reference for Modules 1 and 2, including their existing topic/figure organization.
