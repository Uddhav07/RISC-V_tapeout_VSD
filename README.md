# RISC-V Tapeout using Sky130 PDK

## 📚 Course Overview
This repository contains comprehensive notes and documentation for the RISC-V Physical Design workshop using open-source EDA tools and Sky130 PDK. The course covers the complete RTL to GDSII flow using OpenLANE and related tools.

---

## 📅 Daily Content

### [Day 1: Inception of open-source EDA, OpenLANE and Sky130 PDK](./Day_1/README.md)
**Topics Covered:**
- How to talk to computers - QFN-48 Package, chip architecture, RISC-V basics
- SoC design and OpenLANE - ASIC design components, RTL2GDS flow, OpenLANE introduction
- Getting familiar with open-source EDA tools - Directory structure, design preparation, synthesis

**Key Learnings:** Introduction to chip components, RISC-V ISA, OpenLANE ASIC flow, and hands-on with synthesis

---

### [Day 2: Good floorplan vs bad floorplan and introduction to library cells](./Day_2/README.md)
**Topics Covered:**
- Chip floor planning considerations - Utilization factor, pre-placed cells, decoupling capacitors, power planning
- Library binding and placement - Netlist binding, placement optimization, congestion analysis
- Cell design and characterization flows - Design inputs, circuit/layout design, characterization
- General timing characterization - Timing thresholds, propagation delay, transition time

**Key Learnings:** Floorplanning concepts, placement strategies, cell design flow, timing parameters

---

### [Day 3: Design library cell using Magic Layout and ngspice characterization](./Day_3/README.md)
**Topics Covered:**
- CMOS inverter ngspice simulations - SPICE deck creation, switching threshold, static/dynamic analysis
- CMOS fabrication process - Active regions, well formation, gate/LDD/source-drain formation, interconnects
- Sky130 Tech File Labs - Magic tool usage, DRC rules, tech-file modifications and fixes

**Key Learnings:** SPICE simulation, 16-mask CMOS process, Magic layout tool, DRC verification and fixes

---

### [Day 4: Pre-layout timing analysis and importance of good clock tree](./Day_4/README.md)
**Topics Covered:**
- Timing modeling using delay tables - Grid/track info, LEF generation, timing libraries, delay tables
- Timing analysis with ideal clocks - Setup time, clock jitter/uncertainty, OpenSTA analysis, timing ECO
- Clock tree synthesis - H-Tree algorithm, crosstalk, clock net shielding, TritonCTS
- Timing analysis with real clocks - Setup/hold analysis with real clocks, CTS buffer impact

**Key Learnings:** Delay modeling, STA concepts, CTS implementation, timing optimization techniques

---

### [Day 5: Final steps for RTL2GDS using tritonRoute and openSTA](./Day_5/README.md)
**Topics Covered:**
- Routing and DRC - Maze routing (Lee's algorithm), design rule checks
- Power distribution network and routing - PDN generation, power straps, global/detail routing
- TritonRoute features - Pre-processed route guides, connectivity handling, routing topology

**Key Learnings:** Routing algorithms, PDN implementation, TritonRoute features, final GDSII generation

---

## 🛠️ Tools Used
- **OpenLANE** - Automated RTL to GDSII flow
- **Magic** - Layout editor and DRC tool
- **ngspice** - SPICE simulation
- **OpenSTA** - Static timing analysis
- **TritonCTS** - Clock tree synthesis
- **TritonRoute** - Detailed routing
- **Sky130 PDK** - Open-source process design kit

---

## 📖 Workshop Structure
The workshop consists of **87 topics** distributed across **5 days**, covering:
1. Chip architecture fundamentals and tool setup
2. Floorplanning and placement strategies
3. Custom cell design and characterization
4. Timing analysis and clock tree synthesis
5. Routing and final GDSII generation

---

## 🚀 Getting Started
1. Navigate to the respective day folder
2. Follow the README for that day
3. Complete hands-on labs and take notes in the provided template sections
4. Document commands, screenshots, and key learnings

---

## 📝 Notes Template Structure
Each day's README includes:
- **Key Concepts** - Main theoretical points
- **Notes** - Detailed observations and learnings
- **Commands Used** - Terminal commands for labs
- **Screenshots/Diagrams** - Visual documentation
- **Summary** - Key takeaways and questions

---

## 📂 Repository Structure
```
RISC-V_tapeout_VSD/
├── README.md                 # Main navigation (this file)
├── Day_1/
│   └── README.md            # Day 1 notes and content
├── Day_2/
│   └── README.md            # Day 2 notes and content
├── Day_3/
│   └── README.md            # Day 3 notes and content
├── Day_4/
│   └── README.md            # Day 4 notes and content
└── Day_5/
    └── README.md            # Day 5 notes and content
```

---

## 🎯 Learning Objectives
By the end of this workshop, you will:
- ✅ Understand complete RTL to GDSII flow
- ✅ Work with open-source EDA tools effectively
- ✅ Design and characterize custom standard cells
- ✅ Perform timing analysis and optimization
- ✅ Generate production-ready GDSII files using Sky130 PDK

---

## 📌 Progress Tracking
- [ ] Day 1 - Inception of open-source EDA
- [ ] Day 2 - Floorplanning and library cells
- [ ] Day 3 - Custom cell design and characterization
- [ ] Day 4 - Timing analysis and CTS
- [ ] Day 5 - Routing and final RTL2GDS

---

## 🔗 References
- [OpenLANE GitHub](https://github.com/The-OpenROAD-Project/OpenLane)
- [SkyWater SKY130 PDK](https://github.com/google/skywater-pdk)
- [Magic VLSI](http://opencircuitdesign.com/magic/)
- [ngspice](http://ngspice.sourceforge.net/)

---

**Repository:** RISC-V_tapeout_VSD  
**Branch:** week-6  
**Last Updated:** October 29, 2025
