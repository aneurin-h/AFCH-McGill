# Lecture 7 Slides
## Multiple Output Circuits & Joint Implementation
Combining multiple functions in order to save cost
Share gates between the functions

Steps to design:
- Create individual K-Maps
	- Group into prime implicants
- Identify shared implicant
- Add non-shared implicants
- Draw combined circuit diagram reusing the overlapped implicants
Won't *always* reduce cost
Don't have to always stick solely to prime implicants

Can pick selection of prime and non prime implicants to find optimal multi-output solution
There are likely multiple combinations to check
	Have to check all, and compare costs
Joint implementation can be worse than individual implementations
## Fan-In & Fan-Out
Fan-In
	Number of inputs to the gate
Fan-Out
	Number of gates connected to its output (number of gates it drives)
	Output counts as a gate

 Often imposed as requirements due to the technology used (heat, power, space, etc)

## Two Level Synthesis
POS & SOP are two-level circuits
1st level is the AND (or OR) of the inputs, the 2nd level is the OR (or AND) of those outputs

Typically efficient for functions with few variables

Need to use multiple levels to deal with Fan-In problems
![[Pasted image 20250930093936.png|471x180]]
