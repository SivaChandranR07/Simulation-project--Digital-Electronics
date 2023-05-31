# TITTLE
To Design and simulate mod 5 synchronous upcounter with JK flip flop using Verilog.

# THEORY
Synchronous Counters: It means that all flip-flops are clocked concurrently. The clock pulses drive the clock input of each flip-flop together hence there is no propagation delay.

Mod-5 Counter Synchronous Counter: This have five counter states. The counter design table for such counter shows the three flip-flop and their states also (0 to 5 states), as in table (a), the 6 inputs needed for the three flip-flops. The flip-flop inputs needed to step up the counter from the current to the next state have been worked out along with the assist of the excitation table illustrated in the table.


# LOGIC DIAGRAM
![Logic diragram](https://github.com/SivaChandranR07/Simulation-project--Digital-Electronics/assets/113497395/55e5bd07-4e7c-48dc-a60b-d4cc38badda1)

# NETLIST DIAGRAM
![netlist](https://github.com/SivaChandranR07/Simulation-project--Digital-Electronics/assets/113497395/c576ca8a-8a19-45f3-966a-0603365a8fe5)

# TIMING DIAGRAM
![timing diagram](https://github.com/SivaChandranR07/Simulation-project--Digital-Electronics/assets/113497395/4e2cd876-727c-464e-a0ef-fbd51b48d523)

# PROGRAM
```
module modfivecounter(q, qbar, j, k,clk, rst, pr);
output [2:0] q, qbar;
input clk, j, k;
input rst, pr;
wire a;
nand n1(a,q[1],q[2]);
JKFF_Pos_Edge jkff0(q[o],
qbar[0],j,k,clk,a,pr);
JKFF_PoS_Edge jkff1 (q[1],
qbar[1],j,k,qbar[0],a,pr);
JKFF_PoS_Edge jkff3(q[2],
```

# REFERENCE
https://www.ques10.com/p/6667/design-a-mod-5-synchronous-up-counter-using-j-k--1/
