# Physical Design (PD) — VLSI / OpenLANE Workshop

## Overview

This repository contains the practical work, figures, and notes completed across all **five modules** of the Physical Design workshop. The workshop progresses from open-source EDA and the Sky130 PDK through synthesis, floorplanning, standard-cell design and characterization, timing analysis, clock-tree synthesis, power distribution, routing, and physical verification.

The repository follows the structure and terminology of the supplied **README (2)** as the reference for the complete workshop, while the earlier README was used to preserve and update the Module 1 and Module 2 organization. The complete supplied figure sets are included in the corresponding `Images` folders.

## Modules Covered

### Module 1 — Inception of Open-Source EDA, OpenLANE and Sky130 PDK

Covers how to talk to computers, SoC design, OpenLANE, Sky130 PDK, open-source EDA tools, technology/tool-specific concepts, RTL-to-GDS flow, synthesis, netlist generation, chip-area information, and clock parameters.

[Open Module 1 →](./Module%201/README.md)

### Module 2 — Good Floorplan vs Bad Floorplan and Introduction to Library Cells

Covers chip floorplanning, utilization factor, aspect ratio, cell design and characterization flows, timing-characterization parameters, Magic floorplan/placement views, standard-cell placement, Sky130 library information, metal layers, and synthesis-netlist inspection.

[Open Module 2 →](./Module%202/README.md)

### Module 3 — Design Library Cell Using Magic Layout and ngspice Characterization

Covers CMOS inverter simulation, threshold/VTC analysis, SPICE decks and waveforms, CMOS fabrication steps, Sky130 layers, standard-cell layout, pin configuration, extraction, connectivity, and verification.

[Open Module 3 →](./Module%203/README.md)

### Module 4 — Pre-Layout Timing Analysis and Importance of Good Clock Tree

Covers timing modelling, grid/track conversion, cell characterization, SDC, clock creation, OpenSTA pre-layout analysis, setup analysis, synthesis optimization, clock-tree synthesis, buffering, crosstalk, shielding, leakage power, and physical timing views.

[Open Module 4 →](./Module%204/README.md)

### Module 5 — Final Steps for RTL2GDS Using TritonRoute and OpenSTA

Covers maze routing, DRC, power distribution, straps, global/detail routing, TritonRoute, route guides, connectivity, routing topology, macro/RAM views, routing statistics, and post-route verification.

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
│       └── Module 1 figures
├── Module 2/
│   ├── README.md
│   └── Images/
│       └── Module 2 figures
├── Module 3/
│   ├── README.md
│   └── Images/
│       └── Module 3 figures
├── Module 4/
│   ├── README.md
│   └── Images/
│       └── Module 4 figures
└── Module 5/
    ├── README.md
    └── Images/
        └── Module 5 figures
```

## Tools and Technologies

- **OpenLANE / OpenLane** — RTL-to-GDS implementation flow
- **Sky130 PDK** — open-source process design kit
- **Magic** — layout viewing, extraction, and physical verification
- **ngspice** — SPICE simulation and characterization
- **OpenSTA** — static timing analysis
- **TritonCTS** — clock-tree synthesis
- **TritonRoute** — routing
- **RePlAce** — placement
- **Linux / Ubuntu** — workshop environment
- **Standard-cell libraries** — library and physical-design views

## Overall Learning Outcomes

After completing the five modules, the practical work provides exposure to:

1. Open-source EDA and the role of a PDK in ASIC design.
2. OpenLANE RTL-to-GDS flow and its major stages.
3. Synthesis and gate-level netlist generation.
4. Floorplanning, utilization, aspect ratio, power and pin planning.
5. Standard-cell libraries, placement and physical layout views.
6. CMOS inverter SPICE simulation and characterization.
7. CMOS fabrication concepts and Sky130 layers.
8. Magic layout, extraction, connectivity and DRC.
9. Timing libraries, setup/hold analysis, jitter and uncertainty.
10. Clock-tree synthesis, buffering, crosstalk and shielding.
11. Power distribution, global/detail routing and TritonRoute.
12. Route-guide and connectivity handling.
13. Final physical verification and post-route outputs.

## Practical Evidence

Every module now contains an `Images` directory with the actual image files supplied in the uploaded Module 1–2 and Module 3–5 archives. Each module README links directly to its figures.

## Reference

The overall organization and five-module coverage are based on the supplied README (2), while the previous README (1) was used as the reference for the existing Module 1 and Module 2 work. The supplied figure archives were used directly for the image folders.
