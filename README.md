# 4-Bit Adder-Subtractor Design using Cadence Virtuoso

## 🏗️ Introduction
This project presents the **design, layout, and verification of a 4-bit adder-subtractor circuit** using **Cadence Virtuoso**.  
The objective of the project is to develop a combinational arithmetic circuit capable of performing both **addition and subtraction** operations on 4-bit binary inputs based on a single control signal.  

This work serves as a fundamental building block in **Arithmetic Logic Unit (ALU)** design, forming the core of digital processors.  
The project demonstrates complete **VLSI design flow** — from schematic creation to layout generation, followed by **Design Rule Check (DRC)** and **Layout vs. Schematic (LVS)** verification.

## 🎯 Objectives
- To design a **4-bit Adder-Subtractor** circuit using **Cadence Virtuoso** tools.  
- To understand and apply **hierarchical design methodology** in VLSI.  
- To verify the functionality through **schematic simulation**.  
- To perform **layout design** and ensure correctness using **DRC** and **LVS** checks.  

## ⚙️ Design Overview

### Principle of Operation
The 4-bit adder-subtractor is designed using a **control signal** (`M`) to determine the operation mode:
- When `M = 0` → **Addition** is performed.
- When `M = 1` → **Subtraction** is performed using the 2’s complement method.
The subtraction operation is achieved by complementing the B inputs when `M = 1` and adding 1 through the carry-in of the least significant bit adder.

### Truth Table

| Control (M) | Operation     | Output       |
|--------------|---------------|---------------|
| 0            | Addition       | A + B         |
| 1            | Subtraction    | A - B (A + 2’s complement of B) |

## Circuit Components

### 1. **Basic Logic Gates**
- Implemented using standard CMOS logic in Cadence.  
- Include AND, OR, XOR and NOT gates used throughout the design.  

### 2. **1-Bit Full Adder/Subtractor**
- Core building block of the design.  
- Performs bitwise addition or subtraction depending on the control signal.  
- Accepts three inputs: `A`, `B`, and `Cin`, and produces `Sum/Diff` and `Cout`.

### 3. **4-Bit Adder-Subtractor**
- Constructed by cascading four 1-bit full adder/subtractor modules.  
- The carry-out of each stage is connected to the carry-in of the next stage.  
- The control signal propagates to all stages to define the mode of operation.  

### Block Diagram 

<img width="1248" height="832" alt="4bit_add_sub" src="https://github.com/user-attachments/assets/f2fc501c-fbea-4cb3-9fe0-9a948282b69e" />

## 🧩 Design Methodology

### Step 1: **Schematic Design**
- Each logic gate and 1-bit full adder/subtractor was designed using transistor-level schematic in **Cadence Virtuoso**.  
- Hierarchical connections were created to build the 4-bit design.  
- All nodes and ports were properly named for LVS matching.

### Step 2: **Layout Design**
- Layouts for all modules were created using **Virtuoso Layout Editor**.  
- Metal layers and vias were placed following DRC constraints.  
- Hierarchical layout generation was performed for the 4-bit adder-subtractor.

### Step 3: **Design Rule Check (DRC)**
- Conducted using **Assura DRC** to ensure compliance with foundry-specific design rules.  
- No spacing, width, or enclosure violations were observed.  

### Step 4: **Layout vs. Schematic (LVS)**
- Performed to verify electrical and topological equivalence between layout and schematic.  
- Successful LVS ensures that the physical layout accurately represents the designed schematic.

### Step 5: **Simulation and Verification**
- Functional simulation performed using **Cadence Spectre**.  
- Verified that outputs match expected addition and subtraction results for all input combinations.

## 📈 Simulation Results

| Input A | Input B | Control (M) | Output (Sum/Diff) | Operation  |
|----------|----------|-------------|-------------------|-------------|
| 0101     | 0011     | 0           | 1000              | Addition    |
| 0101     | 0011     | 1           | 0010              | Subtraction |

Waveform and output plots confirm correct arithmetic functionality for all cases.

## 🖼️ Layout and Verification Screenshots
All screenshots are included in the `screenshots/` directory:
- **Schematic View** 
- **Layout View**
- **DRC Report Screenshot**  
- **LVS Verification Screenshot**  
- **Simulation Waveforms**

## 🧮 Tools and Technologies Used
Cadence Virtuoso – Schematic and Layout design  
Cadence Spectre – Functional Simulation  
Assura – DRC and LVS verification  
Technology Node: GPDK 180nm

## ✅ Key Outcomes
- Successfully implemented and verified a 4-bit adder-subtractor using Cadence Virtuoso.
- Verified DRC and LVS clean layout ensuring design correctness.
- Achieved accurate functional simulation demonstrating correct addition and subtraction operations.
- Gained hands-on understanding of digital VLSI design flow and hierarchical circuit implementation.

## 👩‍💻 Author
Priyanka S  
VLSI Design & Verification Enthusiast  
Cadence Tools | Digital Circuit Design | Frontend & Backend VLSI
