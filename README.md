# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
**Developed by: CHANDRU M**
**RegisterNumber: 212222100009**
```
 module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
 input a,b,c,d,w,x,y,z;
 output f1,f2;
 wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
 not(adash,a);
 not(bdash,b);
 not(cdash,c);
 not(ddash,d);
 and(p,bdash,ddash);
 and(q,adash,b,d);
 and(r,a,b,cdash);
 or(f1,p,q,r);
 //type code for f2 as like f1
 not(ydash,y);
 and(s,x,y);
 and(t,ydash,z);
 and(u,w,y);
 or(f2,s,t,u);
 endmodule
```
**RTL realization**

**Output:**

![image](https://github.com/CHANDRUMANIKANDAN/BOOLEAN_FUNCTION_MINIMIZATION/assets/118644502/0a9f02bd-70ce-4ad1-89fe-215cc0ee88fb)


**Timing Diagram**

![image](https://github.com/CHANDRUMANIKANDAN/BOOLEAN_FUNCTION_MINIMIZATION/assets/118644502/66df13d8-4f63-4907-9f3e-521f2d7915f5)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
