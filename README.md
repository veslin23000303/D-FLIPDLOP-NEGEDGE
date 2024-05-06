# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Declare ports for the D flip-flop module, specifying inputs (D, CLK) and outputs (Q, Q_bar).

2.Write Verilog code to create the functionality of the D flip-flop, triggered by the rising edge of the clock signal (posedge CLK).

3.Develop a Verilog testbench to simulate how the D flip-flop responds to different input scenarios.

4.Set up the testbench to test various combinations of input signals (D, CLK) to cover all possible states.

5.Confirm that the D flip-flop's outputs (Q, Q_bar) behave as expected according to its functional table.

6.Ensure that the design doesn't encounter race conditions or undefined states by analyzing the timing and sequence of input changes.

**PROGRAM**
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by:VESLIN ANISH A RegisterNumber: 212223240175
```
```
module DFLIPFLOPNEGEDGE(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![WhatsApp Image 2024-05-06 at 14 21 49_73b241bd](https://github.com/veslin23000303/D-FLIPDLOP-NEGEDGE/assets/151148539/aa6ef522-5cfd-4392-86e8-cb5e694836a6)


**TIMING DIGRAMS FOR FLIP FLOPS**
![WhatsApp Image 2024-05-06 at 14 21 30_2d043209](https://github.com/veslin23000303/D-FLIPDLOP-NEGEDGE/assets/151148539/4f00806d-c9ee-4289-88b5-96daa80c8a92)

**RESULTS**

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.
