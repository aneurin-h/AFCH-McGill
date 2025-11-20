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
Inputs: load/shift, In, CLK, as well as parallel inputs
Outputs: Parallel outputs, and serial out
load/shift = 0, Input is shifted in at next clock cycle
load/shift = 1, Loads from parallel input at next clock cycle
Used for parallel to serial conversion, or for serial to parallel conversion
# Counters
## Up-Counters
Counts up, at positive CLK edge
## 1-Bit counter
Counts modulo 2, i.e. $0\to 1 \to 0 \to 1 \to 0 \to 1 \to\dots$
Implemented via TFF
Frequency divider, will halve the frequency of the CLK input
## 2-Bit Asynchronous Up-Counter
Counts up through 0,1,2,3 and then overflows and repeats
$Q_{1} \text{ changes at the falling edge of }Q_{0}$
Implementation, 2 TFFs, with the CLK of the second driven by the negation of output of the first
## 3-Bits (Asynchronous Up)
Same as above, but 0-7 counting, ie modulo 8
Implementation:
Same as above, with the third TFF also being set to the falling edge of the second TFF
## Down-Counters
Counts down, at positive CLK edge
## 3 Bit (Asynchronous Down)
TFFs toggle on positive edges of the previous

# Asynchronous
Due to $t_{cq}$ delay, changes have to ripple through counter
if $nt_{cq}$ exceeds clock period, can cause errors when reading parallel out
# Synchronous
