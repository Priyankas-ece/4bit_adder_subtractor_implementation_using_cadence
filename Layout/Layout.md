# Layout Design Methodology – Cadence Virtuoso

## Overview
This document outlines the **physical layout design steps** used to implement the **4-bit Adder-Subtractor** in **Cadence Virtuoso Layout Editor**.  
The layout was created at the **transistor level** and verified using **DRC and LVS**.

---

## Tools Used
- Cadence Virtuoso Layout Suite
- Assura for DRC and LVS
- Technology Library (GPDK 180nm)

---

## Layout Design Flow
The layout follows a **hierarchical bottom-up approach**:
1. Layout of basic logic gates
2. Layout of 1-bit full adder
3. Layout of 4-bit adder-subtractor
4. Physical verification

---

## Step 1: Technology Setup
- Load the appropriate technology file.
- Set grid resolution and snapping.
- Verify layer definitions and design rules.

---

## Step 2: Basic Gate Layout
- Design layouts for AND, OR, NAND, NOR, XOR, and NOT gates.
- Place PMOS in N-well and NMOS in P-substrate.
- Use shared diffusion to optimize area.
- Route connections using Metal layers.
- Add `VDD` and `GND` rails and define pins.

---

## Step 3: 1-Bit Full Adder Layout
- Integrate gate layouts hierarchically.
- Ensure symmetric placement for balanced routing.
- Carefully route carry and sum signals.
- Maintain clean power distribution.

---

## Step 4: 4-Bit Adder-Subtractor Layout
- Cascade four full adder layouts.
- Route the control signal `M` across all XOR gates.
- Maintain consistent spacing between stages.
- Add top-level pins for inputs and outputs.

---

## Step 5: Pin Labeling
- Match layout pin names exactly with schematic.
- Define pins for `A[3:0]`, `B[3:0]`, `M`, `S[3:0]`, and `Cout`.

---

## Conclusion
The layout design was successfully completed following standard VLSI practices, ensuring a clean and scalable physical implementation.
