# Lecture 10 Slides
## 2's Complement
Used often in computer architecture
Only one zero

Subtraction much easier
## Addition and Subtraction
### Sign and Magnitude
#### Addition
If signs are equal, add magnitude
	Result has same sign
Different signs:
	Requires borrowing (like subtraction)
	Small number (Absolute Value) must be subtracted from large number (absolute value)
	Keep sign of larger number
	![[image-12.png|424x109]]
#### Subtraction
Same signs
	Small number subtracted from larger number (absolute value), if flipped numbers, flip signs in output
Different signs
	Addition 0->flip sign of subtrahend (?) -> sign of result as the new sign of subtrahend
	Requires additional circuitry (comparators)
![[image-13.png|571x100]]

### 1's Complement
#### Addition
Result without carry out
	Straightforward
Result with carry out
	Add Carry out to result
	Additional circuitry required (extra addition step)
#### Subtraction
For positive numbers
	Straightforward
For negative numbers
	Complex
### 2's Complement
Real circuits use this, nice and easy
#### Addition
No Carry out
	Straight forward
Carry out
	Ignore carry out
#### Subtraction
Negate subtrahend with 2's complement
Preform addition

### Adder/Subtractor Unit
Given two n-bit numbers in 2's complement representation
Design a circuit that can preform both x+y and y+x
Type of operation controlled by a control signal $\bar{Add}$ / $Sub$ 
$\bar{Add}$ / $Sub$ = 0, add
$\bar{Add}$ / $Sub$ = 1 subtract

2's Complement of y = 1's complement of y + 1
y xor 0 = y
y xor 1 = not y

![[image-14.png|408x193]]
XOR circuitry + Carry in converts y to 2's complement of y if control signal is 1

