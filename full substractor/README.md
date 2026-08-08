# Full Subtractor using Verilog

## Overview

A Full Subtractor is a combinational logic circuit that subtracts two binary bits while considering a borrow input from the previous stage. It produces two outputs:

- Difference (D)
- Borrow Out (Bout)

This project implements a Full Subtractor using Verilog HDL and includes a testbench to verify all possible input combinations.

---

## Truth Table

| A | B | Bin | Difference (D) | Borrow Out (Bout) |
|---|---|-----|----------------|-------------------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 |
| 1 | 1 | 1 | 1 | 1 |

---

## Boolean Expressions

Difference:

D = A ⊕ B ⊕ Bin

Borrow Out:

Bout = (~A & B) | (~A & Bin) | (B & Bin)

---

## Project Files

- `full_subtractor.v` – Verilog design
- `full_subtractor_tb.v` – Testbench
- `simulation_results.txt` – Expected simulation output

---

## Software Used

- Icarus Verilog
- GTKWave (Optional)
- ModelSim (Optional)

---

## How to Compile

```bash
iverilog -o full_subtractor full_subtractor.v full_subtractor_tb.v
```

Run Simulation

```bash
vvp full_subtractor
```

Generate Waveform

```bash
gtkwave full_subtractor.vcd
```

---

## Expected Output

```text
A B Bin | D Bout
0 0 0   | 0 0
0 0 1   | 1 1
0 1 0   | 1 1
0 1 1   | 0 1
1 0 0   | 1 0
1 0 1   | 0 0
1 1 0   | 0 0
1 1 1   | 1 1
```

---

## Applications

- Arithmetic Logic Units (ALUs)
- Binary subtraction circuits
- Digital processors
- Computer arithmetic

---

