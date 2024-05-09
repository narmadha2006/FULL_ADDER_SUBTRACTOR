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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: NARMADHA S  RegisterNumber: 212223220065

```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```

**RTL Schematic**

![Screenshot 2024-05-09 171142](https://github.com/narmadha2006/FULL_ADDER_SUBTRACTOR/assets/151390280/12ae8965-13e9-461c-8367-4e9618177455)


**TRUTH TABLE**

**FULL ADDER**

![Screenshot 2024-05-09 171154](https://github.com/narmadha2006/FULL_ADDER_SUBTRACTOR/assets/151390280/cd50e036-6f89-4e40-b65b-63d5ba5978df)

**FULL SUBTRACTOR**


![Screenshot 2024-05-09 171204](https://github.com/narmadha2006/FULL_ADDER_SUBTRACTOR/assets/151390280/9fc751cf-128d-4c51-be3d-e07276a90656)


**Output Timing Waveform**

![Screenshot 2024-05-09 171215](https://github.com/narmadha2006/FULL_ADDER_SUBTRACTOR/assets/151390280/f0023fcf-e57b-42ed-b812-b1a3565d3c35)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



