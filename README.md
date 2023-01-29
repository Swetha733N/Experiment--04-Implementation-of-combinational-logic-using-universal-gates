# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure:

1. Create a project with required entities.
2. Create a module along with respective file name.
3. Run the respective programs for the given boolean equations.
4. Run the module and get the respective RTL outputs.
5. Create university program(VWF) for getting timing diagram. 6. Give the respective inputs for timing diagram and obtain the results

module combo1 (a,b,c,d,f);
input a,b,c,d;
output f;
wire f1, f2, f3;
assign f * 1 = (~c&~b&~a);
assign f 2=( sim d\& sim c\& sim a) ;
assign f 3=(c\& sim( sim b)8 sim a) ;
assign f= f1&~f2&~f3;
endmodule

module combo2 (a,b,c,d,f);
input a,b,c,d;
output f;
wire f 1,f2,f3,f4;
assign f1=c8( sim b) 8a assign f2 = d&(~c)&a;
assign f3=c8( sim b) 8a ; assign f4 = ~(f1|f2|f3);
not (f, f4); endmodule
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by:N.Swetha
RegisterNumber:22008828
*/
## RTL realization

## Output:
## RTL

![WhatsApp Image 2023-01-26 at 15 22 48](https://user-images.githubusercontent.com/122199934/214807714-b9476bd0-6028-4e3e-9bbf-0c7fe2a844d6.jpg)


![WhatsApp Image 2023-01-26 at 15 22 17](https://user-images.githubusercontent.com/122199934/214807644-0a481206-899c-4c85-9ab8-ed233d752944.jpg)


## Timing Diagram

![WhatsApp Image 2023-01-26 at 15 22 38](https://user-images.githubusercontent.com/122199934/214807780-6e6c0b48-3f3c-477a-9e78-e550e1c8ff38.jpg)


![WhatsApp Image 2023-01-26 at 15 22 27](https://user-images.githubusercontent.com/122199934/214807810-90609b79-0533-4d77-817c-fac7dd6c9f4a.jpg)


## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
