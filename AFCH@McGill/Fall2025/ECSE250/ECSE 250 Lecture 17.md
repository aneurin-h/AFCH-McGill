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