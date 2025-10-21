# Lecture 10 Slides
## Delay
Critical path: longest (time) path of a circuit

## Bit Addition
x + y = cs, c = carry, s = sum
$0+0=00,0+1=01,1+0=01,1+1=\color{red}{1}\color{white}0$

s = x XOR y
c = x AND y
This is a **half adder** (One bit added with another, 2 inputs)
![[image-9.png|189x146]]

Binary addition preformed in stages, corresponding to place
Each stage is addition of 3 bits, $x_i,y_i,c_i$ where c is the carry-in
$x_i+y_i+c_i=c_{i+1}s_i$
This is a full adder (Because it uses carry-in)

Boolean functions for full adder
$c_{i+1} = x_iy_i + x_ic_i+y_ic_i$ 3 AND gates and 1 OR gate
$s_i=x_i\oplus{}y_i\oplus{}c_i$
![[image-10.png]]
