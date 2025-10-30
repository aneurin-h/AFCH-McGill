# Lecture 12 Slides
# FPGAs
![[image-22.png|318x253]]
## I/O Blocks
Contain the physical pins
## Logic Blocks
LUT (Look Up Table)
Typical 4-5 input LUT, with $2^n$ to 1 MUX
## Interconnection switch
Programmable switch that configures connections between the I/O Blocks and the Logic Blocks
Uses grid of horizontal and vertical wires, and allows connections to be either present or absent at their intersections
## Programming FPGAs
Set storage cells of LUTs
Program switches to connect
	Input pins to LUT inputs
	LUT outputs to LUT inputs
	LUT outputs to output pins
# Decoders
![[image-23.png|387x233]]
Converter from binary to decimal
Has an `En` (Enable) pin that activates decoder
If En is 0, no outputs are 1
If En is 1, exactly 1 output is 1
	Output is determined by the decimal number represented by inputs
"one-hot" encoding, only one bit is 1