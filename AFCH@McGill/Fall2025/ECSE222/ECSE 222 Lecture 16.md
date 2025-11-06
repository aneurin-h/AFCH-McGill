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

# Sequential Circuits
# Basic Memory Elements - SR Latch