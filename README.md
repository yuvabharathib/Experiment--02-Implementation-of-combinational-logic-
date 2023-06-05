# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
# AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
# Equipments Required:
1.Hardware – PCs, Cyclone II , USB flasher

2.Software – Quartus prime


# Theory
```
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.Combinational logic gates are digital circuits that produce outputs based solely on the current inputs. These gates are the building blocks for implementing digital systems and are used in a wide range of applications, including arithmetic and logic operations, memory devices, and control circuits.The two functions, F1 and F2, can be implemented using a combination of logic gates such as AND gates, OR gates, and NOT gates.
```

# Procedure
```
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output(RTL Viewer and Timing Diagram) to represent F1 and F2.

5.End the verilog program using keyword endmodule.
```
# Program:
```

Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:YUVABHARATHI.B
RegisterNumber: 212222230181

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
```
## RTL realization
# Output:
## RTL
## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/yuvabharathib/Experiment--02-Implementation-of-combinational-logic-/assets/113497404/0f0aa751-f494-4799-93b9-77b344ee1610)


## F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/yuvabharathib/Experiment--02-Implementation-of-combinational-logic-/assets/113497404/46ded809-cb95-4de0-972b-9b6ce640fbfa)


## Timing Diagram
## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/yuvabharathib/Experiment--02-Implementation-of-combinational-logic-/assets/113497404/fb819c9a-804b-44b5-80e1-e1bb4a379a3c)


## F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/yuvabharathib/Experiment--02-Implementation-of-combinational-logic-/assets/113497404/8069b35b-41ed-44ef-a2ba-effe2b814888)


# Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

