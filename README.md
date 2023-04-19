# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
1.Hardware – PCs, Cyclone II , USB flasher

2.Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' 

## Logic Diagram
![image](https://user-images.githubusercontent.com/113497404/233025235-1736dd3b-be6c-4adc-b8bd-51d7c5e6120a.png)


## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:Yuvabharathi.B 
RegisterNumber: 212222230181
Using NAND gates:

module NAND(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P=(~(~C & B & A));
assign Q=(~(~D & C & A));
assign R=(~(C & ~B & A));
assign F=~(P & Q & R);
endmodule

Using NOR gates:

module NOR(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = (C & ~B & A);
assign Q = (D & ~C & A);
assign R = (C & ~B & A);
assign S = (~(P | Q | R));
assign F = (~S);
endmodule
```
## RTL realization
## Output:
### NAND combination
![image](https://user-images.githubusercontent.com/113497404/233026220-2e45680b-35ee-49e7-bf11-180c362ffad2.png)
### NOR combination
![image](https://user-images.githubusercontent.com/113497404/233026410-73369716-6dd1-48d5-b3fb-8a8c6748ac4f.png)


## Timing Diagram
### NAND combination
![image](https://user-images.githubusercontent.com/113497404/233026622-abca74a4-dcf7-47cd-8fb0-f1f1f4fb0e50.png)
### NOR combination
![image](https://user-images.githubusercontent.com/113497404/233026720-e885099a-b0a6-436e-aaea-23bef84d617d.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
