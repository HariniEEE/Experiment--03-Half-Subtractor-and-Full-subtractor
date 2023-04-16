# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule

FULL SUBTRACTOR: 

module FullSub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule

Developed by: Harini.E 
RegisterNumber: 212222050017
*/

LOGIC GATES
![Logic gates](https://user-images.githubusercontent.com/128949246/232283443-697de70c-a5de-4324-9c48-aebfa8500624.jpeg)



## Output:

## Truthtable

Half Subtractor

![Truth half](https://user-images.githubusercontent.com/128949246/232283528-da0fffab-0dcb-455a-bc05-285e4a0ebc72.jpeg)

Full Subtractor

![Truth full](https://user-images.githubusercontent.com/128949246/232283541-ab31243f-969c-494a-bcde-a7821ac12ec8.jpeg)



## OUTPUT RTL realization

Half Subtractor

![RTL half](https://user-images.githubusercontent.com/128949246/232283491-6646431a-e13f-48a1-9940-f114fd2254d5.jpeg)

Full Subtractor

![RTL full](https://user-images.githubusercontent.com/128949246/232283510-48650f88-1b58-4c29-ad43-1bd04669f765.jpeg)


## Timing diagram 

Half Subtractor

![Timing half](https://user-images.githubusercontent.com/128949246/232283565-a0946bf7-9fa3-4721-8fa2-7a26ab030d13.jpeg)

Full Subtractor

![Timing full](https://user-images.githubusercontent.com/128949246/232283580-4a81ae99-3dc1-4564-a5be-dcac856e299e.jpeg)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
