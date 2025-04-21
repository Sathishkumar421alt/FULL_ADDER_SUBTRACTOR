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

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
```
 module fa(a,b,cin,sum,carry);
 input a,b,cin;
 output sum,carry;
 assign sum=( (a ^ b)^cin);
 assign carry= ( (a & b)| ( cin &(a ^ b )));
 endmodule
 module fs(a,b,bin,difference,borrow);
 input a,b,bin;
 output difference,borrow;
 assign difference= ( (a ^ b)^bin);
 assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
 endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: RegisterNumber:SATHISH KUMAR.T/2122241000563
*/

**RTL Schematic**

![Screenshot 2025-04-21 155131](https://github.com/user-attachments/assets/6263aa08-b09e-4314-86ef-8a663978e200)
![Screenshot 2025-04-21 155216](https://github.com/user-attachments/assets/01a4c7e0-846c-47f4-b9f7-be606def075b)



**Output Timing Waveform**
![Screenshot 2025-04-21 155229](https://github.com/user-attachments/assets/7f866101-6d61-4440-9fc8-2bfb988a52cb)
![Screenshot 2025-04-21 155229](https://github.com/user-attachments/assets/5524ef8c-9740-4f0b-9f55-dd7c60066c26)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



