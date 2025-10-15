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

 Addition, 1 = Subtraction output Sum_Diff, // Output: Sum or Difference output
 Cout_Bout // Output: Carry or Borrow );
 
 wire B_xor_mode;   // B modified for subtraction
 wire sum1, carry1, carry2;
 
 // XOR B with mode → if mode=1, B becomes ~B (for subtraction)
 assign B_xor_mode = B ^ mode;
 
 // Full Adder logic
 assign Sum_Diff = A ^ B_xor_mode ^ Cin;  
assign carry1   = A & B_xor_mode;
 assign carry2   = Cin & (A ^ B_xor_mode);
 assign Cout_Bout = carry1 | carry2;
 endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:k.sadhana RegisterNumber:25013407

**RTL Schematic**

<img width="1361" height="512" alt="image" src="https://github.com/user-attachments/assets/efd94deb-d417-404d-9bdd-d41fa3b0b072" />


**Output Timing Waveform**

<img width="1372" height="350" alt="image" src="https://github.com/user-attachments/assets/7a8bd0ca-2c39-4f2a-bf75-673d5ab91a24" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



