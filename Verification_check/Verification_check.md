# Physical Verification – DRC and LVS

## Overview
This document describes the **physical verification process** performed on the **4-bit Adder-Subtractor layout** to ensure manufacturability and schematic equivalence.

---

## Tools Used
- Cadence Assura 
- Virtuoso Layout Editor

---

## Design Rule Check (DRC)
- Ensures layout complies with foundry design rules.
- Checks spacing, width, enclosure, and overlap constraints.
- All DRC violations were resolved successfully.

---

## Layout vs. Schematic (LVS)
- Compares extracted layout netlist with schematic netlist.
- Verifies device count, connectivity, and pin matching.
- Successful LVS confirms electrical equivalence.

---

## Verification Results
- DRC: **PASS**
- LVS: **PASS**

---

## Conclusion
The layout passed all physical verification checks, confirming that the design is both **fabrication-ready** and **functionally correct**.
