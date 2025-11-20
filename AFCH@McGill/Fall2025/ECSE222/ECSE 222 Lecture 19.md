Lecture 17 Slides
# Registers
Inputs: $x_{n-1}, x_{n-1},\dots,x_{1},x_{0}$ & $load, CLK$
Outputs: $Q_{n-1},Q_{n-2},\dots,Q_{1},Q_{0}$
If load is high, and on a CLK rising edge, inputs are stored to the state
Otherwise, on a CLK rising edge, the state is output
## Implementation
n DFFs, all tied to same CLK signal
D pins are driven by a MUX switching on load, with the current state and the input as its inputs
# Shift Registers
Inputs: $In\:\&\: Clk$
Shifts outputs to the next ($n\to n+1$) output on $Clk$ rising edge
Last bit is discarded
## Implementation
n DFFs
D input is driven by output of previous flip flop, or the input in the n=0 case
# Parallel Access Shift Register
Inputs: load/shift, In, Clk, as well as parallel inputs
Outputs: Parallel outputs, and serial out
