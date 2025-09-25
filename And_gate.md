**Structural (Gate-Level) Modeling**

**Code** 
```
module Code(
input wire a,b,
output wire z
    );
    and gate(z,a,b);
endmodule
```

**Testbench**
```
module Testbench(

    );
    reg a,b;
    wire z;
    Code uut(a,b,z);
    initial
    begin
    a=0; b=0;
    #10 a=0; b=1;
    #10 a=1; b=10;
    #10 a=1; b=1;
    #10 $finish;
    end
endmodule
```

**Dataflow Modeling**

**Code**
```
module Code(
input wire in,
output wire out
    );
    assign out = ~in;
endmodule
```
**Testbench**
```
module Testbench1(
    );
    reg in;
    wire out;
    Code uut(in,out);
    initial 
    begin 
    
    in=0;
    #10 
    in=1;
    #10 $finish;
    end
endmodule
```
**Behavioral Modeling**

**Code**
```
module Code(
input wire in,
output reg out

    );
    always@ (*) begin
    out = ~in;
    end
endmodule
```
**Testbench**
```
module Testbench1(
    );
    reg in;
    wire out;
    Code uut(in,out);
    initial 
    begin 
    
    in=0;
    #10 
    in=1;
    #10 $finish;
    end
endmodule
```
![Schematic](Notsche.png)
![Testbench](NotgateG.png)
