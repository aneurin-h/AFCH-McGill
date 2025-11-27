Lecture 19 Slides
# FSMs
System described using a set of finite states
![[image-76.png|370x164]]
Flip-Flops store the state of the system
First combinational segment decides next state based on current state and input
## Mealy FSMs
In Mealy FSMs, the output is a function of the state *and* the input
Pictured above
## Moore FSMs
Output is purely a function of the current state![[image-77.png|403x145]]
## Design Example - Sequence Detector
Given a stream of bits arriving at the rate of one bit per clock cycle
Detect two consecutive 1s
1. Design FSM (Moore)
   ![[image-78.png|360x202]]
2. State Table
   ![[image-79.png|359x174]]
3. State Assignment
   Encode states using 2 bits (as $2^2=4>3$)
   Store each bit $y_{1}\:\&\:y_{2}$ in an FF
   Next state variables are represented as $Y_{1}\:\&\:Y_{2}$
   