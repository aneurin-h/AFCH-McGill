# Lecture 8 Slides
## Factoring To Reduce Fan-In
Use Distributive Property to reduce Fan-In

Can share functions including negating output for one subcircuit (Cost likely lower than reusing)

Cannot apply DeMorgan's on solely one part

## Functional Decomposition
![[Pasted image 20251002090658.png|487x260]]
$g$ is an xor gate here
Can find common subcircuits, and re-use them to decrease cost
In this example $f = gx_3 + g'x_4$ is a 2->1 MUX

### Using Karnaugh Maps
GOING TO BE ON THE EXAM FOR SURE

Identify patterns along cols/rows of K-Maps
Identify input variables to serve as inputs to subfunction
Choose rows or columns that correspond to the cells with 1s

![[image-3.png|474x242]]
Choice of $g$ and $g'$ dont matter, as they will both be present
![[image-4.png|475x243]]
Always use SoP for this

Can use patterns of rows with patterns of columns

