# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
```
A universal gate is a gate which can implement any Boolean function without need to
use any other gate type.
The NAND and NOR gates are universal gates.
In practice, this is advantageous since NAND and NOR gates are economical and
easier to fabricate and are the basic gates used in all IC digital logic families.
In fact, an AND gate is typically implemented as a NAND gate followed by an
inverter not the other way around
Likewise, an OR gate is typically implemented as a NOR gate followed by an inverter
not the other way around
 ```
## Procedure

### Step 1:
Module Declaration. module is a keywords defined in Verilog .

### Step 2:
Input-Output Delecaration. 
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
we have four inputs and one output.

### Step 3:
Use wire declaration and assign statements to define the functionality of logic circuits.

### Step 4:
Ending module. endmodule is a keywords defined in Verilog.


## Program:
```
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: Sowmiya N
RegisterNumber:  212221230106
```
### NAND Gate:
```
module unand(A,B,C,D,Y);
input A,B,C,D;
output Y;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign Y = (~P&~Q&~R);
endmodule
```
### NOR Gate:
```
module norunigate(A,B,C,D,F);
input A,B,C,D;
output F;
wire b,c,P,Q,R,Y;
assign b= ~B;
assign c= ~C;
assign P= C & b & A;
assign Q= D & c & A;
assign R= C & b & A;
nor(Y,P,Q,R);
assign F = ~Y;
endmodule

```

## Output:

## Truthtable
### NAND Gate:
![op](./0nand.png)
### NOR Gate:
![op](./0nor.png)

##  RTL realization
### NAND Gate:
![op](./0a.png)
### NOR Gate:
![op](./norrtl.png)

## Timing diagram 
### NAND Gate:
![op](./0b.png)
### NOR Gate:
![op](./nortd.png)
## Result:
 
Implementation of the given logic function using NAND and NOR gates is done and verification its operation in Quartus using Verilog programming is carried out sucessfully.