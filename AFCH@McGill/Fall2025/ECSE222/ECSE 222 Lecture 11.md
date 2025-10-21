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
![[image-10.png|343x190]]

Multiple stages implemented together using Ripple Carry Adders (RCA)
Several Full Adders chained
![[image-11.png|501x129]]

### Latency of RCA
Depends on the ripple (propagation) of the carry
	Assume x&y arrive together at start
Latency of FA (Critical path)
	$\tau{}_{FA\_carry} = 2$
	$\tau{}_{FA\_sum} = 1$
RCA Latency
	$\tau{}_{RCA}=2n$

## Signed Numbers
Three ways to represent negatived numbers
- Sign and magnitude
- 1s complement
- 2s complement

### Sign and Magnitude
1 bit for sign (first/leftmost)
A signed 4 bit integer is actually 5 bits, because of the sign bit
$5\rightarrow{}00101$
$-5 \rightarrow{}10101$

### 1's Complement (or (r-1)'s Complement)
Given a positive n-digit number P in radix r
	The equivalent n-digit negative number $K_{r-1}$ (radix r -1) is obtained as follows
	$K_{r-1}=(r^n-1) - P$
Equivalent to flipping each bit
$P+K_{r-1}=(r^n-1)$

### 2's Complement (or r's complement)
Given a positive n-digit number P in radix r
	The equivalent n-digit negative number is $K_r=r^n-P$
Example: 4 digit num in radix 2$
$P=5 = 0101$
$K_r = 1011 = 1010 + 1$
Flip bits and add 1
$K_r=10000-0101= 1011$
