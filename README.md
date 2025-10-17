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
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.
Write the detailed procedure here

**Program:**

Developed by: d.amrida varshini
registerNumber: 25004322

verilog
//Full adder

module EXP3_2 (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
verilog
//Full subtractor
module EXP3_4 (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

**RTL Schematic**
1.FULL ADDER
<img width="1016" height="767" alt="image" src="https://github.com/user-attachments/assets/c0c336dc-5364-40b7-9de1-8985d0b886c6" />
2.FULL SUBTRACTOR
<img width="1020" height="422" alt="image" src="https://github.com/user-attachments/assets/4bd78fc8-9509-473e-87a2-d3a87cccd1f8" />

**Output Timing Waveform**
1.FULL ADDER
<img width="1318" height="241" alt="image" src="https://github.com/user-attachments/assets/c3242772-6f6a-44e5-9d8c-11cd4d7c20b8" />
2.FULL SUBTRACTOR
<img width="1316" height="314" alt="image" src="https://github.com/user-attachments/assets/4a0dadf0-37db-4fd0-935a-6dfc552af1e7" />
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



