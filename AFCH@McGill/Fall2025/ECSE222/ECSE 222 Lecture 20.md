# Synchronous Counters
Flip Flops share the same clock
Advantages: No Ripple Delay
![[image-68.png|428x148]]
## Modulo-k Counters
Wire an NAND gate from binary rep of k (from at least $\log_{2}{k}$ bits), and use that to clear all FFs
Holds value of k for less than one clock cycle, as clear is asynchronous

## Synchronous 4-bit Up Counter w/ Enable
![[image-69.png|459x235]]
XOR gate makes DFF into a TFF
Output carry can be used to concatenate multiple counters
	2 4-bit counters -> 1 8-bit counter
### Timing
$Q_{0}$ has $t_{cq}$ delay, + delay of all AND gates & the XOR,  to reach $Q_{3}$ 
Setup Time and Max Frequency:
Find Critical Path (3AND + XOR)
$T \geq{}t_{cQ}+3t_{AND}+t_{XOR}+t_{su}$
$f_{max}=\frac{1}{t_{cq}+3t_{AND}+t_{XOR}+t_{su}}$
Hold Time:
Find shortest delay path starting and ending at FF (XOR)
$t_{cq}+t_{XOR}\geq{}t_{h}$
### Improving Timing
Increase fan-in
![[image-70.png|251x240]]
Critical path is reduced to one AND gate
## Synchronous 4-bit Up Counter with Enable and Parallel Load
![[image-71.png|197x209]]
Used to start the counter counting from a different point than 0
Similar to how the clear was used previously
# Counters with Parallel Load
Can fix problem form earlier about not holding value of k for long enough
	Load only takes effect at the rising edge of the clock
![[image-72.png|257x137]]
# Concatenating Counters with Enable and Output Carry
Use output carry of first counter as enable for second
	Thus the second will only tic