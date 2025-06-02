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

Developed by : Kshira K

Register Number :212224040166
  
**Truth Table**
i)F1
![image](https://github.com/user-attachments/assets/34c74a5d-4e82-4741-a6e2-bf0de1ade9a8)


ii)F2
![image](https://github.com/user-attachments/assets/79008ed0-2390-4424-b204-95f2bd1bee16)



**RTL**
![image](https://github.com/user-attachments/assets/e421164b-8abc-4f36-8f83-2a3e9ef35532)

**Waveform**
![WhatsApp Image 2025-04-16 at 03 41 16_74967713](https://github.com/user-attachments/assets/ac2a1b7e-06d0-4f7f-bb80-b40f5403899f)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
