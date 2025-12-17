# Schematic Design Methodology – Cadence Virtuoso

## Overview
This document describes the **schematic design process** followed to implement the **4-bit Adder-Subtractor** using **Cadence Virtuoso Schematic Editor**.  
The design is created using **CMOS logic**, following a **hierarchical and modular approach**.

---

## Tools Used
- Cadence Virtuoso Schematic Editor
- Technology Library (GPDK 180nm)
- Analog Design Environment (ADE)

---

## Design Approach
A **bottom-up hierarchical design methodology** was adopted:
1. Design of basic logic gates
2. Design of 1-bit full adder
3. Integration into a 4-bit adder-subtractor

---

## Step 1: Creation of Basic Logic Gates
The following logic gates were designed at the transistor level:
- AND Gate
- NAND Gate
- OR Gate
- NOR Gate
- XOR Gate
- NOT Gate

### Procedure:
- Use PMOS and NMOS transistors according to CMOS logic.
- Connect PMOS devices to `VDD` and NMOS devices to `GND`.
- Ensure proper sizing and connectivity.
- Define input and output pins clearly.

---

## Step 2: 1-Bit Full Adder Design
- Construct the full adder using XOR, AND, and OR gates.
- Verify intermediate signals such as carry and sum.

---

## Step 3: 4-Bit Adder-Subtractor Integration
- Cascade four 1-bit full adder blocks.
- Connect carry-out of each stage to carry-in of the next.
- Share the control signal `M` across all stages.
- Label all inputs, outputs, and power nets.

---

## Step 4: Schematic Verification
- Check for floating nodes and missing connections.
- Ensure pin names match across hierarchy levels.
- Save and finalize the schematic for simulation and layout.

---

## Conclusion
The schematic design of the **4-bit Adder-Subtractor** was successfully completed using a modular and hierarchical approach, ensuring correctness and ease of layout implementation.
