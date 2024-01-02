Name: M.suren.

Reg.no:23005055


# Experiment--03-Half-Subtractor-and-Full-subtractor

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

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/8f5d5d3d-cb1b-4548-90d3-9ed12aaab3cc)



![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/509e45c8-a6bf-43c1-ac35-af234688dd6f)



##  RTL realization

half subractor

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/b4a73dfb-de85-464e-94c1-dd70b93cdd35)



full subractor

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/0873ed84-48b3-481c-9b90-79c9e693b104)




## Timing diagram 

![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/376e5a3a-93cc-48fd-b75a-e21b9876f37a)


![image](https://github.com/Msuren48106/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/150503875/2e8b674e-9a26-4fc4-a4c8-03ea66f0a366)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
