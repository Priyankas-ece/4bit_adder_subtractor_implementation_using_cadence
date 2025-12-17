# Simulation Methodology – Cadence Virtuoso

## Overview
This document explains the **functional simulation process** used to verify the **4-bit Adder-Subtractor** design using **Cadence Analog Design Environment (ADE)**.

---

## Tools Used
- Cadence Virtuoso ADE
- Spectre Simulator
- Technology Library Models

---

## Simulation Setup
- Connect power supplies (`VDD` and `GND`).
- Apply input stimulus for `A[3:0]`, `B[3:0]`, and control signal `M`.
- Set simulation time and analysis type (Transient).

---

## Test Cases
- Verify addition operation (`M = 0`).
- Verify subtraction operation (`M = 1`).
- Test multiple input combinations.
- Observe sum/difference and carry-out outputs.

---

## Observations
- Output waveforms match expected arithmetic results.
- Carry propagation functions correctly across all stages.
- Subtraction correctly follows 2’s complement logic.

---

## Simulation Results
Simulation waveforms confirm the correct behavior of the adder-subtractor for both addition and subtraction operations.

---

## Conclusion
Functional simulation validates the logical correctness of the schematic design before physical implementation.
