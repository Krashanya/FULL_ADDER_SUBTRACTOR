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
Full Adder:

<img width="585" height="663" alt="image" src="https://github.com/user-attachments/assets/decd4b2e-3f7f-4142-8355-33dcfcaef8e2" />

Full subtracter:

<img width="768" height="705" alt="image" src="https://github.com/user-attachments/assets/553bc1c3-3383-4f30-8b04-bfc1056c4c98" />

**Procedure**

**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
Full adder:
```
module exp4(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule
```
Full subtracter:
```
module exp4a(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
```

**RTL Schematic**
Full adder:

![WhatsApp Image 2026-03-23 at 8 44 43 PM](https://github.com/user-attachments/assets/c34110b4-7b67-45c2-aee6-09010610f892)

Full subtracter:

![WhatsApp Image 2026-03-23 at 8 46 47 PM](https://github.com/user-attachments/assets/a2f5ef4d-edd1-4ab4-9e77-96dae28d3cd2)


**Output Timing Waveform**
Full adder:

<img width="1463" height="825" alt="image" src="https://github.com/user-attachments/assets/270d4382-aa30-423d-8a0e-1a7816368710" />

Full subtracter:

<img width="1460" height="816" alt="image" src="https://github.com/user-attachments/assets/8ecba32e-4cd9-4598-b96e-debe74660c5a" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



