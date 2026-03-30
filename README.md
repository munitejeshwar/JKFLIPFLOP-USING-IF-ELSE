# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**
1.type the program in quartus software.
2.compiler run the program.
3.generate RTL schematic and save the logic diagram.
4.creates nodes for input and output to generate the timing diagram.
5.for different input combinations generates the timing diagram

**PROGRAM**
~~~
module jk(clk, j, k, qi, gbar);
input j, k, clk;
output reg qi;
output gbar;
always @(posedge clk)
begin
    qi = ((~qi) & j) | ((~k) & qi);
end
assign gbar = ~qi;
endmodule
~~~
/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:MANIKANDAN M  RegisterNumber:212224040183
*/
**RTL LOGIC FOR FLIPFLOPS**
<img width="1121" height="686" alt="image" src="https://github.com/user-attachments/assets/8a0dd14a-c8f4-4386-a089-0cdbf6541e9a" />

**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1907" height="1124" alt="jk flipflop1 - Copy" src="https://github.com/user-attachments/assets/5673c543-9b88-42a9-b83c-ab5dcb3d95df" />


**RESULTS**
Thus the JK flipflop using verilog and validating their functionality using their functional tables implemented.
