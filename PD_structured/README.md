# Physical Design Workshop – OpenLANE & Sky130

This repository contains the practical work completed during the **Physical Design workshop** using the open-source EDA flow and Sky130 technology.

The work is organized into two modules:

- **Module 1:** Inception of Open-Source EDA, OpenLANE and Sky130 PDK
- **Module 2:** Good Floorplan vs Bad Floorplan and Introduction to Library Cells

## Repository Structure

```text
PD/
├── README.md
│
├── Module 1/
│   ├── README.md
│   └── images/
│       ├── openlane.png
│       ├── layer.png
│       ├── specific_to_tools.png
│       ├── specific_to_technology.png
│       ├── chip_area.png
│       ├── default_clock_period.png
│       └── clock_ratio_percentage.png
│
└── Module 2/
    ├── README.md
    └── images/
        ├── design_name.png
        ├── floorplan.png
        ├── magic_floorplan.png
        ├── magic_placement.png
        ├── magic_placement_zoom_out.png
        ├── standard_cell_placement.png
        ├── selected_mask_layer_metal2.png
        ├── selected_mask_layer_metal3.png
        ├── sky130_library.png
        └── synthesis_netlist.png
```

## Module 1 – Open-Source EDA, OpenLANE and Sky130

The first module introduces the fundamentals of digital hardware design, the interaction between computers and hardware-design tools, SoC design, OpenLANE and the Sky130 PDK.

### Topics Covered

1. **How to Talk to Computers**
2. **SoC Design and OpenLANE**
3. **Getting Familiar with Open-Source EDA Tools**
4. OpenLANE and the Sky130 PDK
5. Technology-specific and tool-specific concepts
6. Basic design parameters such as chip area and clock settings

### Practical Work

The practical screenshots include OpenLANE-related work, technology/tool-specific information, layer information, chip-area information and clock parameters.

## Module 2 – Floorplanning and Library Cells

The second module focuses on floorplanning, placement and an introduction to standard-cell libraries and physical design views.

### Topics Covered

1. **SKY130_D2_SK1 – Chip Floorplanning Considerations**
2. **SKY_L1 – Utilization Factor and Aspect Ratio**
3. **Cell Design and Characterization Flows**
4. **General Timing Characterization Parameters**
5. Floorplan and placement visualization
6. Introduction to Sky130 library cells and physical layers

### Practical Work

The screenshots document the design name, floorplan, Magic floorplan/placement views, standard-cell placement, Sky130 library information, selected metal layers and the synthesized netlist.

## Overall Physical Design Flow

```text
RTL Design
    ↓
Synthesis
    ↓
Floorplanning
    ↓
Power Planning
    ↓
Placement
    ↓
Clock Tree Synthesis
    ↓
Routing
    ↓
Physical Verification
    ↓
Final Design
```

The workshop work covered the early stages of this flow, with practical exposure to OpenLANE, Sky130, floorplanning, placement, library cells and physical design views.

## Tools / Technologies

- OpenLANE
- Sky130 PDK
- Open-source EDA tools
- Magic
- Linux environment
- Standard-cell libraries

## Conclusion

These modules provided practical exposure to the beginning of the physical-design flow, starting with open-source EDA and OpenLANE and progressing to floorplanning, placement and library-cell concepts. The included screenshots document the practical workshop activities and provide visual evidence of the work completed.
