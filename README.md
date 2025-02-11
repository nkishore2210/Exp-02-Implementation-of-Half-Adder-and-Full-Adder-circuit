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
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Kishore.N
RegisterNumber: 22008365 
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


### Output:

Half adder:

RTL:
![image](https://user-images.githubusercontent.com/118707090/214297504-66ca63a9-6a37-4c7c-8590-7592e229d610.png)
truth table:
![image](https://user-images.githubusercontent.com/118707090/214297882-7e707a72-7112-4dc5-b06e-6a1de135f575.png)
waveform:
![image](https://user-images.githubusercontent.com/118707090/214298194-22885a9b-fd47-45bb-b09b-d7eda3295616.png)

Full adder:

RTL:
![image](https://user-images.githubusercontent.com/118707090/214298438-c5790e1e-99f2-49fe-a185-75b0b7af223c.png)
truth table:
![image](https://user-images.githubusercontent.com/118707090/214298660-9e480e05-912a-4c87-ade7-61aa462d94b1.png)
waveform:
![image](https://user-images.githubusercontent.com/118707090/214298864-a4b66ba7-fc8e-4d8f-863a-8e45c90f6f24.png)







### Result:
Thus these programs are executed successfully.
