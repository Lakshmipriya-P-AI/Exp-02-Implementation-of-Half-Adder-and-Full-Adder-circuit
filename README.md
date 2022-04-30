# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.

### Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Lakshmi Priya
RegisterNumber:  212221230053
*/

HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
## Output:
## Half Adder :
## Logic symbol :
![ex2 LS](https://user-images.githubusercontent.com/93427923/164619529-5e995fc3-51b3-4b32-9c91-d17f3efe804c.png)

## RTL realization :
![ex2 RTL](https://user-images.githubusercontent.com/93427923/164620603-8988279f-ac8a-4f81-b302-171942bc8331.png)

## Truthtable:
![ex2 tt1](https://user-images.githubusercontent.com/93427923/164625645-a7a8401e-48d8-456c-9a07-66b1d5c35df6.png)

### TIMING DIAGRAM:
![dee924e1-f275-4589-9b4d-f0a3113340ce](https://user-images.githubusercontent.com/93427923/166093958-dde56873-9f33-4ac1-a592-0da54bb80aff.jpg)


## Full Adder :
## Logic Symbol:
![ex2 lg](https://user-images.githubusercontent.com/93427923/164621971-565e0019-2c89-44bc-9127-0df22ea50329.png)

### RTL:
![ex2 r](https://user-images.githubusercontent.com/93427923/164622157-0b4b602f-f342-49ed-b300-2cbcddbd15a8.png)

### TRUTH TABLE 
![faddtable](https://user-images.githubusercontent.com/93427923/166094150-70e8e282-c877-4f04-b93a-098911eea44c.png)

### TIMING DIAGRAM:
![190f57e3-5d31-4ee2-a0a4-4ce3f64ec238](https://user-images.githubusercontent.com/93427923/166093964-8010a5f2-d46a-4f92-a1b5-803336bb3601.jpg)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
