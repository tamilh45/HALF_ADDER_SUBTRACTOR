# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber: 212223110058
*/
**3.1**
```
module exp31(A,B,Cin,Sum,Carry);
Input A,B,Cin;
Output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=((A^B)&Cin)|(A&B);
endmodule
```
**3.2**
```
 module exp32(a,b,diff,borrow);
input a,b;
output diff,borrow;
assign diff=(a^b);
assign borrow=(~a&b);
endmodule
```

**RTL Schematic**
# Half Adder
![434659585-8847e6af-3565-4e28-b0a0-62303248658e](https://github.com/user-attachments/assets/02a71124-3c32-4248-bc13-47b9b0996263)
# Half Subtractor
![434658132-0e929cf3-0d69-49ad-90cf-c1f5e08d51d9](https://github.com/user-attachments/assets/bf347a72-27cf-4186-8a2f-4deb824da3f2)


**Output/TIMING Waveform**

# Half Adder
![434658423-7e1f48c6-2078-4c2e-8b59-2efe67c34f30](https://github.com/user-attachments/assets/01e10be7-3fc9-495d-a57d-2af698709701)

# Half Subtractor
![434658507-43992652-4ceb-4aae-a3b0-5fb2af86c82b](https://github.com/user-attachments/assets/a1bd87e9-4a9a-4314-928e-8f83ad0d14d0)

**Result:**
Thus the Half-Adder-and-Half Subtractor-circuit is implemented.
