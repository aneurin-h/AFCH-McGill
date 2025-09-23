- Karnaugh Maps (K Maps)
	- Minimization Using K-Maps
		- Fewest Implicants
		- Maximum size of each implicant
			- Group size must be between 0 and n (num of variables)
		- Extract function by ORing expressions that represent each implicant
		- Largest implicants results in lowest cost
			- Not always certain to provide minimum cost
			- 85% of the time it will
		- x+x'y - minimize
	![[Pasted image 20250923091149.png]]
	- 
		- XOR would have cost 1, unless we are not allowed to use it
		- K-Map does not give minimal cost if it would use more complex gates
- Minimization continued
	- f=x'yz+xyz'+y'z'+x'z+z

| z    xy | 00  | 01  | 11  | 10  |
| ------- | --- | --- | --- | --- |
| 0       | 1   | 1   | 1   | 1   |
| 1       | 1   | 1   | 1   | 0   |
Minimal form is f=x'+y+z'

# 4 Var
![[Pasted image 20250923093329.png]]
Cells can be adjacent over vertical and horizontal edges

# 5 Var
![[Pasted image 20250923094346.png]]
![[Pasted image 20250923094425.png]]
Used because if we simply had 3 vars along the top, then adjacency would not be coherent

