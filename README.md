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
~~~
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: M.suren.
RegisterNumber:  23005055
half subractor
module digitalexpfour(output b,d,input x,y);
assign d = x^y;
assign b = ~x&y;
endmodule

full subractor
module digitalexpfourone(output b,d,input x,y,z);
assign d = x^y^z;
assign b = ~x&(y^z)|y&z;
endmodule
~~~
*/

## Output: 
The half subractor and full subractor are sucessfully prover

## Truthtable

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/a4faa006-0b25-4609-91d0-754b55863734)


![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/51c4512f-dc0d-4209-94e7-1105119e74e2)


##  RTL realization

half subractor

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/12c968a5-a9bd-4661-9b95-ef2be561c10f)


full subractor

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/71756fc7-1bba-4aeb-b963-2fb2f9449931)



## Timing diagram 

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/0cec1766-f6d0-4049-8b77-bdc817325269)

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/3276ec1d-d488-4fdc-bb0a-4e7590dea697)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
