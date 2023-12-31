# NAME:MALENI.M
# REGISTER NUMBER:212223040110
# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### EQUIPMENTS REQUIRED:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime
### THEORY:
Adders are digital circuits that carry out addition of numbers.
1. TYPE THE PROGRAM IN QUARTUS SOFTWARE.
2. COMPILE AND RUN THE PROGRAM.
3. GENERATE THE RTL SCHEMATIC AND SAVE THE LOGIC DIAGRAM.
4. CREATE NODES FOR INPUTS AND OUTPUTS TO GENERATE THE TIMING DIAGRAM.
5. FOR DIFFERENT INPUT COMBINATIONS,GENERATE THE TIMING DIAGRAM

### PROCEDURE:
1.Create a New Project: Open Quartus and create a new project by selecting "File" > "New Project Wizard." Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2.Create a New Design File: Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." Choose "Verilog HDL File".

3.Write the Combinational Logic Code: Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.Compile the Project: To compile the project, click on "Processing" > "Start Compilation" in the menu. Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.Analyze and Fix Errors:* If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. Review and fix any issues in your code if necessary. View the RTL diagram.

6.Verification: Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. Give the Input Combinations according to the Truth Table amd then simulate the Output waveform

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/984166b3-36b7-4c99-9b3b-777defd54fe1)


Sum = A’B+AB’ =A ⊕ B Carry = AB

### PROGRAM:
```
module de3hafeez(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
 ### RTL REALIZATION:
 ![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/1f6e1dd5-a633-4216-ada1-dafd241a22ed)

### TRUTH TABLE:
![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/2c8d8e52-c6e8-4f43-bde7-79110f46cc2e)

### TIMING DIAGRAM:
![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/7712f645-a909-4719-a4be-0586e302e440)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/a4f8fa7b-bc0a-4074-864e-40709086aa5d)
### PROGRAM:
```
module de3_1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b|b&c|a&c;
endmodule
```
### RTL REALIZATION:
![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/6bee143e-137a-4d38-ad4d-8e4662116d2c)
### TRUTH TABLE:
![image](https://github.com/MALENIMURUGAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870675/74d20077-fe96-45e7-ba92-2241a9ae3b90)

### RESULT:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
