# 💧 Mini Water Treatment ICS Facility

**Designer:** Shawn Li  
**Date Started:** July 13, 2025

---

## 🎯 Objective

This project is a personal initiative to help me gain a better understanding of the electrical and control systems involved in small-scale water and wastewater treatment facilities. While I don’t yet have firsthand experience with Hazen and Sawyer’s specific workflow, this project is an attempt to simulate what such a facility might include — from power distribution and motor controls to SCADA-ready I/O and backup systems. The goal is to prepare for an entry-level engineering role by building foundational familiarity, and to demonstrate initiative and a willingness to learn and grow in the field.

---

## 🏗️ System Overview

The facility includes three zones:

### 1. Collection Pump Station (MCC-1)
- Two influent pumps (1 duty, 1 standby)
- ATS + portable generator inlet
- UPS/DC panel for level & alarms
- PMCB for monitoring

### 2. Filtration Building (MCC-2)
- Screens, dual blowers, dual chemical feed (N+1 redundancy)
- Manual Transfer Switch (optional)
- UPS or 24VDC panel for PLC/SCADA
- SCADA fiber stub
>-This design represents a simplified water treatment process for learning purposes. In full-scale wastewater treatment, additional steps such as clarification, biological treatment, and disinfection would be required to meet regulatory standards.

### 3. Clearwell & Distribution (MCC-3)
- Three booster pumps (2 duty, 1 standby)
- Stationary generator + ATS
- PMCB and UPS-backed SCADA I/O

---

## 📄 Drawing Set

| Sheet # | Title                         | Description |
|--------|-------------------------------|-------------|
| 0      | Site and Floor Plan           | Top-down layout of all zones with MCCs, lighting, pumps |
| 1      | One-Line Power Diagram        | Utility → XFMR → SWBD → MCCs → Loads (w/ gensets, ATS, SPDs, CPTs) |
| 2      | Pump Station Schematic        | HOA logic, start/stop PB, OLs, UPS DC logic |
| 3      | Filtration + Alarm Schematic  | Controls for blowers, chem feed, alarms, SCADA stub |
| 4      | Lighting and Power Layout     | Room lighting, emergency fixtures, receptacles, generator location |
| 5      | Symbol Legend & Abbreviations| Only symbols actually used |
| 6      | General Notes and Title Block | Arc flash, grounding, N+1 strategy, SCADA notes, disclaimer |

---

## ⚡ Electrical Scope Summary

- **Power Chain:**  
  Utility → Transformer (480V, 3Ø) → Main Switchboard → MCCs/Lighting/UPS → Loads

- **Key Equipment:**
  - VFD motors, relays, alarms, sensors
  - 24VDC PLC power and SCADA stub
  - ATS, generators, PMCBs, SPDs, CPTs

---

## 🔋 Backup Power Strategy

| MCC | Zone               | Generator       | Transfer Switch | Control Backup            |
|-----|--------------------|-----------------|------------------|----------------------------|
| 1   | Collection Pumps   | Portable        | ATS              | Local DC Panel + UPS      |
| 2   | Filtration Bldg.   | Optional        | MTS              | UPS or 24VDC Panel        |
| 3   | Distribution Zone  | Stationary (75kW) | ATS            | UPS + SCADA I/O Panel     |

---

## 🏷️ Labeling Conventions

- **Motors:** `P-101`, `B-201`  
- **MCCs:** `MCC-1`, `MCC-2`, `MCC-3`  
- **Lighting Panels:** `LP-1`  
- **Circuits:** `C-101A`, `LGT-102`  
- **PMCBs:** `PMCB-MCC-1`, `PMCB-MCC-3`  
- **ATS Units:** `ATS-1`, `ATS-3`  
- **Transformers:** `CPT-1`, `CPT-2`, etc.

---

## 🧰 Tools Used

- **AutoCAD Electrical** – Wiring and one-line diagrams  
- **Revit (optional)** – Lighting layout and floor plans  
- **DALL·E or sketches** – Conceptual site drawings  
- **GitHub** – Version control and documentation  
- **PDF Export** – Print-ready deliverables

---

## ✅ Progress Log

- **7/13**: Repository created, master plan outlined, electrical scope defined  
- **Next Step**: Begin Sheet 0 – Site and Floor Plan (equipment and MCC layout)

---

> _This project is for learning and demonstration purposes only._
