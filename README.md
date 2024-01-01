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

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
## HALF ADDER
## Program:
module project_3(sum,carry,a,b);

input a,b; 

output sum,carry; 

xor sum1(sum,a,b); 

and carry1(carry,a,b); 

endmodule
## Developed by: Shivaram.M
## RegisterNumber: 212223040195
## Logic symbol & Truthtable:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/34265563-37b3-4de9-8362-f5a566327751)

## RTL realization:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/7f729b0d-6547-427a-9c53-f0bb9880aac3)

## Timing diagram:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/a5026e58-d9a3-4380-a7a9-b5b061567cb3)

## FULL ADDER
## Program:

module project_3_2(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule

## Logic Symbol & Truth Table:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/b2767a88-c917-47a0-8218-e9a4eb1df0b1)

## RTL Realization:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/6293bbd8-44c8-4bb9-95bb-51b015b3e274)

## Timing diagram:

![image](https://github.com/Shivaram2525/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144226303/52a3cefa-9953-40e7-80bf-3a6f283b30be)

### Output
### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
