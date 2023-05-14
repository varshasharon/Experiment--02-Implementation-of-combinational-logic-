# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

#### Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

#### Using NOR gates

Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure
Step 1- Create a project with required entities.
Step 2- Create a module along with respective file name.
Step 3- Run the respective programs for the given boolean equations.
Step 4- Run the module and get the respective RTL outputs.
Step 5- Create university program(VWF) for getting timing diagram.
Step 6- Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: E. VARSHA SHARON
RegisterNumber: 212222100058

module EXP2a (a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d)|(~a&b&d)|(a&b&~c);
endmodule

for F2=xy’z+x’y’z+w’xy+wx’y+wxy

module EXP2b (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule
```
## RTL realization

## Output:
## RTL
#### F1
![image](https://github.com/varshasharon/Experiment--02-Implementation-of-combinational-logic-/assets/98278161/db4abef1-a39b-47f3-9710-77883adb36df)

#### F2
![image](https://github.com/varshasharon/Experiment--02-Implementation-of-combinational-logic-/assets/98278161/cdb90b96-e33b-411d-89a7-c8a89362ee02)

## Timing Diagram
#### F1
![image](https://github.com/varshasharon/Experiment--02-Implementation-of-combinational-logic-/assets/98278161/26b54537-89c9-4faf-b3e5-9ca48d6186e2)

#### F2
![image](https://github.com/varshasharon/Experiment--02-Implementation-of-combinational-logic-/assets/98278161/1cb4c6be-c245-4c3a-9804-e7be43c63fc8)

## Result:
Thus, the given logic functions are implemented using and their operations are verified using Verilog programming.
