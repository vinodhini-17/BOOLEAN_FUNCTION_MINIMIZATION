# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module experiment2(a, b, c, d, w, x, y, z, f1, f2);
input a, b, c, d, w, x, y, z;
output f1, f2;
wire x1, x2, x3, x4, x5, y1, y2, y3, y4, y5;
assign x1 = ((~a) & (~b) & (~c) & (~d));
assign x2 = (a & (~c) & (~d));
assign x3 = ((~b) & (c) & (~d));
assign x4 = ((~a) & b & c & d);
assign x5 = (b & (~c) & d);
assign f1 = x1 | x2 | x3 | x4 | x5;


assign y1 = (x & (~y) & z);
assign y2 = ((~x) & y & z);
assign y3 = ((~w) & x & y);
assign y4 = (w & (~x) & y);
assign y5 = (w & x & y);
assign f2 = y1 | y2 | y3 | y4 | y5;
endmodule
````````` 

Developed by:K VINODHINI 
RegisterNumber: 212223230245


**RTL realization**

**Output:**

**RTL**
![{18536CFA-EE90-4478-88B7-059F0CEC72E2}](https://github.com/user-attachments/assets/0f8a8a16-b646-4e70-8e90-347529be81f4)

**Timing Diagram**
![{1C303F21-3664-491A-A622-9241F9DFC1F5}](https://github.com/user-attachments/assets/fe0656da-7037-46e6-b802-1d0017c98e0f)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

