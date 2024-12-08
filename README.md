# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)
![WhatsApp Image 2024-12-08 at 19 34 36_49761c85](https://github.com/user-attachments/assets/0018f35b-4ea4-4e3f-92bb-c7336d0f1fde)


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)
![WhatsApp Image 2024-12-08 at 19 34 36_eeee9732](https://github.com/user-attachments/assets/ddf8ef10-36fb-4897-87ec-614d04facd4c)


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

![WhatsApp Image 2024-12-08 at 19 34 37_1bfe2f72](https://github.com/user-attachments/assets/47e7e1cb-8637-42f7-9c5e-ec7fbc12fe04)

![WhatsApp Image 2024-12-08 at 19 34 36_62e2e426](https://github.com/user-attachments/assets/97b82af8-af5f-41af-b5b9-c35e4946b5cc)


**Procedure**

Write the detailed procedure here

**Program:**

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^c);

assign carry= ( (a & b)| ( cin &(a ^ b ));

endmodule


module fs(a,b,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

![WhatsApp Image 2024-12-08 at 19 34 38_b7e02c43](https://github.com/user-attachments/assets/dfce283e-84ea-4825-ae3d-1b59f3d58585)

![WhatsApp Image 2024-12-08 at 19 34 38_63b912b2](https://github.com/user-attachments/assets/a35e2f5e-b926-4671-9784-d35b6cbb57b1)


**Output Timing Waveform**

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



