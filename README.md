# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher

 Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor && Full Subtractor
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
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: ASHWIN KUMAR.S

RegisterNumber:  212222240013

*/
## FULLSUBTRACTOR
```
module proj4fullsubtractor(A,B,bin,diff,borrow);
input A,B,bin;
output diff,borrow;
assign diff= A^B^bin;
assign borrow = ((~A)&B)|((~(A^B))&bin);
endmodule
```


## HALFSUBTRACTOR
```
module proj4halfsubtractor(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff = A^B;
assign borrow = (~A)&B;
endmodule
```

## Output:

## Truthtable
### FULLSUBTRACTOR
![TT_FULL](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/b61b4b97-06af-43f4-9adc-606763629835)

### HALFSUBTRACTOR

![TT_HALF](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/1a822ddb-e2e4-46cf-be6d-1397905586f8)



##  RTL realization
### FULLSUBTRACTOR
![fullsubtractor_rtl](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/5720a7ae-2773-40ce-aa96-e58905ef7733)

### HALFSUBTRACTOR
![halfsubtractor_rtl](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/bb269eef-47ce-40ee-b031-3aef982b5da3)


## Timing diagram 

### FULLSUBTRACTOR
![fullsubtractor_wf](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/00414884-de77-4e3f-a090-4d5ef3dcc83f)

### HALFSUBTRACTOR

![halfsubtractor_Wf](https://github.com/Ashwinkumar-03/Experiment--04-Half-Subtractor-and-Full-subtractor/assets/118663725/c8b42fe2-643a-4a35-b0e9-06d28a6b9293)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
