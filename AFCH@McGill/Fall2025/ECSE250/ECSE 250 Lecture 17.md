# Recursion
If a problem has an iterative solution, it has a recursive one as well
Recursion and Iteration are equally expensive

Recursion often used for more complex
## Computational Complexity
Algorithms with $O(n)$ & $\Omega(n)$ takes $\Theta(n)$
Less trivial to analyze for recursive functions
### Back Substitution
![[image-53.png|328x179]]
$T(n) = c + T(n-1)$
$T(n) = kc+T(n-k)$
$T(n) = (n-1)c+T(1)$
$T(n) = (n-1)c+b$

![[image-54.png|313x129]]
$T(1) = a$
$T(n) = b + cn + T(n-1)$
$T(n) = c(n+(n-1)+(n-2)+\dots{}+2) + T(1)$

## Tower of Hanoi
 1. Move n-1 disks from Start to Other
 2. Move nth disk from Start to Finish
 3. Move n-1 disks from Other to Finish
$2^n -1$ total moves
$2^i$ moves per layer, and $\sum_{i=0}^{n}2^i=2^n-1$
Thus $\Theta(2^N)$

With Recurrence:
Base Case time: $T(1) = b$
Recursive Case time 
$T(n)=c+2T(n-1)$
$T(n)=c+2c+4T(n-2)$
$T(n)=c(1+2)+4T(n-2)$
$T(n)=c(1+2+4)+8T(n-3)$

$T(n) = c(1+2+4+\dots{}+2^{k-1})+2^kT(n-k)$
$k=n-1$
$T(n) = c(2^{n-1}-1)+2^{n-1}b$
