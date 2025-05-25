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

  module exp2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule
```
Developed by: Kshira K

Register Number: 212224040166


**RTL realization**

**Output:**

**Truth Table**

i) F1
![image](https://github.com/user-attachments/assets/e7db0fba-d7d8-4425-a6da-fac3a5d34233)

ii) F2
![image](https://github.com/user-attachments/assets/19f5c359-1631-4dd3-843f-880e4e2da32f)

**RTL**
![image](https://github.com/user-attachments/assets/e6992d5f-a547-4543-8d73-3d0f0ba8a1e8)

**Timing Diagram**
![image](https://github.com/user-attachments/assets/45f44c64-90dd-4db9-ad43-0d76e17acc5f)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
