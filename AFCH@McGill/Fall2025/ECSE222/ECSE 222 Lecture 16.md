Lecture 15 Slides
# Switches
## P & N Type switches
P type: Input low, switch on; input high, switch off
N type: input low, switch off; input high, switch on
## Inverter using Switches
![[image-33.png|179x210]]
When in=0, P is closed, pulling out to VDD, N is open
When in=1, N is closed, pulling out to GND, P is open
# NAND Gates
![[image-34.png|251x281]]
# Buffers
Enhance signal quality
Reduce susceptibility to noise
![[image-35.png|145x55]] denoted as:![[image-36.png|96x55]]
Used to delay signal for timing benefits
## Tri-State Buffers
Has three ports, (IN, OUT, & EN)
If not enabled, output is Z (high impedance/open circuit)
	Implemented with pass gates
### 4 Types of Tri-State Buffer
![[image-37.png|309x186]]
## Tri-State Bus
Multiple Tri-State Buffers, with outputs wired together
Enable pins selected by decoder
Using 1-hot encoding, only one input writes to the bus at a time
# Regular Structures
## ROM (Read Only Memory)
Preset regular structure of memory - permanent 0s or 1s
Address line to choose certain memory cell
Permanent memory - stored through power off
Cannot be written to
## RAM (Random Access Memory)
Supports writing
Implemented using a latch (SRAM)
Regular structure in an array fashion
Also has a select line (1 = write, 0 = read)
# Sequential Circuits
Sequential Circuits "remember" previous state
Output at time $t$ depends on inputs at time $t$ and on previous inputs
Require memory elements
Contents of sequential circuit blocks contain the state of the circuit
## Memory Elements
![[image-38.png]]
Not optimal as we cannot set Q
Better Version:
![[image-39.png|251x236]]
Allows 
# Basic Memory Elements - SR Latch