# Lecture 11 Slides
## Multiplexer MUX
Allows selection between a number of outputs
Can be used to implement XOR
Diagrams in slides

### Ex. Majority Function
![[image-16.png]]
Corresponds to which value (0 or 1) appears most often in the inputs
![[image-18.png|371x156]]
![[image-19.png|371x175]]

## Shannon's Expansion
Set a particular variable to either 0 or 1, -> creates a **cofactor** of f 
$f_{x_1}=^\Delta{}f(1,x_2,x_3,...,x_n)$
Any function $f(w_1,w_2,...w_n)$ of $n$ binary variables can be expanded in terms of co-factors
$f=w_1f_{w_1} + \bar{w_1}f_{\bar{w_1}}$
