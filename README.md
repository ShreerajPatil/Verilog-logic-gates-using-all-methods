# Verilog-logic-gates-using-all-methods
A comprehensive Verilog library of fundamental digital logic gates, implemented in multiple modeling styles (Behavioral, Dataflow, Structural) with corresponding testbenches.
# Verilog Logic Gate Library

This repository contains a comprehensive collection of basic digital logic gates implemented in Verilog HDL. Each gate is designed using multiple modeling styles (Behavioral, Dataflow, and Structural) to demonstrate different levels of abstraction.

Every gate also includes a corresponding testbench to verify its functionality, making this an excellent resource for learning and practical application.

## Gates Included
*   AND
*   OR
*   NOT
*   NAND
*   NOR
*   XOR
*   XNOR

---

## How to Use the Code

The files in this repository are provided as templates. To use them in your own projects, you will need to rename the modules to match your file names.

#### Design Code

This is the Verilog code for the gate itself.
```
module Code(
input a, b,
output z
);
nand (z, a, b);
endmodule
```
**To Use This Code:**
*   Replace `Code` with the name of your Verilog file (e.g., `nand_gate_structural`).

---

#### Testbench Code

This is the testbench used to verify the design code.
```
module Testbench();
reg a, b;
wire z;

Code uut(a, b, z);

initial begin
a=0; b=0;
#10 a=0; b=1;
#10 a=1; b=0;
#10 a=1; b=1;
#10 $finish;
end
endmodule
```
**To Use This Testbench:**
1.  Replace `Testbench` with the name of your testbench file (e.g., `nand_gate_tb`).
2.  On the line `Code uut(a, b, z);`, replace `Code` with the module name from your design file (e.g., `nand_gate_structural`). This connects the testbench to your gate.

---

This project is licensed under the MIT License. See the `LICENSE` file for details.

