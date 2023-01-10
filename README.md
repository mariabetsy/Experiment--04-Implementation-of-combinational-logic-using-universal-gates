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
## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

Developed by: Maria Betsy
RegisterNumber:  22008543

FOR NAND GATE

module combo1(A,B,C,D,F);
input A,B,C,D;
output F;
wire p,q,r;
assign p=(~C & B & A);
assign q=(~D & C & ~A);
assign r=(C & ~B & A);
assign F=(~(~p & ~q & ~r));
endmodule

FOR NOR GATE

module combo2(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=( c & ~b & a);
assign q=( d & ~c & a);
assign r=( c & ~b & a);
assign f=((( p | q | r)));
endmodule

```

## Output:

## RTL realization

Using NAND Gate :

![image](https://user-images.githubusercontent.com/122356434/211535387-dc29e4df-bf73-4cd0-bbe5-8dd52ebebfda.png)

Using NOR Gate :

![image](https://user-images.githubusercontent.com/122356434/211535577-c018f9cf-0a87-4b5e-9f6c-20d0931e2a12.png)


## Timing Diagram

Using NAND Gate :

![image](https://user-images.githubusercontent.com/122356434/211535731-d20707aa-f7da-4508-98ca-57976dc28baf.png)


Using NOR Gate :

![image](https://user-images.githubusercontent.com/122356434/211535831-f506d9a8-e343-4fc5-b61d-f2c3d67e05a2.png)

## Truth Table :

Using NAND Gate :

![image](https://user-images.githubusercontent.com/122356434/211535971-4bc65d61-9ee4-408c-9d0d-7972ed87af50.png)

Using NOR Gate :

![image](https://user-images.githubusercontent.com/122356434/211536051-5d4a1ef3-ad85-4d87-8cd0-1b2b1af5bbbe.png)


## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
