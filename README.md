# Verilog Design and Testbench Code: Full Adder, Multiplexers, and Up-Down Counter

This repository contains Verilog HDL implementations of fundamental digital circuits. These projects are ideal for learning and simulating hardware design using various EDA tools.

---

##  Assignment List

### 1. Full Adder Using Two Half Adders  
**Design file:** `full_adder.v`  
**Testbench:** `tb_full_adder.v`  
**Description:** Implements a 1-bit full adder using two half adders. Outputs the sum and carry.  
**Inputs:** `A`, `B`, `Cin`  
**Outputs:** `SUM`, `Cout`  

---

### 2. 4-to-1 Multiplexer  
**Design file:** `mux4to1.v`  
**Testbench:** `tb_mux4to1.v`  
**Description:** A standard 4-to-1 multiplexer that selects one of four inputs using a 2-bit selector.  
**Inputs:** `in[3:0]`, `sel[1:0]`  
**Output:** `out`  

---

### 3. 2-to-1 Multiplexer  
**Design file:** `mux2to1.v`  
**Testbench:** `tb_mux2to1.v`  
**Description:** A basic 2-to-1 multiplexer for binary input switching.  
**Inputs:** `a[3:0]`, `b[3:0]`, `sel`  
**Output:** `y[3:0]`  

---

### 4. 2-to-1 MUX with D Flip-Flop Feedback  
**Design file:** `mux_dff_loop.v`  
**Testbench:** `tb_mux_dff_loop.v`  
**Description:** Implements a 2-to-1 MUX with one input fed from a D flip-flop output, creating a sequential design with memory.  
**Inputs:** `clk`, `i1`, `s`  
**Output:** `y`  

---

### 5. Up-Down Counter with Reset  
**Design file:** `up_down_counter.v`  
**Testbench:** `tb_up_down_counter.v`  
**Description:** A 4-bit synchronous counter that counts up or down based on control and supports asynchronous reset.  
**Inputs:** `clk`, `reset`, `up_down`  
**Output:** `count[3:0]`  

---

##  Simulation Instructions

All modules include testbenches. You can simulate them using tools such as:

- Icarus Verilog + GTKWave  
- VSD-IAT  
- ModelSim / Vivado Simulator  

### Example: Run Simulation with Icarus Verilog

```bash
iverilog -o testbench.out design.v testbench.v
vvp testbench.out
gtkwave dump.vcd
