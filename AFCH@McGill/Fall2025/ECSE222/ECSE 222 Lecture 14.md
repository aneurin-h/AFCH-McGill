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
