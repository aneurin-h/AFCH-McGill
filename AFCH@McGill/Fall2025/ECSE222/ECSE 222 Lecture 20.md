# Synchronous Counters
Flip Flops share the same clock
Advantages: No Ripple Delay
![[image-68.png|428x148]]
## Modulo-k Counters
Wire an NAND gate from binary rep of k (from at least $\log_{2}{k}$ bits), and use that to clear all FFs
Holds value of k for less than one clock cycle, as clear is asynchronous