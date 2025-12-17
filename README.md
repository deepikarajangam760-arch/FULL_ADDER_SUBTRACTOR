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
**RTL Schematic**
<img width="1920" height="1020" alt="Screenshot 2025-11-24 100412" src="https://github.com/user-attachments/assets/9f4ee2f8-6a7e-468c-9dc2-ba1209bd937d" />


**Output Timing Waveform**
<img width="1920" height="1020" alt="Screenshot 2025-11-24 101057" src="https://github.com/user-attachments/assets/fb26abdd-9099-434c-99da-f11208a1efb4" />


**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

**Full Adder**

module exp4(df,bo,a,b,bin);

output df;

output bo;

input a;

input b;

input bin;

wire w1,w2,w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(~w1&bin);

assign df=w1^bin;

assign bo=w2|w3;

endmodule

**Full Subtractor**

module full_subtractor(diff, borrow, a, b, bin);

  output diff;
  
  output borrow;
  
  input a;
  
  input b;
  
  input bin;
  
  assign diff = a ^ b ^ bin;
  
  assign borrow = (~a & b) | (~(a ^ b) & bin);
  
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:R.DEEPIKA

RegisterNumber:25016530
*/

**RTL Schematic**
<img width="1920" height="1020" alt="Screenshot 2025-11-24 130926" src="https://github.com/user-attachments/assets/074993f5-05ad-4348-bea2-ad9198cc8218" />



**Output Timing Waveform**
<img width="1920" height="1020" alt="Screenshot 2025-11-24 132211" src="https://github.com/user-attachments/assets/069e2d6c-3810-4425-b16b-cdf1e04277a2" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



