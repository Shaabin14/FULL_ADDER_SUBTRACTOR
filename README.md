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

![de12](https://github.com/user-attachments/assets/c227a539-5077-452e-a1cd-c14e5ebd5e32)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![de13](https://github.com/user-attachments/assets/d20c843a-7654-4ac1-a627-90b304771956)




Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
a b cin sum carry 0 0 0 0 0 0 0 1 1 0 0 1 0 1 0 0 1 1 0 1 1 0 0 1 0 1 0 1 0 1
 1 1 0 0 1 1 1 1 1 1 

![de14](https://github.com/user-attachments/assets/fe0c354a-2abe-471a-866b-bd1e2d5b9513)


 
a b bin difference borrow 0 0 0 0 0 0 0 1 1 1 0 1 0 1 1 0 1 1 0 1 1 0 0 1 0 1 0 1 0 0 1 1
 0 0 0 1 1 1 1 1 

![de15](https://github.com/user-attachments/assets/f046a104-f04b-4f0a-aeb5-6f0c88b429dd)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
 module fulladder(a, b, cin, sum, carry);
 input a, b, cin;
 output sum, carry;
 assign sum = ( (a ^ b) ^ cin );
 assign carry = ( (a & b) | ( cin & (a ^ b) ) );
 endmodule
```
```
 module fullsub(a,b,bin,difference,borrow);
 input a,b,bin;
 output difference,borrow;
 assign difference = (a ^ b)^bin;
 assign borrow = ( a & b) | ( bin & ((a ^ b )));
 endmodule
``` 
Developed by:SHAABIN R S RegisterNumber:24006663*/

**RTL Schematic**

![de16](https://github.com/user-attachments/assets/d80e84e2-a389-4343-baec-d210d6f782f9)


**Output Timing Waveform**

![de17](https://github.com/user-attachments/assets/b89ec231-f771-4979-9a70-01319a4e75db)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



