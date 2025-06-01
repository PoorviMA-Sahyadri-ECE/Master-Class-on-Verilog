# Verilog Design and Testbench code: Full Adder, 4-to-1 Multiplexer, and Up-Down Counter

This repository contains Verilog HDL implementations of basic digital logic circuits commonly used in learning and practicing digital design and EDA tool usage.

##  Assignment List

### 1. Full Adder Using Two Half Adders
- **Design file**: `full_adder.v`
- **Testbench**: `tb_full_adder.v`
- **Description**: Implements a 1-bit full adder using two half adders. The output includes a sum and carry out.
- **Inputs**: A, B, Cin
- **Outputs**: SUM, Cout

### 2. 4-to-1 Multiplexer
- **Design file**: `mux4to1.v`
- **Testbench**: `tb_mux4to1.v`
- **Description**: Selects one of four input lines based on a 2-bit select signal.
- **Inputs**: `in[3:0]`, `sel[1:0]`
- **Output**: `out`

### 3. Up-Down Counter with Reset
- **Design file**: `up_down_counter.v`
- **Testbench**: `tb_up_down_counter.v`
- **Description**: A 4-bit counter that counts up or down on each clock cycle, with asynchronous reset.
- **Inputs**: clk, reset, up_down
- **Output**: count[3:0]

---

##  Simulation

Each module comes with its own testbench. Use tools like:
- **Icarus Verilog + GTKWave**
- **VSD-IAT**
- **ModelSim or Vivado Simulation**

### To Run Simulation (with Icarus Verilog):
```bash
iverilog -o counter_tb up_down_counter.v tb_up_down_counter.v
vvp counter_tb
gtkwave up_down_counter.vcd
