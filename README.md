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

**Truthtable:**

1.FULL ADDER

![318405960-7116d2bf-8e90-4e96-bfd5-d62af11a317a](https://github.com/user-attachments/assets/52574d6f-58cd-45ae-a6b5-0d57142c3463)

2.FULL SUBTRACTOR

![318405667-33d8ba16-9169-40b0-8696-3bb8e5c3a0b7](https://github.com/user-attachments/assets/262810b8-e209-49cc-92dd-5ea3a7392477)


**Procedure:**
```
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
```

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: Deepak S

RegisterNumber:24007248

1.FULL ADDER
```
module fa(a, b, cin, sum, carry);
    input a, b, cin;
    output sum, carry;

    assign sum = (a ^ b) ^ cin;         
    assign carry = (a & b) | (cin & (a ^ b)); 
endmodule
```
2.FULL SUBTRACTOR
```
module fs(a, b, bin, difference, borrow);
    input a, b, bin;
    output difference, borrow;

    assign difference = (a ^ b) ^ bin; 
    assign borrow = (~a & b) | (bin & (~(a ^ b))); 
endmodule
```

**RTL Schematic:**

1.FULL ADDER
![Screenshot 2024-12-06 114927](https://github.com/user-attachments/assets/104cdd83-d75b-455a-a17b-89bd1d3e41b5)


2.FULL SUBTRACTOR
![Screenshot 2024-12-07 133445](https://github.com/user-attachments/assets/ae0d84aa-c180-4628-a18f-85bdab880d8e)


**Output Timing Waveform:**

1.FULL ADDER
![Screenshot 2024-12-06 115203](https://github.com/user-attachments/assets/0ddf6d83-4053-4679-a20c-163ddbd5a2b9)


2.FULL SUBTRACTOR
![Screenshot 2024-12-07 133647](https://github.com/user-attachments/assets/467c9778-7165-4cf0-aea3-3bdf0a9a9370)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



