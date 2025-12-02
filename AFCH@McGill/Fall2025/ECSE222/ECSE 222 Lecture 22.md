Lecture 20 Slides
# Mealy FSMs
Output is a function of current state and of input
Specify the output for each input state combination
**Outputs are represented on the arrows, outside of the states**
## Example
Sequence Detector
Serial data stream, detect two consecutive ones (ie current and immediately previous)
**State Diagram**
![[image-86.png|586x119]]
**State Table**
![[image-87.png|346x132]]
Only need one FF to store the singular state bit that encodes our two states
**State Assigned Table**
![[image-88.png|300x128]]
